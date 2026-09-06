---
name: Developer story packet
description: >-
  Use this when packaging a closed coding task for Developer / Grok Build —
  five-part packet, accept via real diff + success command, two failed rounds
  stop.
---
# Developer story packet

Use this before any Grok Build or Cloud Agent coding task.

## Required packet fields
1. **Goal** — one sentence outcome
2. **Files allowed to change** (in-scope paths)
3. **Limits** — what must not change
4. **Success command** — exact command + expected result
5. **Answer format** — HANDOFF / Build return shape

Also: story id, acceptance criteria, SPEC/story pointers under `workspace/solutioning/` or `workspace/planning/` when present, Build invocation, human-approval flag, three gates on close.

Write the packet as an Artifact under `workspace/planning/` or `workspace/implementation/`.

## Invoke
```
grok -p --cwd <workdir> --reasoning-effort high "<closed task>"
```
One story / one Build session. Ambiguous packet → stop and escalate.

## Accept
1. Real diff (`git status` / `git diff`)
2. Run success command yourself
3. If you wrote part of the code, use the **Second opinion** Skill

## Limits
One writer at a time · two failed rounds stop · candidate complete ≠ done · no permanent tests unless asked · **Irreversible actions** Skill · **Library docs** Skill before unfamiliar APIs.

## After
HANDOFF with three gates. ACTION_LOG if consequential.
