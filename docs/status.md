# Milestones and known limits

Skill preview: **0.1.0-alpha.7**. Full workflow ready: **no**.
Public results below are maintainer attestations based on restricted records;
private identifiers and raw evidence are not included. They are not yet independent,
publicly reproducible integration tests.

## 2026-09-12 — alpha.7 Slack approval with SMS reminder passed

**The supervised synthetic test passed.** One ordinary SMS attention reminder was
delivered. The owner confirmed that its link opened the intended Slack card and
approved through Slack. The same message now shows Approved with its decision
controls removed. The recorded decision created one held issue operation; no
issue execution, application change, build or release followed.

The complete frozen plan was readable in Slack. Before/after evidence binds the
single send and actual owner decision to the same request version, package and
message, preserving earlier history. The temporary SMS test key is revoked.
SMS remains notification only; it cannot approve anything.

This proves the supervised reminder-to-Slack approval lane. Native bot intake,
unattended orchestration and the full issue/build/release workflow remain unproven.
The public package remains a documentation skill preview without a runtime or
installer. The prior checkpoint below records the state before this owner decision.

## 2026-09-12 — alpha.7 trusted-context revision, before the next owner request

**Corrected trusted context is deployed and normal revision has created a new
planning version. Genuine GPT-6 planning completed, and all five hosted planning
files match the canonical package. The genuine Grok CLI completed with acceptance
and zero blocking findings. Supplemental verification of the unchanged original
evidence passed, and acceptance is recorded through the normal API.** No new owner card or SMS alert is claimed by this
checkpoint preparation.

A durable constitution must not pin a previous request's event marker as a rule
for later requests. The follow-up uses a new versioned trusted-context snapshot
and policy binding, with only the intended profile's context fields changed.
The correction permits the authorized synthetic retest source and normal revisions;
it does not claim that all request-specific markers were removed from the test
fixture. The marker-free reusable-policy guidance is a general setup recommendation.
All three services were verified against the corrected configuration and the same
reviewed runtime revision `edbecc64bb5a38602cbed40b94fd7229c5ae37c7`, with 25 runtime
files matching. The prior frozen package and its history were captured read-only
and retained; the normal API created the new revision and queued planning.

| New-version gate | Current evidence |
| --- | --- |
| Trusted context/configuration | Versioned correction deployed and verified on all three services |
| Runtime | Same previously tested revision; no new runtime implementation or test count claimed |
| Prior package/history | Retained; never rewritten or treated as the new result |
| Normal revision | New planning version created through the normal API |
| Genuine new planning | Completed; all five hosted artifact bytes match the canonical package |
| New operational review | Accepted with zero blocking findings; original evidence reconciled and acceptance recorded through the normal API |
| New owner card, SMS alert and decision | Pending; earlier approval does not transfer |

The new review's original harness failed because the final-verdict marker was
joined to preceding text instead of appearing at the expected line boundary.
Original output and the failed result are retained. Supplemental verification of
that same evidence passed in a separate deterministic check, with no model rerun
or original harness PASS claimed.
This is separate from the earlier package's teardown-output/model-reporting failure
and its completed supplemental review, preserved below.

