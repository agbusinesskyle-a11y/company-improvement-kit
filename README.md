# Company Improvement Kit

**0.1.0-alpha.4 — public skill and documentation preview.** The complete automation
is under development. This release contains no coordinator runtime or installer.
It does not enable Slack, create issues, launch builders or deploy applications.

The intended process is: suggestion → interview → versioned plan → owner approval
→ issues → isolated build → independent review → verified release.

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

The [SMS gateway reference](skills/company-improvements/references/sms-gateway.md)
keeps provider credentials on a separate trusted server and limits an existing bot
to one prepared operation. One supervised SMS was sent and delivered after alpha.3;
that request was cancelled without an owner decision and never had a Slack card.
Its delivery history is preserved. The next milestone prepares
a fresh request shared by Slack and SMS, to observe a genuine SMS decision and the
matching Slack card's terminal update. That paired live proof has not run. Existing
shared-decision protections have private automated tests; general automatic fanout,
inbound listening and an installable public runtime remain unavailable.

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
