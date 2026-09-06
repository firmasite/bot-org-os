---
name: Developer story packet
description: >-
  Use this when packaging a closed coding task for Developer / Grok Build —
  five-part packet, accept via real diff + success command, two failed rounds
  stop.
---
# Developer story packet

Use this before any Grok Build or Cloud Agent coding task. Prefer wrapping the session in [BMAD build](sand-workflow:bmad-build) when the work is a feature/story/bug.

## Required packet fields
1. **Goal** — one sentence outcome
2. **Files allowed to change** (in-scope paths)
3. **Limits** — what must not change
4. **Success command** — exact command + expected result
5. **Answer format** — HANDOFF / Build return shape

Also: story id, acceptance criteria, SPEC/story pointers (`/workspace/bmad/solutioning/specs/...` when present), Build invocation, human-approval flag, three gates on close.

Template: `/workspace/bmad/planning/story-packet-template.md`

## Invoke
```
grok -p --cwd <workdir> --reasoning-effort high "<closed task>"
```
One story / one Build session. Ambiguous packet → stop and escalate.

## Accept
1. Real diff (`git status` / `git diff`)  
2. Run success command yourself  
3. If you wrote part of the code, [Second opinion](sand-workflow:second-opinion) / [BMAD review](sand-workflow:bmad-review)

## Limits
One writer at a time · two failed rounds stop · candidate complete ≠ done · no permanent tests unless asked · [Irreversible actions](sand-workflow:irreversible-actions) · [Library docs](sand-workflow:library-docs) before unfamiliar APIs.

## After
HANDOFF with three gates. ACTION_LOG if consequential.
