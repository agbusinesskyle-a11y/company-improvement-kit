# Native build outcome messages

The private Phase 5/6 status worker connects verified outcomes to the originating
Slack thread, exact owner approval thread and existing Linear issue comment.
The original approval card remains unchanged. Comments communicate status; they
do not change Linear workflow state or authorize review, repair, merge or release.

Enable this worker only for explicitly configured projects on the integrated
Slack host. Keep its Slack and restricted issue-provider credentials in private
runtime configuration. Verify app membership and thread-history access in both
channels and access to the frozen issue/team. Disabled is the default. The public
skill export supplies instructions, not this runtime or an installation command.

The durable ledger derives targets and message facts from current execution
records and the exact approval card, never model prose. It ignores historical
results with later queued work and supersedes stale unsent messages. Source,
owner and issue delivery are tracked separately. One failed destination does not
block another or change build state. Invalid targets have their own persistent
error records. A dead enabled delivery worker fails host readiness; unresolved
provider receipts remain visible as attention without disabling approval callbacks.

Each operation reserves one send permanently. Provider uncertainty triggers
read-only recovery by its original operation identity, checking exact destination,
author and body. A restart never grants another post or build. Unresolved delivery
remains visible in health counts for operator attention. Bounded thread reads may
leave old or inaccessible evidence unresolved; never erase the reservation to
force a retry. A later build result receives its own distinct message.

Report ready-for-build, ready-for-review, failure and uncertainty accurately.
A checked draft is not independently reviewed or released. Before activation,
publish and verify the generic snapshot, then bind it to the exact private test
package. Verify the actual provider messages and ledger receipts, followed by
idle discovery, without repeating completed model/build tests. See
[current status](../../../docs/status.md) for the observed activation result.
