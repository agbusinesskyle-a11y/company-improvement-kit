# Reminders and discovery after planning approval

The current private installation has verified coordinator and integrated Slack code,
normal migrations and execution-host source parity. Both active intake lanes have
running attention workers. Existing approved packages and discovery history remain
unchanged; unresolved findings still block successor planning. A read-only provider
credential check and idle worker health establish connection, not a new SMS delivery
or completed business build. The public kit is documentation only.

## Resume the existing reminder path

The integrated host can explicitly enable `COMPANY_IMPROVEMENTS_REMINDERS=enabled`.
Absent or `disabled` leaves the worker off. Configure the existing Slack identity
and `TWILIO_ACCOUNT_SID`, `TWILIO_API_KEY_SID`, `TWILIO_API_KEY_SECRET` through the
installation's approved secret store or deployment-platform secret variables.
The runtime reads environment variables and does not depend on an external password
manager. Use the installation's authorized credential storage; an empty variable
does not establish access to a persistent key. The credential account must match
the selected delivery binding. Do not reuse revoked test credentials or alter the
registry digest merely to enable the worker. The host uses its intake project; other
profiles are not swept automatically.

For the separate routing path, `COMPANY_IMPROVEMENTS_SMS_ATTENTION_JSON` supplies the
separate private delivery binding. It is bounded, duplicate-free JSON with exactly
`schema_version` (1), `project`, `registry_digest`, `owner_id`, `twilio_account_sid`,
`sms_sender` and `owner_phone`. Its project, full registry digest and owner must
match the current Slack-only planning profile. The SMS account, sender and owner
destination must be verified for the installation. Do not publish filled values.

For multiple active lanes, schema version 2 accepts exactly `schema_version` and
`projects`, a list of 1–32 complete version 1 entries described above. The document
must be smaller than 32,768 UTF-8 bytes. Validate every entry, reject duplicate
projects, and require the requested lane to be present. Each entry retains its
version 1 binding hash. The host creates and owns a reminder worker for each intake
lane; shared owner decision and completion workers remain shared.

Native release cards use a separate immutable release SMS ledger with additive SQL
025. Preparation binds the exact posted release card, challenge, owner and checkpoint.
The existing worker fairly services both plan and release outboxes with the same
provider clients and permanent send reservation rules. Operator prepare/status/send/
reconcile commands select release cards explicitly with `--release`; process-once
handles both. A signed release REVISE may create fresh planning only while the exact
release remains held and has no effect attempt. Preserve its candidate and decision;
the successor requires fresh owner build approval.

Absent routing retains the legacy registry-derived path. Malformed or mismatched
routing fails closed rather than falling back. Disabled hosted reminders return
before parsing routing or reading provider credentials. Once enabled, preparation
and dispatch validate the binding and freeze the actual account/addresses plus a
`delivery_binding_hash` in each new routed alert. A changed binding cannot silently
retarget a prepared alert. Historical status and reconciliation use its original
stored delivery envelope.

Additive SQL 010 adds the immutable binding hash through the normal coordinator
migration command; existing rows retain their legacy null hash. Upgrade every
reminder dispatcher, including hosted workers and operator CLIs, before enabling
separate routing. Do not mix old dispatchers with new bound alerts or roll back to
dispatchers that do not understand the binding. Preserve normal service lifecycle
commands and existing pending/attempt history.

If a new restricted provider key is needed, obtain explicit authorization for key
creation and its exact scope. An earlier activation that permits only existing
credentials does not authorize creating another key. Review and publish the routing
candidate and bind its exact activation scope before requesting that new authority.

The worker reads committed posted cards, verifies the Slack permalink, and uses
the existing SMS outbox preparation and permanent send reservation. This recovers
an interruption between card posting and reminder preparation. Prepared alerts
that became stale are suppressed. Approved, declined, revised or expired cards
without alerts are excluded. Attempted or uncertain sends are never automatically
retried; use the existing original-provider-resource reconciliation procedure.
SMS remains an attention notice and Slack link, with no decision authority.

`alert_cli process-once --project PROJECT` runs one bounded batch. The hosted worker
runs separately from signed acknowledgement and owner decision processing.
Its health is visible as `reminder_worker`; its failure does not disable the owner
receiver. Repeated failures stop it and require operator recovery. Check sender
configuration, eligible work and outbox history before enabling it. Enabling the
worker can send eligible pending reminders; do not replay completed proof cards.

## Continue an approved discovery step

