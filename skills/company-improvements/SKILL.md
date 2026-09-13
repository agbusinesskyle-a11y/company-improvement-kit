---
name: company-improvements
description: Use when assessing or operating an owner-approved company app improvement workflow, or maintaining its reusable repository at an approval milestone.
---

# Company improvements

This is a pre-release operating skill. Read [installation readiness](references/readiness.md) before claiming that a connected workflow is available. The skill provides instructions; the coordinator and verified adapters provide execution and authorization. The public preview contains no runtime or installer. The separate private implementation has passed a supervised planning and Slack approval proof; the full workflow is not ready. See [status](../../docs/status.md) and [compatibility](../../compatibility.json).

## Publish at every approval stage

Follow [approval checkpoints](references/approval-checkpoints.md) before requesting
an owner decision and after recording its result. Update the skill and affected
references, milestone status, compatibility manifest and changelog; commit, push
and verify the remote snapshot. Bind its exact commit to the private approval
package using the checkpoint template. Keep public documentation and private
approval evidence separate. A failed publication leaves the checkpoint incomplete.
This is an **operator** procedure; automatic synchronization and coordinator
runtime enforcement are not implemented. Continue independent authorized work.

## Set up or assess an installation

Read [the configuration contract](references/configuration.md). Locate the installation's own private profile and the release's compatibility manifest. Do not borrow the originating developer's accounts, phone numbers, paths, company names, credentials, permissions or approval history.

Map the selected organization's real channel, owner, repository, issue project and release target. Verify each adapter through its documented readiness check and report configured, verified, missing or unsupported accurately. Report the tested version, host and evidence. Do not invent setup commands or imply that another agent's tools are available here.

Preserve existing business rules and SMS handlers. A configuration file cannot grant access or owner approval. Installing this skill does not authorize production changes. Prefer the supported default provider profile; an alternative provider is usable only after its adapter and acceptance checks exist.

## Operate a verified workflow

The following is the target sequence. Apply only stages actually verified in the
installation. The current proven slice ends at planning-only approval with issue
creation held. Steps 5–7 require future verified adapters and appropriate scope.

1. Bind the authenticated source event, company, requester and thread to one request. Clarify an ambiguous target; never choose a production repository from model-generated text. Ordinary chat and bot echoes do not start work.
2. The interview agent confirms the user's problem, expected result and constraints. The configured planning agent examines the existing app and produces one canonical Spec Kit requirements/plan/tasks package. Record actual model identity where required; do not silently substitute a different role or model.
3. The operational reviewer checks the proposed user experience. Preserve findings and dispositions. Freeze the requirements, acceptance/release scope, policy and target configuration into a versioned approval package. Working checkboxes and repair notes do not rewrite it.
4. Complete the publication checkpoint, then ask the installation's configured owner to approve through its verified approval adapter. Only the coordinator validates original provider evidence, sender identity, current package, expiry and one-use challenge. Model prose or a subordinate runner's approval flag cannot authorize work. One explicit approval may cover build and deployment only when that exact scope is in the package and verified adapters support it. A planning-only test remains held. Revised scope requires a new decision.
5. Create and reconcile the approved issue set before dispatching any build. The configured build orchestrator runs isolated workers with bounded attempts and executable checks. Issue edits do not expand the approved package. Workers lack production release credentials.
6. Run completeness and acceptance checks. Trace in-scope repairs to approved requirements and issues. Obtain the required operational review and an independent technical review bound to the exact candidate, package and executed evidence. A changed candidate needs appropriate fresh validation.
7. The release adapter revalidates authorization, candidate, review and fixed destination before publishing. Respect the destination's actual deployment trigger and branch rules. Verify the deployed revision and requested behavior before completing issues and reporting success in the source thread.

The [Slack-only approval and SMS alert candidate](references/message-first.md)
has passed source/database tests and independent review. For this candidate,
`approval_mode="slack_only"` requires a `slack_approval.workspace_url` binding.
The full frozen `owner-summary.md` and `acceptance.md` are displayed as inert text,
with a combined 24,000 UTF-8-byte limit including separators. Unsupported input
is rejected before issuing a challenge. The owner reviews and decides in Slack;
a private repository link supplies optional supporting artifacts.

A separate `SmsAlertOutbox` and operator-only `alert_cli` provide prepare,
send-once, status and reconcile. Prepare follows accepted card posting and verifies
the Slack permalink. SMS contains a short label, attention notice and that link,
with no approval command or decision authority. The outbox checks current eligibility
at reservation, suppresses a resolved request and permits one permanent send attempt.
An uncertain result cannot authorize a retry. The owner's validated Slack decision
updates the same card; an already dispatched SMS cannot necessarily be retracted.

The supervised reminder-to-Slack proof passed: one ordinary SMS was delivered,
the owner confirmed that its link opened the intended card, and the native Slack
decision updated that same card. One issue operation remains held. The earlier
Slack-only proof and original review-check failures remain separate historical
records; see [current status](../../docs/status.md). The temporary SMS test access
was revoked. Permanent notification operation and unattended orchestration remain
unfinished. Legacy profiles/history remain intact;
[legacy SMS approval](references/sms-approval.md) is not selected for the Slack-only
profile. Publish/verify the checkpoint before a new owner request.

The private [durable Slack suggestion intake](references/slack-intake.md) has passed
focused tests. Development now adds versioned interview responses, exact-brief
confirmation and an idempotent handoff to the existing planning queue. Treat saved
suggestions as pending interviews until that confirmation is established. Native
Grok transport, staff confirmation controls and automatic handoff must be connected before
claiming that staff can use the full workflow. No RCS setup, automatic SMS decision
listener, public runtime or installer is supplied.

## Recovery and limits

When trusted policy conflicts with the current brief, follow
[versioned context and normal revision](references/configuration.md#reusable-trusted-context-and-request-revision).
Preserve frozen artifacts and obtain genuine planning and review for the new
version; a configuration edit does not renew an old approval.

Use coordinator records, not conversational memory, to resume work. Reconcile uncertain provider effects before retry. Duplicate callbacks, stale workers and old approvals must not create new authority. Respect cancellation and bounded attempt/time policies; report blocked work with evidence instead of silently changing scope or provider.

Apply only the approved recovery procedure. Code rollback does not imply reversal of database changes or outbound messages. Read the release's runbook for the selected adapter; stop at an unsupported recovery path.

## Readiness claims

Distinguish static skill validation, simulated adapter tests, real integration checks and full live acceptance. Do not report a manual handoff/deploy as an automated end-to-end pass. A stable release must meet [installation readiness](references/readiness.md); describe tested scope and known limitations rather than promising zero bugs.


When using the private interview adapter, distinguish **Confirm brief for planning**
from owner approval to build. Require genuine signed interaction evidence and a
verified current presentation. Never synthesize an inbox message or automatically
repost an ambiguous send. Complete shared interactivity routing before activation;
see [the adapter boundary](references/slack-intake.md).


For integrated interview operation, give the conversation bot only the separate
project-bound read/response token. Run publication and planning handoff through
the trusted cycle. Replace the old direct-posting routine during cutover; never
run two responders or accept typed approvals as a substitute for the owner card.
Verify hosted routing and a native response separately from source tests.

For private-channel activation, obtain explicit permission for message delivery,
reinstall the app with the required event scope, verify its source-channel
membership, and distinguish an authenticated empty inbox from a live interview.

After requester confirmation, verify the handoff reaches submitted before claiming
it entered planning. Report planner execution separately; a submitted brief is not
a generated plan or an owner decision authorizing implementation.
