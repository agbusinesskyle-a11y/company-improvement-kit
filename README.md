# Company Improvement Kit

**0.1.0-alpha.15 — public skill and documentation preview.** The complete automation
is under development. This release contains no coordinator runtime or installer.
It does not enable Slack, create issues, launch builders or deploy applications.

The intended process is: suggestion → interview → versioned plan → owner approval
→ issues → isolated build → independent review → verified release.

The current native-bot milestone is [step 5](skills/company-improvements/references/bot-handoff.md):
approved package → one issue → assigned bot receipt → ready for build. That narrow
scope stops before the later build, review and delivery stages.

Start with [the skill](skills/company-improvements/SKILL.md), [current status](docs/status.md)
and [the roadmap](docs/distribution.md). Give the skill folder to a compatible agent
to assess an installation or follow the documented process. Reading or installing
it supplies instructions only. No automated installation command or independent
clean install is available yet. Each organization needs its own accounts.

## Updated throughout development

At every approval stage, maintainers update the skill, relevant references, status,
compatibility manifest and changelog. They publish and verify a GitHub snapshot
**before requesting the owner's decision**, then record its commit beside the
private approval package. After the decision they publish its generic outcome and
remaining gaps. See [approval checkpoints](skills/company-improvements/references/approval-checkpoints.md).
This is an operator procedure today; automatic publication/runtime enforcement is
future work.

A private supervised test passed real planning, operational review and human Slack
approval, ending with issue creation held. It did not prove the later stages or
installation for another organization. [Status](docs/status.md) records that scope;
raw private records are not included.

The [Slack-only approval and SMS alert candidate](skills/company-improvements/references/message-first.md)
has passed source/database tests and independent review. It displays the frozen
owner summary and acceptance details in Slack without requiring a private
repository login. A separate operator-only SMS outbox sends a short attention
notice and the verified Slack permalink; SMS carries no decision command or
authority. Existing profiles and history are preserved.

The supervised test delivered an SMS reminder, its link opened the intended Slack
card, and the owner approved there. The same card updated and its decision controls
were removed; one issue operation remains held. Temporary test access was revoked.
See [current status](docs/status.md) for evidence and limits. Permanent notification
operation remains disabled pending its separate setup. A private execution
candidate passed connected synthetic checks; it has not been activated or proven live.

Private development includes [durable Slack suggestion intake](skills/company-improvements/references/slack-intake.md)
and a reusable [post-approval execution process](skills/company-improvements/references/execution.md).
The execution candidate applies only to newly scoped requests; existing planning-only
approvals stay held. See status for each component’s actual verification and activation. This does not make the public preview an executable installation.
No scheduler, new HTTP gateway, bot automation, RCS setup, public runtime or installer
is included. Earlier proof and retirement results remain historical.

## Contents and reuse

- [Operating skill](skills/company-improvements/SKILL.md) and essential references.
- [Checkpoint template](templates/approval-checkpoint.json), filled only in private storage.
- [Compatibility manifest](compatibility.json) and [changelog](CHANGELOG.md).
- [Distribution roadmap](docs/distribution.md) and [external requirements](docs/third-party.md).
- [MIT license](LICENSE) for the authored content shipped here.

The target uses Slack, Grok, GPT-6, Spec Kit-style artifacts, Linear, Ringer, GitHub
and Railway. Full Spec Kit command integration is not established by the existing
five-document planning proof. A generic role mapping does not imply support for
every provider or model.

Public history starts from reviewed generic content. Company plans, identities,
credentials and approval evidence stay in each installation's private storage.
Open a repository issue for reusable questions or suggestions without private data.
There is no stable release or support SLA yet. Tests establish a scope, not zero bugs.
