# Milestones and known limits

Skill preview: **0.1.0-alpha.2**. Full workflow ready: **no**.
Public results below are maintainer attestations based on restricted records;
private identifiers and raw evidence are not included. They are not yet independent,
publicly reproducible integration tests.

## 2026-09-12 — separate SMS proof preparation

**Not sent; live approval test pending.** The previous test exercised Slack only.
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
| SMS | Private adapter groundwork; no live SMS test in this proof |
| Web or Grok owner approval | Not proven; model conversation is not authority |
| Linear issue creation | Not implemented in coordinator |
| Ringer application builds after issues | Not implemented in coordinator; planning invocation is insufficient |
| Independent application review and GitHub/Railway release | Complete automated path not proven |
| Public runtime and installer | Not included |
| Fresh install, second organization, upgrade/recovery | Not run |
| Stable release | Not ready |

Next: configure and run the separate supervised SMS approval proof, then implement
the approved-package-to-Linear handoff and bounded Ringer build dispatch.
Do not repurpose the synthetic held operation as real app-change authorization.
