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

For a separate SMS lane test, use [the SMS runbook](references/sms-approval.md)
and [the bounded gateway reference](references/sms-gateway.md). The bot receives
only an expiring token for one prepared operation and may supply a selected Message
SID as a locator. The trusted gateway keeps provider credentials and independently
fetches original evidence; bot text cannot approve. The dated pre-dispatch status
records reviewed private code and tests; it does not establish a deployed binding
or live SMS proof. Publish the pre-approval snapshot before outbox preparation and
final binding/deployment, then verify those conditions before sending. The public
preview provides no runtime.

## Recovery and limits

Use coordinator records, not conversational memory, to resume work. Reconcile uncertain provider effects before retry. Duplicate callbacks, stale workers and old approvals must not create new authority. Respect cancellation and bounded attempt/time policies; report blocked work with evidence instead of silently changing scope or provider.

Apply only the approved recovery procedure. Code rollback does not imply reversal of database changes or outbound messages. Read the release's runbook for the selected adapter; stop at an unsupported recovery path.

## Readiness claims

Distinguish static skill validation, simulated adapter tests, real integration checks and full live acceptance. Do not report a manual handoff/deploy as an automated end-to-end pass. A stable release must meet [installation readiness](references/readiness.md); describe tested scope and known limitations rather than promising zero bugs.
