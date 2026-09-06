# Artifacts bus

| Kind | Path (template layout) |
|------|------------------------|
| Phase work | `workspace/{analysis,planning,solutioning,implementation}/` |
| Handoffs | `workspace/handoffs/HANDOFF.md` (+ per-job HANDOFF next to Artifact) |
| Org OS | `workspace/org/` (playbooks, ACTION_LOG, audits) |
| Action log | One file only — see ACTION-LOG.md |

## Close requirements

Every Bot close needs:

1. **Artifact path** under the bus roots above  
2. **HANDOFF** with required fields + **three gates** (source, evidence, action)  
3. Consequential runs appended to ACTION_LOG  

Chat-only substantial handoffs are refused. Party debate may inform; the file wins.
