# Milestones and known limits

Skill preview: **0.1.0-alpha.6**. Full workflow ready: **no**.
Public results below are maintainer attestations based on restricted records;
private identifiers and raw evidence are not included. They are not yet independent,
publicly reproducible integration tests.

## 2026-09-12 — alpha.6 Slack decisions with SMS alerts

**Selected direction; alert-only delivery is not implemented or live-tested.**
Keep the detailed frozen change order and owner decision in Slack. An ordinary SMS
only calls attention to the verified Slack card and links to it. SMS replies do
not authorize work. The owner should be able to review the proposal in Slack
without a mandatory private repository login.

Post and verify the exact Slack card before sending an alert. The future adapter
must prevent duplicate sends and suppress an alert if the request is already
resolved. A validated owner click records one decision and updates that same card
to its terminal state. An SMS already sent cannot necessarily be retracted.
These are requirements for the selected path, not claims of a completed adapter.

The earlier paired synthetic Slack card was posted and its matching original SMS
receipt reports delivery. Actual owner decision and SMS-to-Slack terminal closure
remain unverified; that proof is incomplete. The paired phone-approval test was
cancelled through the normal API after the workflow direction changed. Its frozen
package is retained. Cancellation is not owner approval; scoped cleanup is verified.

Retirement was checked independently: 19 bounded read-only database checks passed,
with no owner decision or issue operation, preserved delivery/planning/history
records, and accepted cancellation of the same Slack card. A separate Slack read
confirmed its cancelled display without decision controls. The temporary provider
key was revoked, the gateway stopped and stripped of its test credentials, and
both scoped planning grants returned unauthorized after the unchanged-source
coordinator restart. Original Slack access remained available. Local temporary
credential copies were removed. This verifies retirement, not SMS approval.

RCS and in-message phone approval are not selected. No RCS sender registration or
fees setup is being pursued; alpha.5 remains a historical feasibility record.
The new direction requires verified Slack review content, an alert-only adapter,
exclusion of SMS decision authority for the new profile, and a supervised live
acceptance check. No new runtime suite, model evaluation or live alert-only proof is claimed.
Follow [the selected procedure](../skills/company-improvements/references/message-first.md)
and publish/verify the public checkpoint before another owner request. No public
runtime, installer or complete workflow is supplied.

## 2026-09-12 — alpha.5 message-first feasibility (historical, not selected)

**Historical proposal: phone-message approval and RCS are not the selected direction.**

**Paired delivery observed; owner decision and terminal closure unverified.** A
synthetic Slack approval card was posted, and the matching SMS original provider
receipt reports delivery. The current paired proof remains incomplete. These
observations do not establish owner approval or an SMS-to-Slack terminal update.

The owner experience exposed friction in requiring a private repository review
link. A private blob URL cannot be assumed to open directly in the intended mobile app
from Messages or without sign-in. The desired experience is a detailed frozen change order in Messages
followed by Approve/Disapprove; see [the feasibility reference](../skills/company-improvements/references/message-first.md).

| Capability or condition | Evidence or remaining gap |
| --- | --- |
| Paired Slack card and matching SMS | Card posted; original provider receipt reports SMS delivery |
| Actual owner decision and SMS-to-Slack terminal closure | Not verified; current proof incomplete |
| Current SMS interface | Long exact text command plus private plan URL |
| Detailed frozen message body and short decision commands | Not implemented |
| RCS phone business-setting confirmation | Prerequisite only; does not prove sender setup or working buttons |
| RCS adapter and quick-reply evidence | Not implemented; signed webhook evidence or a visible request-code/body path requires review and actual provider evidence; hidden reply metadata is not documented in Message GET |
| Provider registration, terms and fees | Separate setup decisions; not approval of an application plan |
| General automatic fanout or inbound listener | Not implemented/proven |
| Public runtime, installer and full workflow | Not supplied/proven by this documentation milestone |

No new runtime tests or model application tests are claimed for this documentation
update. Earlier executed evidence remains tied to its recorded version and scope.
Before another owner request, publish/verify the updated public checkpoint and
verify the implemented presentation and decision path against the exact private
package. Preserve the current proof honestly; do not treat delivery or setup
consent as its missing owner decision.

## 2026-09-12 — alpha.4 paired-proof preparation (historical snapshot)

