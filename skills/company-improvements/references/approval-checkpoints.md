# Publish at every approval stage

This is an **operator** procedure today. Automated export and coordinator validation
of a public publication receipt are not implemented.

## Before requesting the decision

1. Update the skill and affected setup/recovery references with implemented behavior
   and supported scope. If instructions did not change, record the reviewed no-change
   reason against their current revision in the private checkpoint.
2. Update [status](../../../docs/status.md), [compatibility](../../../compatibility.json)
   and [changelog](../../../CHANGELOG.md) for this milestone: stage, tested scope,
   actual results, test type, known gaps and next gate. Distinguish privately observed
   integrations from shipped and independently installable components.
3. Review an explicit list of public files. Include generic source/instructions/tests
   and synthetic examples. Keep private plans, profiles, provider identities, approval
   receipts, credentials, logs and operational history outside public Git history.
4. Commit and push the reviewed public snapshot. Independently read remote visibility,
   exact commit and intended file contents. Keep the commit permalink; local files or
   an unverified push do not satisfy publication.
5. Copy [the checkpoint template](../../../templates/approval-checkpoint.json) into
   private operator storage. Fill milestone, skill version, public commit/file hashes,
   implementation revision, validation evidence and the exact private request,
   package/version and scope. Confirm owner access to the separate private plan;
   a private repository URL does not establish direct opening in the intended mobile app from Messages or sign-in-free access.
   Any future in-message presentation must be verified against that exact frozen
   package through its implemented adapter.
   Never publish the filled record in this public repository.
6. Once the checkpoint is complete, present the real owner approval through its
   verified provider. Include the reusable snapshot link alongside the private plan
   when supported, or in the accompanying update. The coordinator validates the
   owner's actual decision; publication is not an approval or deployment authority.

If publication fails, keep the pre-approval checkpoint incomplete and reconcile the
remote state before retrying. Continue independent authorized work. Do not make a
private repository public as a shortcut or claim automatic synchronization.

## After the decision

Verify the original provider-backed decision and durable state. Record it privately.
Publish a sanitized outcome and remaining gaps in status/changelog; commit, push,
verify and append that commit to the private checkpoint. This applies to approval,
revision and decline. Do not modify frozen plan bytes or repeat a card/decision
because documentation publication failed. A valid owner decision remains recorded
while post-decision publication is reconciled.

The first public Slack result is a retrospective backfill because the maintainer
requested this publication rule after that test. Do not imply that its public
snapshot existed before the owner's click. Subsequent checkpoints precede requests.
