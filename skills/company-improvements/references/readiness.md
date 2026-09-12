# Installation and stable-release readiness

Current public package: skill/documentation preview 0.1.0-alpha.4. The separate
private implementation has a planning coordinator and signed Slack approval
receiver, with a supervised synthetic owner proof passed. Runtime/adapters are not
shipped in this preview. Installer: missing. Independent clean installation and
full live end-to-end acceptance: not run. The bounded SMS gateway has completed
private repair, review and executed tests. This pre-approval milestone does not
prove the next paired operation's binding/deployment or an owner SMS decision.
One earlier SMS was delivered; its SMS-only request was subsequently cancelled
without an owner decision, with its delivery history preserved.
The fresh same-request SMS decision/Slack terminal-update proof remains pending.
Publish and verify its public snapshot before either owner-facing request. General
automatic fanout/listening and independent installation remain unproved.
No stable release exists.

Read [status](../../../docs/status.md), [compatibility](../../../compatibility.json)
and [approval checkpoints](approval-checkpoints.md). Publication is currently an
operator requirement, not a coordinator runtime gate. Instructions cannot provide
missing runtime, credentials or authority. The proven planning-only approval leaves
issue creation held.

The future readiness command must report each component separately and exit unsuccessfully when a required production gate fails. It must not send messages, create issues or deploy while performing read-only diagnostics. Live proof is a separate explicitly identified operation with documented effects.

## Required before an external stable release

- A tagged source revision includes the implemented skill, runtime, adapters, configuration schema, dependency/version lock and verified installation instructions.
- Dependencies are either redistributable under recorded terms or linked with installation/access requirements. The package does not embed personal copies of private tooling or rely on the creator's logged-in machine.
- A clean supported machine and separate test organization can install using only the release instructions and their own credentials. The evaluator receives no undocumented local state.
- Repeat setup preserves existing configuration and secrets; an interrupted setup can resume or explain the exact recovery step. Upgrade and uninstall behavior are tested and documented, including retained data.
- Negative tests reject wrong-owner, wrong-company, duplicate, expired, cancelled and changed-scope approvals; stale workers, changed candidates and failed reviews cannot release.
- End-to-end testing includes genuine source suggestion, owner reply, real issue creation, isolated build, independent review, release and live behavior verification. Manual substitute steps are disclosed and do not satisfy the automated test.
- Deployment and recovery are proven for each advertised provider/profile. A successful test for one application does not certify another release mechanism.
- Source, release archive/container and full public Git history are checked for credentials, personal identifiers, private records and machine-specific dependencies. The public repository begins from reviewed generic content, not a private working history.
- A versioned compatibility matrix, troubleshooting runbook, known-issues list, changelog, release evidence and maintainer/support route accompany the release.
- No unresolved critical or high-severity defect remains in the advertised scope. Lower-severity known issues and unsupported configurations are documented. A release is described as tested within that scope, never universally bug-free.

Start external testing as a private alpha with a willing friend and their separate accounts. A release candidate follows successful installation and repeated workflow runs, including recovery from an interruption. Publish stable only after the evidence and distribution terms are reviewed. Keep a way to withdraw a bad version and restore the prior supported release.
