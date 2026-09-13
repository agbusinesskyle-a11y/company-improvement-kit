# Private installation configuration contract

This document defines the fields the implemented setup flow must collect and validate. It is not a current executable configuration schema. A release must publish its actual schema and matching redacted example before claiming installability.

| Configuration group | Required information | Validation |
|---|---|---|
| Organization | Local organization ID and display name | Cannot resolve to another organization's profile |
| Project | Stable project ID, repository, non-deploying branch policy, issue project, release target | Read the actual provider objects and deployment triggers; reject unknown mappings |
| Intake | Slack workspace/channel, permitted requesters, verified bot connector and trigger | Confirm identities and a correlated request/result round trip |
| Owner approval | Owner ID, verified destination, approved sender and incoming-event route | Owner participates in a real challenge; wrong/stale/replayed replies fail |
| Model roles | Interviewer, planner, operational reviewer, builders, independent technical reviewer | Record supported identities and actual invocation evidence; no silent substitutions |
| Execution | Worker host, build orchestrator, source access, work directory and limits | Restart recovery and isolated execution; no production credentials in build process |
| Release | Explicit services/environments, release identity, check and recovery procedure | Wrong target or code revision cannot release; successful release has live proof |
| Operations | Request retention, backup/recovery, notifications, pause/cancel and support contact | Verify restore/cancellation procedures and keep secrets out of shared logs |

Secrets live in the installation's approved secret store or host environment, with credential references in configuration. The source repository contains only synthetic examples and field names. Do not ship personal CLI sessions, browser cookies, Slack/SMS history, private code, private project registries or machine-specific paths.

Each friend initially runs a separate installation with their own accounts and database. A shared hosted service with cross-customer administration is outside the first release. The original owner's approval never authorizes a friend's deployments, and the reverse also holds.

The first verified provider profile is the support boundary. A profile may map model roles without changing the workflow, but a newly selected model, operating system, issue tracker or deployment provider requires its own compatibility check and documented evidence. Do not describe a generic adapter interface as implemented support.

## Reusable trusted context and request revision

A project's constitution holds reusable business rules, safety limits and approval
scope. Keep a prior request's event markers, thread identifiers, expected response
text and temporary setup state out of durable policy. Current request facts belong
in the authenticated source and confirmed brief. Synthetic test fixtures need this
same separation.

Keep trusted checkout context and the constitution in versioned, read-only
snapshots. Compare them with the confirmed brief before planning. A conflicting
trusted rule requires explicit correction; do not tell the planner to ignore it.

If a conflict is found after a package is frozen, retain the old snapshot, artifacts
and results. Create a new context snapshot and policy version. Narrowly update the
intended project's `checkout_path`, `constitution` and `policy_version` when these
are the changed fields, preserving other profiles and authorization bindings.
Verify the active configuration on every service that consumes it. A registry edit
alone does not refresh an existing request's captured context.

For a request still eligible for revision, use the normal revision API with the
current `expected_version`, confirmed brief and a fresh idempotency key. This
captures the current trusted context in a new request version and invalidates old
eligibility while retaining frozen artifacts. Run genuine planning for the new
job, publish and verify its exact artifact bytes, obtain an actual review of that
package, and record the real verdict through the normal API. Do not edit frozen
artifacts, transfer an old review to a new hash, fabricate a review, or reset old
attempts to make recovery appear complete. A context edit cannot reopen an approved
request; follow the supported state rules.

## Alpha.7 private candidate fields

The private candidate accepts optional project `approval_mode="slack_only"`.
If omitted, legacy behavior is preserved; do not infer Slack-only enforcement for
old profiles. Slack-only mode requires the existing `slack_approval` identity
bindings plus `workspace_url`, a canonical `https://<workspace>.slack.com` origin
without a path, query, fragment, port or trailing slash. It is bound to the exact
posted card when verifying its provider-returned permalink. This is not an
arbitrary alert destination supplied by a bot.

The full frozen `owner-summary.md` and `acceptance.md`, with their separators,
must fit a combined 24,000 UTF-8-byte review budget and the supported inert-text
rules. Invalid or oversized content is rejected before challenge creation;
shortening or changing frozen scope requires normal revision and review.
Supporting private artifact publication remains part of package provenance, but
reviewing the displayed owner summary and acceptance must not require opening it.

Notification commands are private operator interfaces with environment-only
configuration; see [the candidate runbook](message-first.md). Keep database and
provider credentials on the trusted operator host. Configuration values and
credentials are not approval authority. Source/database tests and independent
review passed; isolated runtime wheel checks passed without a full installed test
suite. Hosted preflight verified the deployed source, registry bindings and schema.
The earlier Grok CLI document review was accepted after supplemental evidence
verification and normal API recording. That package received an actual Slack
approval and same-card terminal closure; no SMS alert was prepared or sent.
New-version genuine GPT-6 planning and all five hosted artifact bytes are verified.
Its Grok CLI review completed with acceptance, but the original harness failed
a verdict-marker formatting check. Supplemental verification passed, preserving
that original failure, and acceptance is recorded. The supervised reminder was
delivered and the owner approved in Slack; this does not prove unattended operation. See
[current status](../../../docs/status.md) for the separate milestones. This public skill ships no configuration installer or runtime.
