# Test the SMS approval lane

This runbook describes the separately implemented private coordinator. The public
preview still ships no runtime or installer. A successful Slack test does not
send a text or prove SMS approval. Read the current status and compatibility
manifest before treating any step as configured or live-tested.

For an existing bot interface, read [the bounded gateway reference](sms-gateway.md).
The private gateway has reviewed code and verification. A paired synthetic Slack
card was posted and its matching SMS original receipt reports delivery. The
actual owner decision and SMS-to-Slack terminal closure are unverified; the proof
is incomplete. Provider keys stay on the trusted server; the bot receives only
one-operation gateway access. Current SMS uses a private plan URL and long exact
text command. Read [message-first feasibility](message-first.md) for the proposed
in-message change order and controls; no such renderer, short-command support,
RCS adapter or automatic listener is implemented.

## Ready before sending

Use a fresh request whose package covers one synthetic planning-only SMS approval
and no issue/build/release effects. A completed Slack request has a consumed
challenge and must remain unchanged. Bind the real account, registered SMS sender
and full verified owner destination before generating a new immutable package.
Use a genuine planner and operational review; publish and verify the exact private
plan. Publish and verify the public pre-approval snapshot before preparing the
outbox and final gateway binding/deployment. Complete those live-use checks and
the private checkpoint before requesting the decision. Do not require an already
deployed operation binding as evidence for this earlier public snapshot.

Use a trusted operator or separately verified gateway with private database access
and environment-only Twilio credentials. The bot receives only the gateway token,
never database access or provider keys. Twilio keys do not belong in model prompts,
this public repository or the Slack receiver. A Restricted key can limit resource actions, but Messaging read
and create permissions do not inherently restrict individual numbers or SIDs.
Verify the actual permissions and fixed application bindings. Preserve existing
SMS handlers, opt-out behavior and shared bot polling.

## Paired Slack/SMS proof on one fresh request

This is the supervised procedure; paired delivery alone does not complete the
proof. It is not an automatic fanout service.
Use the same fresh immutable request/version/package and shared challenge for the
Slack card and SMS notification. Keep the earlier completed Slack proof and the
separate delivered SMS, subsequent cancellation and absence of an owner decision
as their own historical records.

1. Update the public skill/status/compatibility/changelog, push and independently
   verify the exact public commit before either owner-facing card or text. This
   snapshot may precede package preparation; record both verified public commit
   and exact private package in the checkpoint before the owner is asked.
2. Cancel any superseded pending request through the normal API and verify its
   challenge invalidation without changing its history. Include both surfaces in
   the registry profile before new intake, then complete genuine planning/review
   and byte-verify the fresh private publication. Do not add a card to an old
   package or create a second independent approval authority.
3. Synchronize configuration and restart all receiver replicas before posting;
   stale configuration can freeze a superseded card display. Prepare SMS first,
   then Slack with the same challenge lifetime. Verify their exact shared
   request/version/package/challenge, intended owner and fixed destinations, and
   the gateway's one-operation grant and live binding.
4. Complete the private live-use checkpoint. Post the prepared Slack card and
   verify accepted delivery before sending the prepared SMS once. Keep original
   delivery evidence. A failed or uncertain send does not authorize another POST,
   and an expired challenge is not refreshed by retrying the same send.
5. Let the owner personally send the full SMS challenge reply. Independently fetch
   its selected original SID and validate the bound command before core ingestion.
   Verify one exact durable decision and consumed shared challenge. APPROVE leaves
   one held issue operation; DECLINE/REVISE leave no new issue operation.
6. Observe or invoke the existing terminal-update worker and verify that the exact
   matching Slack card displays the recorded outcome and removes decision controls.
   Record whether the update was supervised or automatic. The cosmetic update
   does not create approval; if it fails, preserve the decision and reconcile the
   existing update without reopening authority, repeating the SMS or replacing
   the card to manufacture a pass.
7. If Slack records the first genuine decision, retain it and report that the
   intended SMS-to-Slack direction was not proved. Duplicate/stale messages must
   not create another decision or issue operation. Publish the actual sanitized
   result and remaining gaps after the decision, verify the commit and append it
   to the private checkpoint. No build, release or issue execution follows.

## One send, one real reply

1. Prepare a short-lived challenge when the owner/operator are ready, then use the
   durable send-once operation once. Record the returned message identity privately.
2. Distinguish provider creation, handset delivery and owner approval. Preserve a
   known failed/undelivered creation receipt. Reconcile the original outbound SID
   if necessary; uncertainty never authorizes another send.
3. The owner personally replies using the full challenge command. A chat yes or
   model-authored approval cannot substitute for the original SMS.
4. Obtain the exact inbound Message SID from a trustworthy provider observation.
   Treat it only as a locator. The trusted operator or gateway independently GETs
   that resource from Twilio and validates account, sender/recipient, direction,
   timing and the exact bound request/challenge before core ingestion. It performs no
   message-list scan. A bot paraphrase cannot establish approval.
5. Verify the durable decision, exact request/version/package/owner and consumed
   challenge. APPROVE leaves one held issue operation. DECLINE leaves the request
   declined; REVISE leaves it needing revision; neither creates an issue operation.
   Provider status or ingest counts alone are insufficient.

The older polling command scans shared-sender history with a prior-day overlap;
do not describe it as an owner-only read or substitute it without addressing that
scope. The selected-original path is a supervised proof, not an automatic inbound
listener. Missing credentials, an unknown SID or expired challenge remains a real
blocker; do not fabricate a provider event.

Publish a sanitized result after the decision, retain restricted evidence privately,
and revoke access explicitly temporary for the test. The result does not establish
a complete unattended workflow or independent installation.

Sources: [Twilio Message resource](https://www.twilio.com/docs/messaging/api/message-resource)
and [Restricted API keys](https://www.twilio.com/docs/iam/api-keys/restricted-api-keys).
