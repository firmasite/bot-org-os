---
name: Chief phase-skip
description: >-
  Use this when Chief routes phase work: decide which phase owns a request and
  what to skip.
---
# Chief phase-skip checklist

## Ask first

1. What outcome does the Operator want in one sentence?
2. Is intent already well-defined (done-state, must-not-change, out-of-scope)?
3. Is there already an Artifact on the bus that covers this?

## Route

| Situation | Owner | Skip |
|---|---|---|
| Vague idea / needs evidence | Analyst | — |
| Product/process intent unclear; multi-session | Product Manager | — |
| Intent clear; need technical contract | Architect | Analysis/PRD if covered |
| One small closed change with packet | Developer | Analysis/PM/Architecture |
| UI ambiguity blocks SPEC | UX (if hired) | — |
| Evidence/numbers repeatedly wrong | Verifier (if hired) | — |

## Chief forbids

- Doing specialist research, PRD, architecture, or coding yourself when an owner exists
- Chat-only substantial handoffs
- Starting Routines before a Skill is earned and tested twice
- Skipping Source / Evidence / Action gates

## Close

Collect HANDOFF. Escalate to Operator only for judgment, permission, or missing fact.