**Historical alpha.4 pre-request state; later paired delivery is recorded above.**

**Preparation only: the same-request live proof has not passed or run.** This
public milestone precedes the next owner-facing approval card or text. A fresh
synthetic planning-only request will place the same immutable package/version and
shared challenge on Slack and SMS. The intended observation is a genuine SMS
reply recorded once by the core, followed by the matching Slack card's terminal
update. No issue execution, application change, build or release is in scope.

One actual SMS was sent and delivered following alpha.3. That original SMS request
was subsequently cancelled through the normal API, with its sole challenge
invalidated and zero owner decisions verified by a private database read. It never
had a Slack card; delivery evidence and history remain intact. Cancellation is not
an owner decision or a paired-channel update. The earlier completed Slack proof is a different request;
combining separate successes does not prove the proposed same-request path.

| Boundary | Current evidence or next condition |
| --- | --- |
| Shared challenge, one durable decision and cross-surface race/replay protections | Existing private automated tests; not a claim that this paired live test passed |
| Public checkpoint for the new owner request | Publish and independently verify this snapshot first; bind its commit to the private package/checkpoint |
| Fresh canonical package | Both surfaces in the registry before new intake; real planning, honest review and verified private artifact publication required |
| Paired preparation | Synchronize/restart all receiver replicas; prepare SMS then Slack with the same lifetime and verify the exact shared binding; require accepted Slack posting before SMS send |
| Gateway authority | Retain server-only provider key/database access; bot gets only an expiring one-operation token and SID locators |
| SMS decision | Not yet observed for the fresh paired request; original provider GET and core validation required |
| Slack terminal update after SMS | Not yet observed; verify that exact card reflects the durable outcome and removes decision controls |
| Automatic general fanout or inbound listener | Not implemented/proven; this phase remains supervised |
| Runtime distribution and independent installation | Not included/proven by this public documentation preview |

Use [the paired-proof procedure](../skills/company-improvements/references/sms-approval.md)
without altering prior frozen packages or relabelling the earlier cancelled SMS
request as an owner decision. Preserve its delivery history and the recorded
cancellation/challenge invalidation. Never replay an old message or manufacture
a provider event to make the new proof pass.

If the owner chooses Slack first, preserve that genuine result and identify the
SMS-to-Slack direction as unproven. An update failure also leaves the durable owner
decision intact; reconcile the existing card rather than sending again or reopening
approval. Report which processing/update steps were supervised or automatic.
After the actual decision, publish its sanitized outcome and any remaining gap,
verify the public commit and append it to the private checkpoint.

## 2026-09-12 — alpha.3 gateway pre-dispatch (historical snapshot)

**Historical alpha.3 pre-dispatch state; later delivery is recorded above.** Private
code/reviews were verified; no live SMS send or owner decision was then proved. This
entry describes the state before outbox preparation and the final operation-bound
gateway deployment. Publishing it precedes those actions; it does not claim they
have already occurred.

The existing text-message bot/account/number are retained. A separate trusted
Railway gateway holds the dedicated Restricted Messaging key privately; storage
was authorized and verified, with no local copy. Base database, registry, port and
HTTPS configuration are prepared. The bot receives only an expiring bearer for
one exact prepared operation and selected Message SIDs as locators. No provider
key, database access, caller-authored SMS body, evidence JSON or verdict is delegated.

The [gateway reference](../skills/company-improvements/references/sms-gateway.md)
describes strict status/send/reconcile/ingest boundaries. Original provider GETs
and the core decision ledger establish authority. This is a supervised path, with
no automatic inbound listener or gateway message-list scan.

| Recorded evidence | Result at this milestone |
| --- | --- |
| Frozen private implementation | `b71bac221f7374f70d66d0cac44c4edbd0b09c14` |
| Independent authority/race review | Both findings closed: post-reservation active check and post-lock grant check; factual finish remains permitted for already-attempted sends |
| Independent real-PostgreSQL reproductions | Passed for the repaired findings |
| Focused host tests | 593 passed, zero skipped |
| Installed full suite | 1,286 passed, one optional local Codex help check skipped, three deprecation warnings; 59.00 seconds |
| Installed runtime/SQL parity | 21 files byte-equal to reviewed source |
| Test environment | Disposable PostgreSQL and synthetic provider transport; no live provider proof |
| Documentation application | Two manual scenarios by the draft's author; no fresh evaluator/model run; see skill validation |

