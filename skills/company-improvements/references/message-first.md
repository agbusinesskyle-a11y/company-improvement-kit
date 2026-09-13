# Slack approvals with SMS alerts

**Alpha.6, 2026-09-12: selected direction, not an implemented alert-only adapter.**
Slack holds the canonical review and owner decision. Ordinary SMS only draws
attention to it: “An approval in Slack needs your attention,” with a link to the
verified card. SMS replies never authorize work in this selected path. No RCS
sender registration or fees setup is being pursued.

## Required owner experience and delivery order

1. Freeze the reviewed change order and show its proposed changes, acceptance
   criteria, limits and exact approval scope in Slack. Keep supporting artifacts
   private, but do not make a separate repository login mandatory for the owner
   review. Verify that the displayed details match the immutable package and that
   the configured owner can access them.
2. Complete [the public checkpoint](approval-checkpoints.md), then post and verify
   the exact Slack card and its decision controls. Do not text a missing or
   unverified card link.
3. The future alert adapter must check that the bound request is still unresolved
   immediately before dispatch, reserve durably and permit at most one send for
   that alert operation. Suppress alerts already resolved; a timeout or lost reply
   does not authorize a duplicate POST. Reconcile the original attempt.
4. The owner reviews and decides through verified Slack controls. Validate the
   original Slack event, configured owner, exact package and current one-use
   authority; record one durable decision. Update that same card to its terminal
   state and remove decision controls. A card-update failure does not reopen
   approval or justify a repeat SMS.
5. A decision can race with a dispatched alert. A sent SMS cannot necessarily be
   retracted, so its link must lead to the card's current state. A reply to the SMS,
   its delivery receipt or a bot interpretation cannot create a decision. Publish
   the sanitized actual result after the decision and retain evidence privately.

The alert-only adapter, its resolved-request checks and live acceptance proof are
not implemented. Existing SMS approval ingestion is a different capability and
must not provide decision authority for the new profile. Verify this exclusion
before use; do not infer it from this documentation change. Preserve existing
unrelated SMS handlers. No automatic inbound listener, public runtime or installer
is supplied.

## Prior work and current proof boundary

The earlier paired synthetic Slack card was posted and its matching original SMS
receipt reports delivery. Actual owner decision and SMS-to-Slack terminal closure
remain unverified. The test was cancelled through the normal API after the
direction changed, with its frozen package retained. Cancellation is not owner
approval. The cancelled card and scoped credential cleanup are verified; preserve the
delivery evidence and record cleanup separately from owner approval.

Alpha.5 explored detailed change orders and approval controls inside Messages,
including RCS. That proposal is not selected. Neither an RCS adapter nor working
buttons were proved; hidden reply metadata was not documented in Message GET and
the visible action/code alternative lacked a verifying provider sample. Preserve
[the historical milestone](../../../docs/status.md#2026-09-12--alpha5-message-first-feasibility-historical-not-selected)
without treating its feasibility work or phone settings as app-plan approval.
