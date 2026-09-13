# Bounded gateway for an existing SMS bot

**Alpha.5, 2026-09-12: message-first feasibility.** Private gateway code has
completed repair, review and verification. A paired synthetic Slack card was
posted and its matching SMS original receipt reports delivery. Actual owner
decision and SMS-to-Slack terminal closure are not verified; this proof is incomplete.
The current gateway validates the full SMS command. It does not implement the
[proposed message-first renderer, short commands or RCS adapter](message-first.md).
The public kit supplies neither this runtime nor an installer. Check
[current status](../../../docs/status.md) and [compatibility](../../../compatibility.json)
before using it. Earlier milestones retain their own historical evidence.

## Credentials and authority

Retain the installation's existing messaging account, registered number and bot
interface. A separate trusted gateway keeps private database access and a dedicated
Restricted Twilio Messaging read/create key in its environment. The provider key
never goes to the bot, model prompt, public repository or Slack receiver. Restricted
resource permissions do not inherently limit individual phone numbers or Message
SIDs; fixed application bindings provide that narrower boundary.

The bot receives only a short-lived gateway bearer tied to one exact project,
request, version, package digest, prepared notification operation, registry digest
and expiry. Treat that token as a secret. Do not paste it into public checkpoints,
URLs or logs. Creating the dedicated provider key is an account-owner-authorized
setup action; it does not create a new messaging account or number and does not
constitute approval of a plan.

The trusted operator prepares the reviewed package and delivery. The bot cannot
choose a phone number, message body, publication URL, arbitrary provider URL,
credential, grant, original-message JSON or owner verdict. Updating the grant or
changing scope is an operator action, never conversational bot output.

## Narrow interface

These routes are implemented and covered by private tests. The gateway service
configuration holds the authorized provider key privately. For each new proof,
the operator completes the public checkpoint, prepares the reviewed outbox and
verifies the exact expiring binding and deployment before using these routes live.

| Route | Caller input | Required server behavior |
| --- | --- | --- |
| `GET /healthz` | None | Liveness only; not proof of database, grant, provider or approval readiness |
| `GET /status` | Bearer only | Safe state for the bound operation/version; no body, challenge secret, phone or newer-version details |
| `POST /send` | Bearer and `{}` | Validate the current bound authorization, reserve durably, attempt at most one fixed provider POST, then persist factual outcome |
| `POST /reconcile` | Bearer and `{"message_sid":"SELECTED_OUTBOUND_SID"}` | Fetch and validate that original outbound resource; preserve the existing attempt and never resend |
| `POST /ingest` | Bearer and `{"message_sid":"SELECTED_INBOUND_SID"}` | Fetch that original inbound resource, validate exact bound scope, and let the core decide |

The selected SID is only a locator. The server independently GETs the original
Twilio resource and verifies its account, sender, recipient, direction, status and
time. It then matches the original full command to the exact bound request/version
and operation's challenge secret before core ingestion. A same-project message for
another request, including an already processed SID, cannot supply authority or
reveal that other request's outcome. No message-list scan is part of this path.

Grant expiry and challenge expiry are separate. An expired or revoked bearer cannot
start a new gateway operation, including status or provider reads. Recheck authorization
after waiting for database locks and before starting a provider action. A send also needs the
current unconsumed challenge and delivery authority. Once a provider send has been
attempted, retain factual finish evidence even if access expires, scope changes or
another approval surface wins. Terminal status and factual reconciliation do not
reopen dispatch. Lost responses, restart and uncertainty never authorize another
POST; reconcile the existing operation instead.

## Supervised proof and records

Use a fresh reviewed synthetic planning-only package. For the paired proof, follow
[the same-request procedure](sms-approval.md#paired-slacksms-proof-on-one-fresh-request)
and verify the Slack card and SMS share the exact package/version/challenge.
Preserve the earlier Slack package/outcome and the separate SMS delivery and
cancellation history; cancellation must not be recorded as an owner decision.
Publish and verify the [public checkpoint](approval-checkpoints.md)
first, recording its commit and known pre-dispatch limits privately. Then prepare
the outbox and expiring grant, finish the exact binding/deployment checks, and
complete the private checkpoint before requesting the owner decision. Deployment
is a condition for live use, not a prerequisite for publishing this snapshot.
Do not send until the current prepared operation, grant and challenge are verified.

The owner personally sends the full challenge reply through the existing SMS
interface. The bot or operator may locate its original SID; a paraphrase or chat
confirmation is not original provider evidence. A liveness response, accepted
provider creation, reported delivery or nonzero ingest count does not prove owner
approval. Verify the bound durable decision and consumed challenge separately.
APPROVE leaves exactly one held `issues_pending` operation; DECLINE records
`declined` and REVISE records `needs_revision`, without creating that operation.
No issue execution, build or release is authorized by this synthetic package.

This remains supervised: no automatic inbound listener or unattended end-to-end
bot integration is claimed. Preserve existing bot polling, cursors, messaging
handlers and opt-out behavior. After the decision, publish only its sanitized
outcome, verify that public commit, append it to the private checkpoint and revoke
access explicitly temporary for the proof. Keep raw provider, approval and account
records private.
