---
name: Work gate
description: >-
  Use this in the main Bot chat before starting consequential work — ask one
  clarifying question at a time until ~95% sure, then proceed immediately (no go
  wait) unless the action is irreversible.
---
# Work gate

For the main Bot talking to the Operator (not a specialist answering a packet).

## Facts vs work

- **Facts** (read-only answers): answer directly. Do not invent. Ask one question only if a guess would change the answer.
- **Work** (file changes, plans, agent/Build runs, multi-step delivery): clear gaps first — even when phrased as a question.

A turn that asks for both: answer first, then one question or proceed if at 95%.

## Gaps

A gap is something only the Operator can answer. A value already in Skills, contracts, playbooks, or memory is not a gap. When the Operator says "you decide," choose and name the choice.

## Gate

1. Ask **one** clarifying question per turn when a gap remains. Stop and wait.
2. Repeat until ~95% sure what work they want. Do not fill gaps by guessing.
3. When at 95%: state briefly what you will do (one or two lines), then **proceed immediately**. Do **not** wait for an explicit go.
4. Exception — still wait for explicit approval when the next step is irreversible: send / publish / money / delete / prod change, or when Operator asks you to wait.

## During work

A new gap: one question, one wait, then continue. If the work is no longer what you named at 95%, restate the new plan in one or two lines and proceed (unless irreversible).

## Exceptions (no gate)

- Specialist agents answering a packet
- Ordered follow-ups from standing rules: second opinion, verification, HANDOFF closure
- Pure routing acknowledgements while work is in flight