See [context configuration](../skills/company-improvements/references/configuration.md#reusable-trusted-context-and-request-revision)
and [revision readiness](../skills/company-improvements/references/readiness.md#check-a-revised-context-before-a-new-owner-request).
The normal API now reports ready for owner approval. Publish and independently
verify this public checkpoint before posting the new card. Keep its commit bound to the exact private version/package. SMS delivery
remains unproven; no previous review or approval can fill that gap. The supervised
planning-only scope still holds all downstream issue execution, builds and releases.

## 2026-09-12 — alpha.7 Slack decision verified; SMS alert still unproven (historical outcome)

**This completed result belongs to the earlier package; the new revision above
has no owner approval.**

**The owner approved the synthetic planning-only package in Slack. No SMS alert
was prepared or sent before that decision.** The complete frozen review content
was verified on the posted card. The original owner action produced one durable
approval, and that same card shows Approved with its decision controls removed.
The request is `approved_waiting_issues` with exactly one held `issues_pending`
operation. This proves the supervised Slack decision and terminal update; it does
not authorize issue execution, an application change, build or release.

Alert preparation exposed a transport defect: `chat.getPermalink` was sent as
POST/JSON and returned `invalid_arguments`. An authenticated read-only GET returned
the expected canonical permalink. The correction uses GET with query parameters
for this lookup alone, preserving the identity, channel, fixed-origin and exact
permalink guards and the existing transport for other Slack methods.

| Current evidence | Result and scope |
| --- | --- |
| Repair revision | `edbecc64bb5a38602cbed40b94fd7229c5ae37c7`, committed and remotely verified |
| Regression demonstration | Three targeted cases failed against the original POST transport before repair |
| Focused checks | 205 passed |
| Fresh full host suite | 1,445 passed, one skipped, three deprecation warnings; disposable PostgreSQL and synthetic transports |
| Fresh package checks | Isolated runtime wheel installation and dependency check passed; 25 Python/SQL files match source, wheel and installed package |
| Installed-test limit | No full installed-package test suite is claimed |
| Repair deployment verification | All three deployed services match the 25 reviewed source files and registry profiles; shared database schema verified |
| Live Slack result | One actual owner approval; same card Approved with controls removed; one issue operation remains held |
| SMS alert result | No alert rows and no send; pending-request reminder delivery remains unvalidated |

The operator observed that the request was resolved and did not dispatch an alert.
This does not demonstrate automatic live SMS suppression. A pending-only preflight
correctly rejected the resolved state; it was not a runtime-source verification
failure.

This is a **post-decision** snapshot. Preserve the original verified pre-card
publication receipt and frozen package; this later outcome must not be represented
as preceding the card. The original Grok review harness failure and accepted
supplemental verification remain distinct, as recorded in the historical checkpoint
below. The transport repair does not create a new model review or approval.

Publish and verify this outcome before a fresh synthetic pending-card test. That
separate test must have its own exact package and completed public checkpoint,
verified Slack review/card, current eligibility and one permitted SMS attempt.
Do not send a reminder for the already approved request. Actual SMS delivery and
the subsequent owner decision must be verified separately. No automatic listener,
scheduler, public runtime, installer or full-workflow pass is claimed.

## 2026-09-12 — alpha.7 pre-card checkpoint (historical snapshot)

**This earlier checkpoint preceded the card; the later repair and actual Slack
decision are recorded above. Pending statements below describe that earlier state.**

**Source/package checks, hosted preflight, genuine planner bytes and exact-package
document review verified; the new live approval/alert test remains pending.** This is a pre-approval milestone for a supervised synthetic planning-only
test. The owner reviews the full frozen owner-summary and acceptance details in
Slack without a mandatory private repository login. SMS only draws attention to
the accepted card through its verified permalink and carries no decision command.

| Candidate interface | Scope and verification boundary |
| --- | --- |
| Optional `approval_mode="slack_only"` | Requires `slack_approval.workspace_url`; legacy profiles and history are preserved |
| Complete inert Slack review | Combined owner-summary/acceptance text limited to 24,000 UTF-8 bytes including separators; unsupported input rejected before challenge issuance |
| Separate `SmsAlertOutbox` | Notification ledger distinct from legacy SMS approval delivery |
| Operator-only `alert_cli` | Prepare, send-once, status and reconcile; no scheduler, new HTTP gateway or bot automation |
| Alert delivery | Short label, attention notice and verified card permalink; current eligibility checked at reservation, one permanent attempt, resolved suppression and no retry after uncertainty |
| Owner authority | Slack-only for the selected profile; SMS commands/replies do not decide |
| Reviewed implementation | Private committed revision `1fc3423e895998b7d16d99573ba9e00eaff27b15`; remote source publication verified |
| Full host regression | 1,445 passed, one skipped, three deprecation warnings; 62.96 seconds |
| Test environment | Real disposable PostgreSQL and synthetic provider transports; no live-provider evidence |
| Independent reviews | Source review and explicit 18-file public privacy review found no blockers; maintainer diff review complete |
| Isolated runtime wheel | Installation and dependency check passed on macOS Python 3.14.6; 25 Python/SQL files byte-identical across source, wheel and installed package |
| Installed test limit | Runtime-only dependencies checked; the full installed-package test suite was not run |
| Hosted preflight | Deployed source matches the 25 reviewed Python/SQL files; registry bindings and schema through migration 005 verified |
| Fresh planning package | Genuine GPT-6 produced five planning files; successful hosted reads matched the exact artifact bytes |
| Exact-package operational review | Accepted document-only Grok CLI review of the same five frozen planning documents, with zero findings; independent supplemental verification passed and the normal API recorded acceptance. Configured model 4.6, observed reported model 4.6-build |
| Remaining live acceptance | SMS alert delivery, actual owner decision and same-card terminal closure remain pending; native bot transport is not proved by this review |

The executed source checks include the repaired exact-copy and permalink-response
guards. These results do not prove live provider delivery or owner approval.
The original review harness failed on teardown-output parsing and a configured/
reported model-name mismatch. The Grok CLI itself completed with acceptance.
Independent supplemental verification checked the exact original evidence without
rerunning the model; the original harness result remains failed. Acceptance was
recorded through the normal API. This document-only review proves neither native
bot transport nor owner approval. No SMS alert has been sent for this test. Publish and independently verify the public snapshot,
then bind its commit
to the exact private package and live-use checkpoint. Post/verify the Slack card
before preparing/sending the SMS alert. Verify delivery, the actual Slack decision
and terminal closure separately. An already dispatched text may still arrive after
the decision; its link must show the same card's current state.

This candidate does not ship a public runtime/installer or prove the full workflow.
RCS is not selected. Earlier observed results and retirement evidence remain tied
to their historical milestones. See [the candidate runbook](../skills/company-improvements/references/message-first.md).

## 2026-09-12 — alpha.6 selected direction (historical snapshot)

**Historical alpha.6 direction and retirement evidence; candidate progress is recorded above.**

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
| Selected Slack-only candidate + SMS alerts | Exact frozen Slack review, actual owner approval and same-card terminal closure verified; one issue operation held; SMS alert delivery remains unproven |
| Web or Grok owner approval | Not proven; model conversation is not authority |
| Linear issue creation | Not implemented in coordinator |
| Ringer application builds after issues | Not implemented in coordinator; planning invocation is insufficient |
| Independent application review and GitHub/Railway release | Complete automated path not proven |
| Public runtime and installer | Not included |
| Fresh install, second organization, upgrade/recovery | Not run |
| Stable release | Not ready |

Next: complete supplemental verification of the original review evidence and
record the actual verdict for the revised package, then verify its public/private
checkpoint before the fresh owner card. Verify the card before one eligible SMS
attempt and verify delivery separately. No issue execution, build or release
follows either synthetic planning-only test.
