# Bot Org OS

Public template: docs, contracts, Skills stubs, and folder layout for a **Chief + phase specialists** org.

For use with Grok Bot. Not affiliated with SpaceXAI / not an official product.

### Begin here

1. [docs/BEGINNER.md](docs/BEGINNER.md) — plain-language explainer  
2. Diagrams: [roster-map](docs/diagrams/roster-map.md) · [install-flow](docs/diagrams/install-flow.md) · [artifact-bus](docs/diagrams/artifact-bus.md)

### Paste to install

Send this URL to any Bot that can create agents and install Skills:

`https://github.com/firmasite/bot-org-os`

That Bot should read [`AGENTS.md`](AGENTS.md) + [`BOOTSTRAP.md`](BOOTSTRAP.md) and install. **Linking is the install trigger.**

Manual copy steps are only a fallback when CreateAgent / Skills tools are missing — see [`docs/QUICKSTART.md`](docs/QUICKSTART.md).


## Optional tools

Core install works without extra CLIs or connectors.
See [docs/OPTIONAL-TOOLS.md](docs/OPTIONAL-TOOLS.md) for a checkbox list (Grok Build, `gh`, Cloud Agents, later connectors). Recommend only — never require.

---

## Why this exists

Anyone should recreate similar structure:

- **Chief** coordinates; specialists own Artifacts
- **Skills** shared; **Routines** only after a Skill is earned twice
- **Artifacts bus** + **HANDOFF** with three gates (source, evidence, action)
- **Hire only for a recurring, evidenced bottleneck** — not because a role name sounds useful
- **Shared-computer** hard limits

## Five primitives

| Primitive | Meaning here | In this repo |
|-----------|----------------|--------------|
| **Bots** | Persistent roles with contracts | `roster/` |
| **Chats** | Talk to one Bot or a small group | Core Team · optional Extended |
| **Prompts** | One-shots · **Skills** · **Routines** | `skills/` — Routines stay off until earned |
| **Tools** | Shared capabilities (box, connectors, Build) | Account-wide |
| **Artifacts** | Durable files on the bus | `workspace/` + `docs/ARTIFACTS.md` |

Details: [docs/PRIMITIVES.md](docs/PRIMITIVES.md)

## Roles

**Core (always on):**

| Role | Phase | Owns |
|------|-------|------|
| Chief | Route / collect | Assignment packets, ACTION_LOG collect |
| Analyst | Analysis | Research packs, cited briefs |
| Product Manager | Planning | PRD / process / bus docs |
| Architect | Solutioning | Architecture spine + SPEC |
| Developer | Implementation | Story packets + code via Build/Cloud Agent |

**Extended (idle until bottleneck):** UX Designer · QA · Tech Writer · Verifier — see `roster/extended/`

Operator = the human. Far-end services see the Operator's identity.

## Process map (optional)

Map work to phases if it helps. Chief routes; owners produce Artifacts.

```
Analysis → Planning → Solutioning → Implementation
 Analyst      PM        Architect      Developer
```

Skip phases when intent and Artifacts already cover them. See Skill `chief-phase-skip`.

## Hire only for recurring bottlenecks

Hire only for a recurring, evidenced bottleneck — not because a role name sounds useful.

1. Log pain in [docs/BOTTLENECKS.md](docs/BOTTLENECKS.md)
2. Require **Times seen ≥ 2** (or Operator explicit assign)
3. Prefer waking idle Extended over CreateAgent
4. Keep Routines at **0** until a Skill has two clean earn runs

## Hard limits (shared computer)

Read [docs/SHARED-COMPUTER.md](docs/SHARED-COMPUTER.md):

1. No dry-run — first run is live  
2. Bot ≠ security boundary  
3. Approvals prevent; they do not reverse  
4. Far end sees you as Operator  

Spend caution: token use and overage are real cost.

## Layout

```
AGENTS.md      Install-now instructions for any Bot
BOOTSTRAP.md   Executable install runbook
docs/          Playbooks + templates + beginner guide + diagrams
roster/        Bot contracts (core + extended)
skills/        Skill stubs (YAML name + description)
workspace/     Empty phase folders for Artifacts
```

## License

MIT — see [LICENSE](LICENSE). Contributions: [CONTRIBUTING.md](CONTRIBUTING.md).
