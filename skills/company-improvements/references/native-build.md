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
employee-request chain are separate evidence. The public export does not supply
a scheduled routine, Linear status sync, Slack readiness message or cross-host
candidate transfer. The originating private installation uses the execution-host
background pickup described below. Same-user processes are not isolated by private
directory permissions.


## Activate one installation

Keep each existing registry entry and approval scope unchanged. Add a separately
bound fixture when testing a different repository; never rewrite a historical
project to gain new build authority. Publish the compatible coordinator and owner
receiver together, retain ordinary migration/startup commands, verify installed
source and health, and provision distinct project/kind/worker grants.

The native routine should call a trusted local wrapper with credential file paths,
never credential values in its prompt. One cycle may run issue, handoff and build
pickups in sequence under a process lock. Require the issue provider credential
before claiming work. Keep each stage's environment separate, retain pending state,
and stop on blocked or uncertain outcomes. Use the bot's supported schedule only
after one configured pickup succeeds; an empty queue is access evidence only.

Prepare a fresh exact plan and perform the public checkpoint before its real owner
card. Verify the resulting issue, handoff, model call, candidate and check receipts
through `ready_for_review`. Report source deployment, configured credentials, enabled
routine and completed live chain as separate facts. The originating installation
verified an owner-approved fixture through issue, handoff and a checked recovery
to `ready_for_review`. Its host service supplies pickup because the native app
timer did not dispatch reliably.
Public distribution remains documentation only.


An operator activation fixture is not an employee request and should be labeled
as such. Retain its actual provider source identity and ordinary planner/reviewer
evidence. A planner context reference must resolve to a real read-only document
in the configured checkout before dispatch. Freeze any correction before request
creation; never change a package to make an existing approval fit. Keep prior
profile entries byte-equivalent when adding the fixture.

The review API treats every `findings` entry as blocking. For a real accepted plan
with no blockers, submit `verdict: accept` and `findings: []`; keep informational
observations and reviewer identity in separate private evidence. Do not turn
nonblocking notes into requested changes. An incorrect recorded review follows
the normal revision path; retain its history and never edit frozen plan bytes.


## Separately authorized recovery

Do not replay a failed model effect or clear its evidence. Retain and verify the
coordinator's exact terminal receipt before acknowledging a stopped worker journal.
A retry needs a separate owner instruction. The privileged operator verifies that
instruction, retains it privately, and supplies its digest with the exact current
request/version/package and failed job/result to `native_recovery`. This CLI uses
operator runtime access; no employee, builder, or ordinary intake API exposes it.

The recovery ledger rejects cancelled/drifted requests, uncertain effects, active
work, mismatched owners/packages/results, reused failure authorizations and attempts
above the frozen ceiling. It creates one new build linked to the accepted handoff,
without creating another issue, altering old results, or expanding scope. Retain
the public checkpoint before dispatch. Authorization evidence is not public.

Native CLI output is retained privately by session before parsing/validation.
Credential copies still use a temporary home and are removed afterward; commands,
authentication files and environment are not copied into response evidence.
Historical planning language is not a new instruction to the approved builder.


## Execution-host background pickup

If the native app timer does not dispatch reliably, the same trusted worker command
can run under the execution host's service manager. This changes the timer, not
model selection, approval authority, credential scope or receipt handling. Record
that distinction. On macOS, a per-user LaunchAgent can use `ProgramArguments` for
the exact private venv Python, trusted pickup script and enable flag, `RunAtLoad`,
and `StartInterval: 300`. Put stdout/stderr in restricted operator storage. Never
put credentials or shell-interpolated commands in the service definition.

Verify both the automatic startup and a later timed cycle. Reuse the existing
process lock and durable stage journals; never introduce a second unguarded worker.
Disable the redundant native app timer when its UI is available. A screen lock
does not stop this background process, but host sleep, logout or shutdown affects
availability. The model remains the authenticated native Grok CLI.
