# Bot Org OS

A public template for a Chief + phase specialists Bot organization. For use with Grok Bot. Not affiliated with SpaceXAI / not an official product.

## Install (one paste)

**Copy this whole block** into any new Bot. That Bot will **become Chief**.

```
Install Bot Org OS now from https://github.com/firmasite/bot-org-os

Do this without asking what I want (install is the ask):
1. Fetch AGENTS.md + BOOTSTRAP.md (and roster/, skills/, docs/) via GitHub raw or gh.
2. Follow BOOTSTRAP.md end-to-end. Become Chief. Do not CreateAgent a duplicate Chief. CreateAgent only for Analyst, Product Manager, Architect, Developer.
3. Tell me what you created in one short beginner welcome: introduce yourself as Chief, say what exists, tip right-click Chief → Pin, end warmly. Do not send a routing menu.

Do not ask clone vs review vs setup.
```

Same text: [`INSTALL-PROMPT.md`](INSTALL-PROMPT.md). Repo: https://github.com/firmasite/bot-org-os

---

## What you get

- **Chief** — routes work and collects results
- Four **phase specialists** — Analyst, Product Manager, Architect, Developer
- Shared **Skills** and empty **Artifact** folders
- **HANDOFF** gates on every close (Source · Evidence · Action)
- A **Core Team** group chat

Extended roles (UX, QA, Tech Writer, Verifier) stay idle until a real bottleneck appears.

---

## Who is who

**Operator (Human)** — you. You set goals and approve irreversible acts. Far-end services see you.

**Bot** — a persistent assistant with a named job. A Bot is not a security boundary.

**Chief** coordinates only. Specialists own Artifacts. Chief does not write specialist product files when an owner exists.

```mermaid
flowchart LR
  OP[Operator] -->|goals · approvals| CH[Chief<br/>route · collect]
  CH --> SP[Four specialists<br/>Analyst · PM · Arch · Dev]
  SP --> CT[Core Team chat]
  CH -.->|wake via BOTTLENECKS| EX[UX · QA · Writer · Verifier]
  EX -.-> IDLE[Stay idle<br/>until bottleneck]
```


---

## How install works

Paste the INSTALL-PROMPT block into a Bot (not a bare link). That Bot will **become Chief**. It fetches AGENTS.md and runs BOOTSTRAP.md — no second go-ahead. Do not CreateAgent a duplicate Chief.

Bootstrap creates workspace folders, installs Skills, CreateAgent only for Analyst → Product Manager → Architect → Developer, opens Core Team chat (installing Bot as Chief + four specialists), writes INSTALL-STATUS, then a beginner welcome: Chief introduces themself, what exists, Pin tip, warm close. First chat is guided, not a routing menu.

Dashed steps below are branches of the same Bootstrap run. **Optional tools** (dashed) are Operator-chosen after Status — recommend, never require. Extended Bots and Routines are not created on day one.

```mermaid
flowchart LR
  A[Paste INSTALL-PROMPT<br/>bot-org-os] --> B[AGENTS + BOOTSTRAP<br/>install now]
  B -.-> F[workspace/<br/>phase folders]
  B -.-> S[Skills<br/>library]
  B --> C[Chief + 4 specialists<br/>+ Core Team]
  F -.-> I[INSTALL-STATUS<br/>then tell Operator]
  S -.-> I
  C --> I
  I -.-> O[Optional tools<br/>Build · gh · Cloud]
```


---

## How work moves

Chat is control. Files are the bus. An **Artifact** is a durable file under `workspace/<phase>/`. Close needs an Artifact path, a **HANDOFF** with three gates, and ACTION_LOG when consequential.

| Gate | Question |
|------|----------|
| **Source** | Did required inputs come from approved authoritative sources? |
| **Evidence** | Are important claims marked VERIFIED / INFERRED / UNKNOWN? |
| **Action** | Does any send / publish / purchase / prod change need Operator approval? |

```mermaid
flowchart LR
  ASK[Ask] --> ASG[Assign<br/>one owner]
  ASG --> WORK[Phase work]
  WORK --> ART[Artifact<br/>workspace/phase]
  ART --> HO[HANDOFF<br/>3 gates]
  HO --> COL[Collect<br/>ACTION_LOG]
  COL -.->|if needed| GATE[Action gate]
```


---

## Optional tools

Core install works **without** these. Recommend only — never require.

- [ ] **Grok Build** (`grok` CLI) — heavier reasoning/coding for Developer packets. An execution engine, not a Bot.
- [ ] **GitHub CLI (`gh`)** — clone/fetch from GitHub. Optional if you paste files another way.
- [ ] **Cloud Agents / coding agents** — optional for repo work when Developer needs them.
- [ ] **Other connectors** — only when a bottleneck appears. Do not install a zoo on day one.

Duplicate checklist: [`docs/OPTIONAL-TOOLS.md`](docs/OPTIONAL-TOOLS.md).

---

## Shared-computer four limits

1. **No dry-run** — first run is live
2. **Bot ≠ security boundary** — same computer, files, sessions for every Bot
3. **Approvals prevent; they do not reverse**
4. **Far end sees you as Operator**

Spend caution: token use and overage are real cost.

---

## More detail

- [`AGENTS.md`](AGENTS.md) — install-now for Bots
- [`BOOTSTRAP.md`](BOOTSTRAP.md) — executable install runbook
- [`roster/`](roster/) — role contracts
- [`docs/`](docs/) — playbooks (maintainers: Archify sources under docs/diagrams/)

## License

MIT — see [LICENSE](LICENSE).
