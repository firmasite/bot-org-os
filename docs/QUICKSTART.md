# Quick start

New to this template? Read [BEGINNER.md](BEGINNER.md) and the [diagrams](diagrams/) first.

## Preferred path — paste the repo link

Send this URL to any Bot that can create agents and install Skills:

`https://github.com/firmasite/bot-org-os`

That Bot reads [`AGENTS.md`](../AGENTS.md) and runs [`BOOTSTRAP.md`](../BOOTSTRAP.md). Linking is the install trigger. Success = Core Bots, Skills, playbooks on the bus, Core Team channel, `workspace/org/INSTALL-STATUS.md`, and a short Operator summary.

Use the manual steps below **only if** Bootstrap tools are missing (no CreateAgent, no Skills library access, or cannot fetch the repo).

## Manual fallback (tools missing)

1. Read [PRIMITIVES.md](PRIMITIVES.md) and [SHARED-COMPUTER.md](SHARED-COMPUTER.md).
2. Create **Chief** from [../roster/chief.md](../roster/chief.md). Paste contract into the Bot.
3. Create core specialists: Analyst, Product Manager, Architect, Developer.
4. Install Skills from `skills/*/SKILL.md` (start with `install-from-repo`, `chief-of-staff`, `work-gate`, `irreversible-actions`).
5. Copy [HANDOFF.template.md](HANDOFF.template.md) into your handoffs folder; copy playbooks into `workspace/org/`.
6. Open [BOTTLENECKS.md](BOTTLENECKS.md) — keep Extended idle; freeze CreateAgent.
7. Create a **Core Team** group with Chief + the four specialists.
8. Run one small job: Chief assigns → specialist writes Artifact under `workspace/<phase>/` → HANDOFF with three gates → Chief collects → append ACTION_LOG.

## Definition of first success

- One closed Artifact + HANDOFF on the bus  
- Chief did **not** write the specialist Artifact  
- No new Bot created beyond Core  
- No Routine created  

Repeat once more. Then consider Skill earn tags. Routines only after two clean earns.
