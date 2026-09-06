# Workspace (Artifacts bus)

Empty phase folders for durable work. Point your live org here (or copy the layout).

| Folder | Phase / use | Typical owner |
|--------|-------------|----------------|
| `analysis/` | Research / recon | Analyst |
| `planning/` | PRD / process / stories | Product Manager |
| `solutioning/` | Architecture / SPEC | Architect |
| `implementation/` | Story packets / build notes | Developer |
| `handoffs/` | Live HANDOFF mirror | All → Chief collects |
| `org/` | Org OS copies (ACTION_LOG, audits) | Chief / PM |

See `docs/ARTIFACTS.md` and `docs/BUS-RULE.md`.

`.gitkeep` files keep empty dirs in git. Your `.gitignore` may ignore local content under `workspace/**` except keepers — adjust if you want phase Artifacts versioned.
