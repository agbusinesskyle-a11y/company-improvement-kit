# Milestones and known limits

Skill preview: **0.1.0-alpha.3**. Full workflow ready: **no**.
Public results below are maintainer attestations based on restricted records;
private identifiers and raw evidence are not included. They are not yet independent,
publicly reproducible integration tests.

## 2026-09-12 — bounded SMS gateway, pre-dispatch snapshot

**Private code/reviews verified; no live SMS send or owner decision proved.** This
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
| SMS | Private gateway code/review/tests verified; exact operation binding/deployment and live SMS proof follow this pre-dispatch snapshot |
| Web or Grok owner approval | Not proven; model conversation is not authority |
| Linear issue creation | Not implemented in coordinator |
| Ringer application builds after issues | Not implemented in coordinator; planning invocation is insufficient |
| Independent application review and GitHub/Railway release | Complete automated path not proven |
| Public runtime and installer | Not included |
| Fresh install, second organization, upgrade/recovery | Not run |
| Stable release | Not ready |

Next: publish/verify this pre-dispatch snapshot, prepare the reviewed outbox,
complete exact binding/deployment checks and run the separate supervised SMS proof.
Later implement
the approved-package-to-Linear handoff and bounded Ringer build dispatch.
Do not repurpose the synthetic held operation as real app-change authorization.
