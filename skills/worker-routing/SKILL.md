---
name: Worker routing
description: >-
  Use when choosing Bot vs Grok Build vs Cloud Agent vs cheap mechanical work
  for a stage.
---
# Worker routing

Separate work into:

- **ROUTING** — who owns it (Chief)
- **MECHANICAL** — extract/transform/format (cheap Bot work)
- **DEEP REASONING** — ambiguous analysis where mistakes are expensive (Analyst owns; may execute via Grok Build headless)
- **EXECUTION** — browser, terminal, coding (specialist Bot; code via Build or Cloud Agent)
- **VERIFICATION** — independent check (Verifier; preferably fresh session with edits denied)

Do not use the most expensive path because it exists.

## Prefer

| Work | Path |
|------|------|
| Format, move, thin extract | Bot |
| Cited research / synthesis | Analyst → optional Build read-mostly |
| SPEC/architecture judgment | Architect |
| Closed code change | Developer → Build or Cloud Agent |
| Claim/number check | Verifier fresh session |
| Chat UI / desktop | Bot computer tools — not Build plugins by default |

## Anti-patterns

1. Build for mechanical work
2. Ignoring failed auth / missing models
3. Always-approve on send/publish/purchase/delete/prod
4. Letting Build own the chat-of-record (Bot writes HANDOFF)
5. Hiring a permanent "Build specialist" Bot
6. Skipping Analyst/PM ownership because Build drafted text
