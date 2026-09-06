# Single bus rule

Chat is control. Files are the bus. Write durable work under agreed roots only.

## Allowed write roots

| Root | Use |
|------|-----|
| `workspace/analysis/` | Research / recon packs |
| `workspace/planning/` | PRD / process / stories |
| `workspace/solutioning/` | Architecture / SPEC |
| `workspace/implementation/` | Build packets / code notes |
| `workspace/handoffs/` | Live HANDOFF mirror |
| `workspace/org/` | Org OS: playbooks, ACTION_LOG, audits |

Do not invent new top-level durable trees for consequential work.

## HANDOFF required fields

| Field | Meaning |
|-------|---------|
| TASK | Closed ask |
| STATUS | `complete` / `partial` / `blocked` |
| OUTPUT | Exact Artifact paths |
| SOURCES | What was read |
| DECISIONS | Choices locked this close |
| UNCERTAINTIES | Open items — do not invent answers |
| NEXT OWNER | Who collects or acts next |
| DO NOT ASSUME | Explicit non-goals |

## Three gates (every close)

| Gate | Question |
|------|----------|
| **Source** | Required inputs from approved sources? PASS / FAIL |
| **Evidence** | Claims tagged or backed by files? PASS / FAIL / N/A |
| **Action** | Send / publish / purchase / prod? NONE / PENDING / APPROVED |

## Definition of done

- [ ] Artifact under an allowed root  
- [ ] HANDOFF filled  
- [ ] Three gates filled  
- [ ] ACTION_LOG appended when consequential  
- [ ] NEXT OWNER named (usually Chief)  
