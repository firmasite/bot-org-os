# Optional tools

Core install works **without** these tools.
Bots, Skills, and Artifacts folders do not require them.

Treat this list as recommendations. The Operator chooses what to add.
Do not install a large set of connectors on day one.

## Checklist (Operator chooses)

- [ ] **Grok Build** (`grok` CLI) — heavier reasoning and coding execution for Developer story packets. It is an **execution engine**, not a separate Bot. Install only if Developer work needs it. Docs: product help for the `grok` CLI on your account.
- [ ] **GitHub CLI (`gh`)** — clone and fetch this template from GitHub during Bootstrap. Optional if you paste files another way (zip, existing workspace path, raw URLs).
- [ ] **Cloud Agents / coding agents** — optional helpers for repository work when Developer needs them. Not required for org install.
- [ ] **Other connectors** — add only when a real bottleneck appears (email, chat, issue tracker, …). Prefer one connector that unblocks a logged pain over a full zoo.

## Rules of thumb

1. Finish Core install first (see [BOOTSTRAP.md](../BOOTSTRAP.md)).
2. Run one small Artifact + HANDOFF loop before adding tools.
3. Recommend, never require.
4. Log pain in [BOTTLENECKS.md](BOTTLENECKS.md) before adding more connectors.

## Related

- Beginner guide: [BEGINNER.md](BEGINNER.md)
- Install diagram: [diagrams/install-flow.md](diagrams/install-flow.md) (dashed “Optional tools” box)
