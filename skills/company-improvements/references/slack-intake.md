# Durable Slack suggestion intake

This is the next private implementation slice after the completed supervised
SMS-reminder-to-Slack approval proof. It is not a public runtime release or a
verified native Grok Bot connection. Consult the current status before activation.

The receiver checks Slack's signature over the original request body, delivery
timestamp and fixed installation identity. An explicit leading keyword starts a
conversation; the same requester uses that keyword on follow-ups in its thread.
Ordinary conversation, bot events and edits do not create work. Sessions retain
their original source and configuration binding in PostgreSQL. Replayed events
and repeated deliveries of a message must not duplicate sessions or transcript
entries. Conflicting replays and changed configuration require reconciliation.

An accepted suggestion is only `pending_interview`. It does not confirm a brief,
request owner approval or authorize execution. The interview connection must
retrieve the exact session, ask its questions in the same thread, preserve the
requester's confirmation and submit the resulting brief once to the coordinator.
That bridge remains a separate integration milestone.

Use an installation's own private project registry, app identity, bot identity,
channel, requester allowlist and trigger. The private candidate uses a separate
profile with `schema_version`, `project`, `app_id`, `bot_user_id` and `trigger`.
Database and signing-secret values remain in the service environment. A signed
Slack delivery does not prove that a message attributed to a user was typed by
a human: an integration posting with that user's token can share that identity.
Do not treat this intake as owner approval or use a text prefix to authenticate a bot.

The original inbox has no model caller, outgoing Slack sender or
planning dispatcher; later private adapters are described below. A follow-up received before its root returns a retryable
failure; recovery after Slack exhausts retries is not implemented. Keep intake
inactive until the supported interview bridge and recovery procedure are ready.
Local synthetic/database tests are distinct from real Slack delivery and an
owner-driven end-to-end test.

The provider contract comes from Slack's [request signing guide](https://docs.slack.dev/authentication/verifying-requests-from-slack/)
and [Events API documentation](https://docs.slack.dev/apis/events-api/).

## Interview record and planning handoff

The next private component records questions and versioned briefs against the
exact input-message count. An agent can propose a brief; its output cannot mark
that brief confirmed. A trusted confirmation adapter must bind the requester,
original source event and exact current draft. New input makes an earlier draft
stale. Preserve the original response and confirmation history.

The internal confirmation proof uses a stored original Slack message containing
the exact draft hash. This is a transport contract for development, not the final
staff interface. Do not ask staff to copy hashes. Native confirmation and verified presentation now have a source implementation
below; live integration and the Grok bridge remain required before activation.
The bot receives no database credential or bearer-authorized confirmation route.

After confirmation, freeze the source and brief in a durable handoff record.
Submit that same payload to the coordinator with the same idempotency key on
recovery. A lost response must not generate another request or change the brief.
An extra message before dispatch requires revision; a message after dispatch
cannot rewrite the already submitted snapshot. Brief confirmation permits
planning only. Owner approval, issue creation, building and release retain their
separate gates.


## Slack presentation and signed confirmation

The private adapter renders all saved brief fields in plain-text blocks in the
original thread. It reserves delivery before sending and validates the provider
acknowledgement. Ambiguous sends must not be silently retried. Questions and
incomplete briefs have no confirmation button.

The button identifies a durable presentation. Its signed callback must match the
original requester, configured app/workspace/channel, posted message and latest
unchanged draft. Store real interaction evidence; never manufacture a source
message. Confirmation freezes the same planning-only handoff used by the ledger.

Compose the interview handler with the owner receiver, or configure a distinct
Slack app, before activation. Do not replace the working owner interactivity URL.
Native Grok integration, automatic dispatch and terminal button updates remain
unfinished. Local tests do not prove a live connection.

Provider references: [block actions](https://docs.slack.dev/reference/interaction-payloads/block_actions-payload/)
and [message posting](https://docs.slack.dev/reference/methods/chat.postMessage/).


## Integrated runtime and bot boundary

The private integrated host now composes signed events, the existing owner
interaction URL and the interview action handler. Existing owner actions retain
their own validator. Interview routing preserves the original signed request
bytes and revalidates them at the interview boundary.

Give the interview bot a separate project-bound token. Its API permits listing
interview metadata, retrieving the exact source/response snapshot and proposing
a question or draft with an expected message count and stable event key. It
cannot confirm, approve, publish, change source identity or invoke a build.
Keep tokens in private configuration; never in public instructions or examples.

A trusted bounded cycle publishes eligible responses and hands confirmed briefs
to planning. It skips stale responses, completed handoffs and uncertain outbound
reservations. Do not reset ambiguous sends to force another attempt. The cycle
does not execute a planning model; run the separately configured planner.

Before cutover, replace the native routine's direct Slack posting and typed-decision
logic with the limited API flow. Keep one routine and preserve source restrictions.
The inbox requires the configured exact prefix followed by whitespace and text;
a platform substring trigger alone is insufficient. Follow-up messages must also
use the prefix. Handle event/inbox arrival races with bounded read-only recovery.

Complete the required event subscription and bot permissions, verify deployment,
and prove a real native response before calling this connected. Restrict a proof
to its configured requester; do not silently enable the entire staff allowlist.

Activation checks: verify the signed event URL is saved, the intended event is
subscribed, required private-channel history permission is installed, and the app
is a source-channel member. Verify healthy worker status plus rejected anonymous
and accepted scoped API reads. These checks do not prove native response delivery.
A deployment restart may reuse older startup metadata; verify the actual running
entry point after changing the service configuration.