These are evidence for the stated private code, not runtime delivered by this
public preview. Final public structure/privacy checks are tracked separately in
[skill validation](skill-validation.md).

The following are expected next conditions, not missing prerequisites to publish
this pre-dispatch snapshot: prepare the fresh reviewed outbox, configure the exact
operation/version/package/registry/expiry binding, deploy and verify that binding,
then run the separate SMS proof. Provider creation, handset delivery and the actual
owner decision must each be observed and recorded honestly. No send occurs merely
because a key is configured or a liveness endpoint responds.

Before requesting the decision, verify the public snapshot and record its commit
with the exact private package, operation and live-use checks in the private
checkpoint. After the real decision, publish only its sanitized outcome and gaps,
verify that commit and append it privately. The previous Slack package/decision
and held operation remain unchanged. Public synchronization is an operator procedure.

## 2026-09-12 — alpha.2 selected-original preparation (historical snapshot)

**Historical alpha.2 state; not a current credential/deployment inventory.** No
SMS was sent in that milestone; the previous live test exercised Slack only.
The existing SMS bot has no configured adapter to the approval coordinator.
A separate test requires live account/sender binding, a dedicated trusted operator,
a new reviewed planning-only package and a genuine SMS reply.

The [SMS runbook](../skills/company-improvements/references/sms-approval.md) separates
provider creation, handset delivery and owner approval. It uses a selected original
inbound Message SID to avoid the older shared-sender list scan. That path requires
its tested private implementation; it is not an automatic inbound listener or a
runtime shipped in this preview. The combined private source suite passed 1,138
tests against disposable PostgreSQL and synthetic provider responses; one optional
local CLI help check was skipped. Independent reader review found no blockers.
The send operator also preserves known failed/undelivered creation receipts without
a second send. These changes are committed but not deployed for a live SMS test.
No SMS credentials, new package, handset delivery or owner decision are claimed.

## 2026-09-12 — planning and Slack owner approval

**Passed:** supervised synthetic planning-only approval. This entry is a
retrospective backfill, published after the owner's decision.

- A real GPT-6 run produced five immutable planning files; hosted copies matched.
  Native Grok reviewed the exact revised package and accepted. Review transport was
  operator-assisted.
- The owner clicked Approve then Approve plan in Slack. The receiver recorded one
  matching owner decision and callback for the exact package. Request state became
  approved_waiting_issues with exactly one issues_pending operation still held.
- Thirteen final read-only checks passed. Slack's terminal update succeeded on its
  first attempt and removed decision controls. Temporary operator SSH access was
  revoked and task key files removed.
- The installed full suite passed 1,027 tests before a later five-line card-link
  change. The final change passed 165 focused source and installed-package tests;
  the full suite was not rerun afterward. Twenty installed runtime source files
  matched reviewed receiver source.

These counts do not certify other organizations or this public documentation
package. [Skill validation](skill-validation.md) is recorded separately.

| Capability | Evidence or remaining gap |
| --- | --- |
| Skill publication at approval stages | Instructions/template/progress included; operator-enforced |
| Automatic publication/runtime checkpoint enforcement | Not implemented |
| Unattended intake/interview/review | Supervised path proven; complete unattended handoff not proven |
| Earlier paired Slack/SMS proof | Matching card posted and original SMS receipt delivered; actual owner decision and SMS-to-Slack terminal closure unverified |
| Selected Slack decision + SMS alert path | Alert-only adapter not implemented/live-tested; detailed Slack review and duplicate/resolved suppression require verification |
| Web or Grok owner approval | Not proven; model conversation is not authority |
| Linear issue creation | Not implemented in coordinator |
| Ringer application builds after issues | Not implemented in coordinator; planning invocation is insufficient |
| Independent application review and GitHub/Railway release | Complete automated path not proven |
| Public runtime and installer | Not included |
| Fresh install, second organization, upgrade/recovery | Not run |
| Stable release | Not ready |

Next: implement and verify detailed Slack review with an alert-only SMS adapter,
including duplicate suppression and same-card closure. Preserve the verified
retirement of the cancelled paired test. Publish/verify the next
checkpoint before another owner request. Later implement the approved-package-to-
Linear handoff and bounded Ringer build dispatch. Do not repurpose synthetic held
operations as real app-change authorization.