An APPROVE decision and an operation named `issues_pending` do not themselves
authorize implementation. The discovery adapter binds an operator-created record
to the exact approved planning version, package, original decision and held
operation. Its allowed action is `discovery_configuration`; build and release
authority remains false.

Freeze required finding keys at preparation. Record confirmed, not-applicable or
unresolved findings with provenance. They are append-only revisions outside the
original package. Source records establish conventions and comparator details;
they cannot supply missing owner choices. Resolve required fields before continuing.
Not-applicable findings still need an explanation and provenance.

The operator continues with the exact discovery revision and findings hash. The
adapter queues one fresh planning version while preserving the original confirmed
brief, source, package and decision. The held operation is consumed only as a
discovery handoff. The planner receives bounded findings as quoted data; the new
manifest binds their context hash. No build job or issue-provider write is created.
Ordinary preapproval revision behavior remains unchanged.

Deploy compatible coordinator and Slack-service manifest handling plus the planning
worker before queuing a continuation. Apply SQL 009 through the explicit
`discovery_cli migrate` command under the installation's migration authorization;
status and finding commands do not migrate the database. Keep required/finding
input files private, bounded regular JSON files. Normal service migration commands
do not apply SQL 009. Preserve those migration/start commands and use an authorized
operator execution route to the private database for the separate discovery step.
If that route is unavailable, report migration and recording as pending; a healthy
receiver does not establish discovery readiness. Obtain explicit authorization for
additional private operator access and keep its scope bounded to the required
operation. Preserve public endpoints and normal service lifecycle commands.
For explicitly temporary access, revoke it, verify its absence and remove local
key material after the authorized operation. Record cleanup evidence privately.

After preparation and recording, verify the discovery revision, exact findings
hash, unresolved keys and unchanged parent package/decision. Keep the held issue
operation intact and do not invoke continuation while required findings are
unresolved. An empty reminder preflight proves the observed queue state only; it
does not verify persistent sender credentials or establish reminder delivery.

The successor package needs exact-package operational review, a published reusable
checkpoint, and its own owner decision. The original approval remains in history
and grants no authority over expanded scope. Automatic planning-review and revision feedback remain separate gaps. The new
[execution candidate](execution.md) applies to newly scoped requests and does not
upgrade this discovery approval. Its connected verification and activation are
tracked in the current milestone. Ordinary revision
of a discovery successor is rejected with `discovery_revision_requires_context`
until a revision path can retain and revalidate those findings. This explicit hold
prevents silently queuing a plan that has lost its operational configuration.

## Resolve a request that already works

Use the private `discovery_cli resolve-without-change` command only after the owner
explicitly confirms that the existing behavior satisfies the request. This is an
operator procedure; a model finding or employee suggestion cannot authorize it.
Bind the exact project, discovery ID, revision, findings hash and stable event ID.
Supply a private confirmation document with exactly `owner_id`, `source`, `reference`
and `statement`; source is `operator_recorded_owner_confirmation`. The owner must
match the current registry. Keep the actual statement and attributable reference;
do not manufacture Slack evidence or infer confirmation from silence.

Additive migration 026 retains an immutable resolution. Only an unchanged approved
planning-only discovery with a held issue placeholder and no execution run can
resolve. The transaction consumes that placeholder and reaches a terminal outcome
without revising the original package or creating a build, issue or deployment.
Unresolved findings stay as evidence; closure does not falsely confirm them. Replays
of the same event are idempotent, and altered confirmation conflicts. Normal progress
delivery reports the outcome in the existing source and owner threads.

## Operational review response and recovery

The pre-approval reviewer must return its completed verdict from the supplied
frozen package and brief in one response. It must not issue a progress note, request
source tools, or promise a later review. A cancelled or incomplete CLI response is
not a review, even when its text resembles a verdict. Retain its exact evidence.
The private shared worker can make exactly one automatic retry when retained output
proves a single-call, correct-session, correct-model cancellation with the explicit
CLI turn-limit error. It rechecks the exact current reservation before retrying.
Record each failure immutably and retain its private output; neither partial text
nor the failure receipt is a verdict. Two failures stop the request and report
needs-attention in its original thread. Missing, mismatched or uncertain output
stops without another model call. Restart recovery can consume a retained completed
response read-only. A lost failure acknowledgement replays the same report, not the
model. Park acknowledged terminal failures so other requests can proceed.

This bounded recovery is separate from the limit on planning revisions. It grants
no owner decision or build authority. Previously recovered requests and old failure
evidence are not replayed. Publish the reviewed generic/private checkpoint before
the normal owner card. Installation state is recorded in compatibility.
