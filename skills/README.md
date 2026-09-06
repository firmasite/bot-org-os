# Skills

Each folder is a Skill stub: `SKILL.md` with YAML frontmatter `name` + `description` ("use this when …") and a short actionable body.

## Install

**Preferred:** paste [`INSTALL-PROMPT.md`](../INSTALL-PROMPT.md) into any new Bot — Bootstrap installs every Skill (including `install-from-repo`). A bare GitHub URL is not enough.

Manual:

1. Create a Skill in Grok Bot (shared org Skills).
2. Paste the `SKILL.md` contents (keep frontmatter).
3. Tag earn status in your live org: `earned` only after two clean consequential uses with HANDOFF/ACTION_LOG evidence. Porting ≠ earning.
4. **Routines only after** a Skill is earned twice.

## Included stubs

| Skill | Use when |
|-------|----------|
| install-from-repo | Operator pastes INSTALL-PROMPT or asks to install — run BOOTSTRAP.md |
| chief-of-staff | Coordinating as Chief |
| work-gate | Starting consequential work with Operator |
| chief-phase-skip | Routing / skipping optional phase steps |
| irreversible-actions | Undoability line for FORBIDDEN / Action gate |
| memory-policy | Writing or reading Bot memory |
| worker-routing | Choosing Bot vs Build vs Cloud Agent |
| second-opinion | Before calling work done or choosing one plan |
| grok-build-execution | Delegating heavy work to `grok -p` |

Adapt paths to your workspace. Strip any private host details if you fork from a private org.

## Ported Claude-style ops (live workflows)

| Skill | When |
|-------|------|
| `failure-report` | Broken build / failed command / bad page — four-part format |
| `library-docs` | Before calling outside packages — fetch real docs |
| `developer-story-packet` | Closed coding task packet for Developer / Grok Build |

These are public stubs for common ops workflows. Earn ≠ install.
