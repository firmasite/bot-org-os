# Bot Org OS — beginner guide

This guide explains the system in plain language.
Read this page and the three diagrams first.
You do not need other docs to understand the idea.

**Product name:** Bot Org OS  
**Repo slug:** `bot-org-os`  
**Paste-link install:** `https://github.com/firmasite/bot-org-os`

This template is for use with Grok Bot. It is not affiliated with SpaceXAI and is not an official product.

---

## What this is

Bot Org OS is a **public template**.
It is a set of folders, role contracts, Skills stubs, and playbooks.

You paste the repo URL into a Bot.
That Bot reads `AGENTS.md` and `BOOTSTRAP.md` and installs the org layout.
**Linking is the install trigger.**

After install you get:

- A **Chief** Bot that routes work
- Four **phase specialists** (Analyst, Product Manager, Architect, Developer)
- Shared **Skills** and empty **Artifact** folders
- A **Core Team** group chat

Extended roles stay idle until a real bottleneck appears.

---

## Human vs Bot

| Who | Role |
|-----|------|
| **Human (Operator)** | You. You set goals, approve irreversible acts, and own far-end identity. |
| **Bot** | A persistent assistant with a named job and a contract. |

**Operator** — the human who owns the account and the work.  
Far-end services (email, GitHub, spend) see the Operator, not the Bot name.

**Bot** — a durable role (Chief, Analyst, …). Bots share tools and Skills. Each Bot keeps its own memory and Routines.

A Bot is **not** a security boundary. Approvals stop bad first moves; they do not undo damage already done.

---

## Chief vs specialists

**Chief** — coordinator only. Triage, assign, watch handoffs, collect results, escalate to you. Chief does **not** write specialist product Artifacts when an owner exists.

**Specialists** — own one phase lane:

| Role | Phase | Typical Artifact |
|------|-------|------------------|
| Analyst | Analysis | Research / brief |
| Product Manager | Planning | PRD / process docs |
| Architect | Solutioning | Architecture + SPEC |
| Developer | Implementation | Story packet + code via Build tools |

**Extended** (idle until hired for a bottleneck): UX Designer, QA, Tech Writer, Verifier.

See diagram: [roster-map.md](diagrams/roster-map.md).

---

## Skills vs one-shots vs Routines

These are three kinds of **prompts**:

| Kind | Meaning | When to use |
|------|---------|-------------|
| **One-shot** | A prompt you use once | Ad-hoc ask; no need to reuse |
| **Skill** | A saved reusable recipe (shared across Bots) | Same multi-step job appears more than once |
| **Routine** | A Skill-like job on a **schedule or event** | Only after a Skill earned clean runs twice |

**Earn** — mark a Skill ready only after two clean real uses. Porting a stub from this repo is not the same as earning it.

Keep Routines at **zero** until earn is real. Do not create Routines for “maybe later.”

---

## Artifacts bus

**Artifact** — a durable file that is the source of truth for a piece of work. Chat is for control; files are the bus.

Phase folders (template layout):

```
workspace/analysis/
workspace/planning/
workspace/solutioning/
workspace/implementation/
workspace/handoffs/
workspace/org/          ← playbooks, ACTION_LOG, install status
```

Rules:

1. Substantial work lands as a file under the bus, not only in chat.
2. Closing a job needs an Artifact path **and** a HANDOFF.
3. One ACTION_LOG file records consequential closes.

See diagram: [artifact-bus.md](diagrams/artifact-bus.md).  
More detail: [ARTIFACTS.md](ARTIFACTS.md), [BUS-RULE.md](BUS-RULE.md).

---

## HANDOFF three gates

**HANDOFF** — a short close-out file that says what was done, what sources were used, and what must not be assumed.

Every close needs these **three gates**:

| Gate | Question |
|------|----------|
| **Source** | Did required inputs come from approved authoritative sources? |
| **Evidence** | Are important claims marked VERIFIED / INFERRED / UNKNOWN? |
| **Action** | Does any send / publish / purchase / prod change need Operator approval? |

Template: [HANDOFF.template.md](HANDOFF.template.md).

Chief collects HANDOFFs. If Action is PENDING, work stops until you approve.

---

## Paste-link install

1. Send this URL to any Bot that can create agents and install Skills:  
   `https://github.com/firmasite/bot-org-os`
2. That Bot reads `AGENTS.md` and runs `BOOTSTRAP.md` **now**.
3. Success = Core Bots + Skills + playbooks on the bus + Core Team channel + `workspace/org/INSTALL-STATUS.md` + a short note to you.

See diagram: [install-flow.md](diagrams/install-flow.md).  
Manual fallback (tools missing): [QUICKSTART.md](QUICKSTART.md).

---

## First success (after install)

1. Ask Chief for one small job.
2. Chief assigns one specialist.
3. Specialist writes an Artifact under `workspace/<phase>/`.
4. Specialist closes with a HANDOFF (three gates).
5. Chief collects. Append ACTION_LOG if consequential.

Do **not** hire a new Bot or create a Routine on the first job.

---

## Diagrams

| Diagram | Shows |
|---------|--------|
| [roster-map.md](diagrams/roster-map.md) | Core Team + Extended idle |
| [install-flow.md](diagrams/install-flow.md) | Paste URL → Bootstrap → Bots / Skills / folders |
| [artifact-bus.md](diagrams/artifact-bus.md) | Phases + HANDOFF loop |

---


## Optional tools

Core install does **not** need extra CLIs or connectors.

Optional (you choose):

1. **Grok Build** (`grok` CLI) — heavier coding/reasoning for Developer packets. Not a Bot.
2. **GitHub CLI (`gh`)** — clone from GitHub. Skip if you paste files another way.
3. **Cloud Agents / coding agents** — optional for repo work.
4. **Other connectors** — only when a bottleneck appears.

Full checklist: [OPTIONAL-TOOLS.md](OPTIONAL-TOOLS.md).

## Where to go next

| Need | File |
|------|------|
| Install now | [`../AGENTS.md`](../AGENTS.md), [`../BOOTSTRAP.md`](../BOOTSTRAP.md) |
| Shared-computer limits | [SHARED-COMPUTER.md](SHARED-COMPUTER.md) |
| When to hire | [BOTTLENECKS.md](BOTTLENECKS.md) |
| Five primitives table | [PRIMITIVES.md](PRIMITIVES.md) |
