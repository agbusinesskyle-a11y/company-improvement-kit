# Reminders and discovery after planning approval

The private coordinator and integrated Slack service have been deployed with their
installed source verified against the approved candidate. Reminders remain disabled
pending persistent sender access; explicit discovery migration and live recording
await an authorized route to the private database. Track hosted code, worker
enablement and discovery readiness separately. The public kit is documentation.

## Resume the existing reminder path

The integrated host can explicitly enable `COMPANY_IMPROVEMENTS_REMINDERS=enabled`.
Absent or `disabled` leaves the worker off. Configure the existing Slack identity
and `TWILIO_ACCOUNT_SID`, `TWILIO_API_KEY_SID`, `TWILIO_API_KEY_SECRET` through the
installation's authorized secret store. The account must match the selected
Slack-only profile. Do not reuse revoked test credentials or alter the registry
digest merely to enable the worker. The host uses its intake project; other
profiles are not swept automatically.

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

The successor package needs exact-package operational review, a published reusable
checkpoint, and its own owner decision. The original approval remains in history
and grants no authority over expanded scope. Automatic review, revision feedback,
Linear execution and application release remain separate gaps. Ordinary revision
of a discovery successor is rejected with `discovery_revision_requires_context`
until a revision path can retain and revalidate those findings. This explicit hold
prevents silently queuing a plan that has lost its operational configuration.
