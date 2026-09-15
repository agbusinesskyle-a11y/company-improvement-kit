# Phase 6: a checked draft

This milestone adds a private source implementation, not a public runtime or
installer. Read [status](../../../docs/status.md) and [compatibility](../../../compatibility.json)
for source, native integration and hosted activation evidence.

A new `issue_handoff_build` approval permits one issue, exact bot handoff, and one
isolated draft build. The earlier `issue_and_bot_handoff` scope still ends before
building. Never reuse a planning-only or handoff-only decision as build permission.

Before planning, freeze the repository/base, allowed paths, check argv, local Docker
image ID, requested/reported model IDs, handoff/build workers and limits. Use separate
handoff and build credentials. Keep deployment credentials away from the builder.
Follow the [publication checkpoint](approval-checkpoints.md) for the new exact package.

The native bot invokes the disabled-by-default private build client on a verified
host with Python, Git, authenticated Grok and Docker. The implementation reference
is `docs/phase6-native-build.md` in the private source. The worker copies existing
Grok authentication into an ephemeral private home; it imports no user plugins,
hooks or MCP configuration, disables tools/delegation, and runs one headless turn.
There is no Ringer or API-key fallback. Verify both requested and reported model
identities; do not silently accept a replacement model.

The model returns file changes as data. The trusted client validates scope and
limits, creates a separate local candidate commit, exports committed bytes, and
executes the configured checks in a pinned Docker image with no network or host
credentials. Missing isolation stops before a model call. The image and build-state
mount must already work on the selected host. A bot's ability to use a shell is
not evidence that its own cloud computer has suitable isolation.

Retain the exact envelope, dispatch marker, proposal, model/session/usage receipt,
Git candidate, check output and final receipt. A restart recovers original evidence;
it never blindly invokes the model again. Cancellation, expiry, policy drift,
failed checks and conflicting evidence prevent readiness. One successful build
ends at `ready_for_review`. It does not run review, repair, push, PR creation, merge,
preview or deployment. Those later stages require their own implementation/scope.

The initial supported unit is small: 32 text-file changes, 1 MiB proposal and source
context, and bounded model/check time. Binary edits, symlinks, submodules, no-op
results and unsupported/oversized trees are refused. Output-token limits are checked
from returned usage and are not a prepaid spending guarantee. Split larger changes
into smaller newly approved packages. Checks passing does not prove functional
completeness or independent approval.

Public source tests, native model integration, client installation and a live hosted
employee-request chain are separate evidence. No scheduled routine, Linear status
sync, Slack readiness message or cross-host candidate transfer is supplied in this
slice. Same-user processes are not isolated by private directory permissions.
