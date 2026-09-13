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
The original Grok CLI document review was accepted after supplemental evidence
verification and normal API recording. Live alert/owner-decision verification
remains pending. This public skill ships no configuration installer or runtime.
