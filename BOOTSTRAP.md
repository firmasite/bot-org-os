# BOOTSTRAP — install Bot Org OS

Executable install runbook. When the Operator asks to install/setup/bootstrap Bot Org OS (see INSTALL-PROMPT.md), run these steps **now**. Do not ask "want me to install?" or "clone vs review vs setup?".

---

## Step 0 — Fetch this repo

Prefer:

```bash
gh repo clone firmasite/bot-org-os
```

into the shared workspace (or clone into an existing org root if already mapped).

Alternatives if `gh` differs or is missing:

- Read files via GitHub raw URLs or `gh api repos/firmasite/bot-org-os/contents/...`
- Use whatever fetch/clone tools this account has

If tools differ, adapt — still obtain the full tree (especially `docs/`, `roster/`, `skills/`, `workspace/`).

Record the local clone/read root; later steps use it as `$REPO`.

---

## Step 1 — Create Artifacts folders

Create (or map to the account's real Artifact roots):

```
workspace/{org,analysis,planning,solutioning,implementation,handoffs}/
```

If the product already has Artifact roots, map these phase names onto them. Document the **chosen live paths** in STATUS (Step 7).

---

## Step 2 — Copy playbooks

Copy all `$REPO/docs/*.md` into `workspace/org/` (playbooks live there).

Overwrite by filename if updating an existing install.

---

## Step 3 — Install Skills

Install every Skill under `$REPO/skills/*/SKILL.md` into the account Skills library (create or **overwrite by name**).

Include the new **`install-from-repo`** Skill so future paste-of-URL installs stay automatic.

Keep YAML frontmatter. Tag earn status later in the live org — porting ≠ earning.

---

## Step 4 — Become Chief, then CreateAgent specialists

1. **Become Chief** — the installing Bot must become Chief. Rename itself. Set the description from `roster/chief.md` (profile update / equivalent). Do **not** CreateAgent a Chief. Never CreateAgent a second Chief.
2. **CreateAgent only for Analyst, Product Manager, Architect, Developer.** Use their roster contracts. Set **name** + **description** from each contract.

Do **not** auto-create Extended bots on first install (`roster/extended/` stays documented idle). Wake them only via `docs/BOTTLENECKS.md`.

If a specialist already exists with the same name, update its contract. Do not duplicate.

---

## Step 5 — Core Team channel

Create a group chat/channel named **Core Team** with:

- The installing Bot (now Chief)
- Analyst
- Product Manager
- Architect
- Developer

Skip an Extended channel until BOTTLENECKS allows a wake.

---

## Step 6 — Orient Core Team

Right after the channel exists, Chief briefs every specialist on how the org works.

1. **Post into Core Team** a short working-system brief covering:
   - Who is Chief vs who owns each phase (Analyst → analysis, Product Manager → planning, Architect → solutioning, Developer → implementation)
   - Chat is control; files are the bus (`workspace/{analysis,planning,solutioning,implementation,handoffs,org}/`)
   - Close rule: Artifact path + HANDOFF + three gates (Source / Evidence / Action). No chat-only substantial handoffs
   - Contracts at `workspace/org/roster/`; playbooks at `workspace/org/` (start: `BUS-RULE.md`, `ARTIFACTS.md`, `BOTTLENECKS.md`)
   - Stay in JOB; escalate to Chief for judgment, permission, or missing fact; wait for routed work — do not invent jobs
   - No new Bots/Routines except via BOTTLENECKS / earn rules; Extended stays idle
2. **Also SendToAgent each specialist 1:1** with the same brief (or a one-line pointer). Group posts alone are not enough — specialists must get a direct wake.
3. Tell each specialist their **first message in Core Team** must introduce themselves: name + phase they own + one line they will follow Artifact+HANDOFF (example: `Analyst — I own Analysis. I will follow Artifact+HANDOFF.`). Intros belong **in Core Team** (visible to the Operator). Use 1:1 for the wake/brief only — do **not** tell specialists to ack only in 1:1 (that leaves the room empty). Do not wait forever; note missing intros in STATUS and move to Operator welcome.

Do this **before** the Operator day-one welcome so the roster is warm when the first job lands.

---

## Step 7 — Write STATUS

Write `workspace/org/INSTALL-STATUS.md` listing:

- This Bot as Chief (renamed); specialists created or updated (names)
- Skills installed (names)
- Artifact / playbook paths chosen
- Open items (missing tools, Operator taps needed, Extended still idle)

---

## Step 8 — Tell the Operator

Day-one is a **beginner welcome**. One short message.

1. **Introduce yourself** as Chief in first person: you coordinate the Core Team; you route and close; you pick owners — the Operator does not.
2. Briefly what exists: Analyst, Product Manager, Architect, Developer; Skills; playbooks path; Core Team. Link worked — install finished (or partially finished; see STATUS).
3. Soft tip (one short line): Right-click **Chief** in the Grok Bot sidebar → **Pin**.
4. End like meeting someone — warm and ready — not an intake form. One human invite line is fine ("What's on your plate?" / "What should we start with?"); never a routing prompt.

**Forbidden** as the day-one close: a routing menu, "what should I route", owner pickers, thin-loop widgets, "suggest next thin job" as a routing prompt, or leading with a cold interrogative instead of introducing yourself. Guide the Operator. Pick owners yourself. Do not dump specialist routing on beginners.

---

## Failure modes

| Problem | What to do |
|---------|------------|
| **Missing CreateAgent** (or equivalent) | Still **become Chief** (rename + description). Create Skills + copy docs into `workspace/org/` only. Write STATUS naming which specialist Bot steps need Operator taps. Tell Operator clearly. |
| **Rate limits / mid-run stop** | Resume from `workspace/org/INSTALL-STATUS.md` — skip completed rows. |
| **Cannot fetch repo** | Ask Operator for a workspace path that already has the tree, then continue from Step 1. |
| **Irreversible choice** (public publish, delete, spend) | Stop and ask; Bootstrap does not auto-approve those. |

---


---

## Optional tools (not required for install success)

Core success = folders + playbooks + Skills + this Bot as Chief + four specialists + Core Team + Core Team orientation (channel + 1:1) + STATUS + Operator welcome.

Do **not** block install on these. Operator may add later (see `docs/OPTIONAL-TOOLS.md`):

- [ ] Grok Build (`grok` CLI) — Developer execution engine (not a Bot)
- [ ] GitHub CLI (`gh`) — clone/fetch; optional if tree is already local
- [ ] Cloud Agents / coding agents — optional for repo work
- [ ] Other connectors — only after a logged bottleneck

## After install

- Hire only for a recurring, evidenced bottleneck — not because a role name sounds useful. See `docs/BOTTLENECKS.md`.
- **Become Chief** is the rule. This installing Bot is Chief. Do not treat "hand off to Chief" as an equal default. Do not DIY specialist product work when an owner exists.
- Routines stay at **0** until a Skill has two clean earn runs.
