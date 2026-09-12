# Test the SMS approval lane

This runbook describes the separately implemented private coordinator. The public
preview still ships no runtime or installer. A successful Slack test does not
send a text or prove SMS approval. Read the current status and compatibility
manifest before treating any step as configured or live-tested.

For an existing bot interface, read [the bounded gateway reference](sms-gateway.md).
The pre-dispatch snapshot records repaired private code and verification. It keeps
provider keys on a trusted server and gives the bot only one-operation gateway
access. Exact binding/deployment and live SMS outcomes are later conditions; this
preview does not install a listener or change the existing number.

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
