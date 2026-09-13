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

The candidate deliberately has no model caller, outgoing Slack sender or
planning dispatcher. A follow-up received before its root returns a retryable
failure; recovery after Slack exhausts retries is not implemented. Keep intake
inactive until the supported interview bridge and recovery procedure are ready.
Local synthetic/database tests are distinct from real Slack delivery and an
owner-driven end-to-end test.

The provider contract comes from Slack's [request signing guide](https://docs.slack.dev/authentication/verifying-requests-from-slack/)
and [Events API documentation](https://docs.slack.dev/apis/events-api/).
