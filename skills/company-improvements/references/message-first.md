# Slack-only approvals with SMS alerts

**Alpha.7, 2026-09-12: hosted preflight, planner bytes and document review verified; live approval/alert proof pending.**
Slack holds the canonical review and owner decision. SMS is an attention notice
and link only, with no approval command or SMS decision authority. The candidate
adds optional `approval_mode="slack_only"` and requires
`slack_approval.workspace_url`; omitted mode preserves legacy profiles/history.
Read [configuration](configuration.md) before preparing a new package.

## Frozen review and delivery order

1. Freeze and review the synthetic planning-only package. The candidate displays
   the complete `owner-summary.md` and `acceptance.md` as inert Slack text. Their
   combined text, including separators, must be at most 24,000 UTF-8 bytes;
   unsupported input is rejected before issuing a challenge. A supporting private
   artifact link remains available, but the owner must not need that login to
   review the displayed details. Verify the actual copy and rendering.
2. Finish the candidate checks, independent review and live-use preparation.
   Publish and independently verify [the public checkpoint](approval-checkpoints.md)
   before requesting the owner decision. Bind its commit to the exact private
   package. Post and verify the Slack card before preparing its SMS alert.
3. Operator preparation resolves the provider permalink, and the separate
   `SmsAlertOutbox` verifies its binding to the exact posted card and configured
   workspace. Its fixed SMS body is
   `{label}: An approval in Slack needs your attention. {permalink}`.
   Expiry and decision guidance stay in Slack. The text contains no approval
   command; callers cannot choose an arbitrary message body, recipient or URL.
4. Sending checks current eligibility under the reservation locks, suppresses a
   resolved or otherwise ineligible alert, and records one permanent attempt
   before the provider POST. A duplicate call, process restart or unknown outcome
   cannot authorize another send. Reconcile the original selected outbound message.
5. The owner decides in Slack. Validate the original event and current owner/package
   authority, record one durable decision, and update that same card to its terminal
   state without decision controls. Delivery does not prove that decision. An SMS
   already authorized for dispatch may still arrive after the decision and cannot
   necessarily be retracted; its link must show the card's current state.

## Private operator interface

These candidate command shapes are not public installation instructions. The
package and trusted private environment must already exist. Identifiers below
are placeholders; credentials never belong in command arguments or public records.

| Command | Required arguments | Purpose |
| --- | --- | --- |
| `python -m company_improvements.alert_cli prepare` | `--project PROJECT_KEY --card-id CARD_ID` | Verify a posted card/permalink and prepare its notification ledger |
| `python -m company_improvements.alert_cli send-once` | `--project PROJECT_KEY --operation-id OPERATION_ID` | Reserve and attempt the fixed notification once |
| `python -m company_improvements.alert_cli status` | `--project PROJECT_KEY --operation-id OPERATION_ID` | Read bounded operation status |
| `python -m company_improvements.alert_cli reconcile` | `--project PROJECT_KEY --operation-id OPERATION_ID --message-sid OUTBOUND_MESSAGE_SID` | Verify the selected original provider message without resending |

There is no scheduler, new HTTP gateway or new bot automation for these commands.
The legacy SMS approval gateway is a separate capability; SMS preparation/ingestion
must not authorize decisions in a Slack-only profile. Existing unrelated handlers
and history remain intact. No RCS setup, public runtime or installer is supplied.

## Remaining verification and result

Exact-text copy and permalink-response repairs passed source checks and independent
review. The full host suite passed 1,445 tests with one skipped and three deprecation
warnings against disposable PostgreSQL and synthetic transports. Isolated runtime
wheel installation, dependency checks and 25-file source parity passed on macOS
Python 3.14.6; a full installed-package test suite was not run. Hosted preflight
verified source, configuration and schema, and five genuine GPT-6 planning files
matched their hosted bytes. The original Grok CLI document review was accepted
after supplemental evidence verification and normal API recording. Alert delivery
and the actual owner decision remain pending. See [status](../../../docs/status.md)
for the reviewed revision and original harness/model-reporting limits. Complete
the public checkpoint before the owner request, then observe alert delivery, the actual owner Slack decision and
same-card closure separately. APPROVE leaves one held issue operation in this
planning-only test; decline/revision produces no new issue operation. A failed
card update leaves the durable decision intact and does not justify a repeat SMS.
Publish the sanitized result after the decision and keep all private evidence in
the checkpoint. No issue execution, build or release follows this synthetic test.

## Prior work and current proof boundary

The earlier paired synthetic Slack card was posted and its matching original SMS
receipt reports delivery. Actual owner decision and SMS-to-Slack terminal closure
remain unverified. The test was cancelled through the normal API after the
direction changed, with its frozen package retained. Cancellation is not owner
approval. The cancelled card and scoped credential cleanup are verified; preserve the
delivery evidence and record cleanup separately from owner approval.

Alpha.5 explored detailed change orders and approval controls inside Messages,
including RCS. That proposal is not selected. Neither an RCS adapter nor working
buttons were proved; hidden reply metadata was not documented in Message GET and
the visible action/code alternative lacked a verifying provider sample. Preserve
[the historical milestone](../../../docs/status.md#2026-09-12--alpha5-message-first-feasibility-historical-not-selected)
without treating its feasibility work or phone settings as app-plan approval.
