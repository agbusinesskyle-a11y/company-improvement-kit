# Message-first approval feasibility

**Alpha.5, 2026-09-12: proposed experience, not implemented.** A paired synthetic
Slack card was posted and its matching SMS original provider receipt reports
delivery. The actual owner decision and SMS-to-Slack terminal closure are not
verified. This delivery result does not complete the approval proof.

## Desired owner experience

Present a detailed frozen change order in Messages: the proposed changes,
requirements, acceptance criteria, limits, and exactly what approval authorizes.
The owner should be able to review it there and choose Approve or Disapprove.
Preserve an exact version/package binding and accessible private supporting
artifacts; never make private plans public to avoid access friction.

The current SMS instead contains a private plan URL and long exact reply command.
A private repository blob link cannot be assumed to open directly in the intended
mobile app from Messages or without sign-in. Confirm access on the actual owner path. A link or successful
message delivery does not establish informed review or a recorded decision.
There is no detailed body renderer, short-command support or RCS adapter today.
Do not silently accept bare Approve/Disapprove text under the existing command
validator or claim a conversational reply is an approval.

## Transport and evidence gates

For ordinary SMS, design and verify any detailed rendering and shorter reply
format before advertising it. Preserve the frozen package, owner, expiry and
one-use decision binding. Define how a short reply distinguishes concurrent
requests and maps Disapprove to a supported negative outcome without authorizing
work. Rendering or scope changes require the appropriate fresh review/checkpoint.

RCS phone business-setting confirmation is only a prerequisite. It does not prove
provider sender registration, capability, routing or functioning buttons. The RCS
evidence adapter is unresolved. Hidden quick-reply metadata is available through
original signed webhooks but is not documented in the Message GET representation.
One candidate is signature-verified webhook evidence. Another candidate puts an
explicit opaque request code in the visible button title and verifies the original
provider Message GET Body, if a real provider sample proves the code is preserved.
Neither candidate is implemented or verified here.

A new credential/evidence review must establish an original provider-backed choice
and its exact owner/package binding, then prevent replay and duplicate decisions
across approval surfaces. A display label, bot report or fabricated callback is not
sufficient evidence. Do not treat hidden payload as retrievable through GET, assume
the visible code survives transport, or reuse the existing SMS original-GET proof
as proof of RCS buttons.

Provider registration, terms and fees require their own setup decisions. Neither
phone settings nor acceptance of provider terms approves an application change
order. No automatic inbound listener is implemented.

## Evidence before claiming completion

Follow [approval checkpoints](approval-checkpoints.md): publish and independently
verify the public snapshot before a new owner request, then bind it privately to
the exact package and verified presentation/adapter. Check actual owner access and
real decision behavior. Verify one durable core decision and, for an SMS-to-Slack
proof, the matching Slack card's terminal update separately from delivery. Keep a
partial or failed result honest; it does not authorize another send or fabricated
event. Publish the sanitized outcome after the real decision and keep provider
identities, credentials, private plans and raw approval evidence out of public Git.

The public preview contains no runtime or installer and proves no complete
workflow. See [current status](../../../docs/status.md) for the evidence boundary.

Provider references: [inbound webhook fields](https://www.twilio.com/docs/messaging/guides/webhook-request),
[Message GET schema](https://www.twilio.com/docs/messaging/api/message-resource),
and [RCS onboarding](https://www.twilio.com/docs/rcs/onboarding).
