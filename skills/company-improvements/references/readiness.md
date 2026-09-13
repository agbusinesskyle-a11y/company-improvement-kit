# Installation and stable-release readiness

Current public package: skill/documentation preview 0.1.0-alpha.6. The selected
path is [Slack review and decisions with SMS alerts](message-first.md). The owner
reviews the detailed frozen proposal in Slack without mandatory private repository
login. An SMS links to that card and has no approval authority. The alert-only
adapter is not implemented or live-tested. Verify Slack content, card-before-text
ordering, duplicate/resolved suppression and same-card closure before claiming it
works. RCS sender/fees setup is not being pursued.

A separate earlier supervised planning/Slack owner proof passed. A later paired
card was posted and its matching SMS receipt reports delivery, but the actual
owner decision and SMS-to-Slack terminal closure are unverified. That proof remains
incomplete. The test was cancelled through the normal API with its frozen package
retained; cancellation is not approval and scoped cleanup is verified.
Runtime/adapters and an installer are not shipped. Independent clean installation and full live acceptance
have not run. No stable release exists.

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
