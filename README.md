# Company Improvement Kit

**0.1.0-alpha.5 — public skill and documentation preview.** The complete automation
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

The paired synthetic proof posted a Slack card and delivered its matching SMS,
verified through the original provider receipt. The actual owner decision and
SMS-to-Slack terminal update remain unverified; the proof is incomplete.
[Message-first approval](skills/company-improvements/references/message-first.md)
records the desired next experience: a detailed frozen change order in Messages
with Approve/Disapprove. The current SMS instead uses a private plan URL and long
exact reply command. Private repository links cannot be assumed to open directly in the intended mobile app from Messages
or without sign-in. No detailed message renderer, short-command support or RCS
adapter is implemented. General automatic fanout, inbound listening and an
installable public runtime remain unavailable.

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
