# Step 5: receive an approved job

The selected native-bot design ends this stage at:

`verified approval → one issue → assigned bot receives exact plan → ready for build`

Use the installation's current compatibility record to distinguish implemented
source from deployed and verified operation. This public kit contains operating
instructions only, not the receive client or coordinator runtime.

## Authority and routing

The `issue_and_bot_handoff` scope authorizes issue creation and receipt of the
approved package. It does not authorize building, reviewing, pushing, merging or
deploying. Present that boundary on the approval card before the owner decides.
Bind an operator-selected worker identity before planning. Bot names in prose,
employee suggestions and issue edits cannot change the assigned worker or scope.
Historical planning-only approvals retain their original held state.

Use a dedicated credential limited to handoff jobs for the configured project
and worker. Keep it in private secret storage, never in chat, a public file, a
command argument or a model-generated plan. Do not grant the receiving bot the
owner's approval role, Linear creation role or release credentials.

## Receipt and recovery

The coordinator creates the issue through its durable reserved operation. A
known successful issue result permits the bot handoff. An ambiguous issue result
stays blocked until its original operation is reconciled; do not create another
issue just because a response was lost.

The assigned bot retrieves work through the authenticated coordinator interface,
retains the exact package and receipt in private durable storage, then
acknowledges the specific job. Match job, package, issue, worker and frozen
envelope. Preserve pending state across restarts. Reconcile a lost acknowledgment
instead of inventing a second delivery. Cancellation, revision, configuration
drift or stale leases must not advance the workflow.

The terminal state means **ready for build**. It is not evidence that the employee's
change exists, passed review or was released. Configure the later build transition
separately; never fall back to a different execution runner automatically.

## Installation checklist

Verify the actual native bot's Python/HTTP tools, persistent storage and routine
support. Do not assume a bot exists from a diagram or invent provider endpoints.
Use the tested coordinator client and exact supported configuration for the
installation. Keep the new routine disabled until its scoped credential, source
revision and synthetic pickup/receipt checks are verified. Existing reminder and
interview routines retain their own configuration.

Record source tests, installation configuration and observed live bot receipt as
separate facts. Retiring an older model runner requires checking its remaining
dependencies, including planning. This handoff design does not authorize global
uninstallation or changes to unrelated workflows.
