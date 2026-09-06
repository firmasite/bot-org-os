---
name: Grok Build execution
description: >-
  Use when a Grok Bot should delegate heavy reasoning, structured analysis,
  critique, or coding to the Grok Build CLI (grok -p) instead of doing it
  itself.
---
# Grok Build execution

Grok Bot orchestrates. Grok Build executes. **Do not** create a specialist Bot whose only job is "run grok."

## Preconditions

- Build CLI installed and on `PATH`
- Authenticated via device login — never paste tokens into chat or logs
- Check available models before expensive runs

## When to use

Closed, expensive work where a Bot owns the outcome:

- Coding / patches — Developer story packets
- Research synthesis — Analyst owns evidence gates
- Critique / review — independence controls (Verifier)
- Structured analysis — schema + prompt file for machine-checkable output

Mechanical extract/format/moves stay on the Bot. Chat-of-record and HANDOFF stay on the Bot.

## Headless defaults

- Closed task + acceptance criteria + allowed paths
- Prefer prompt files over huge argv; no secrets on the command line
- Prefer structured output; treat missing cost fields as **unknown**, not free
- Always-approve only if fully sandboxed (no send/publish/purchase/delete/prod)
- After finish: Bot writes HANDOFF (what ran, Artifacts, unverified)

## Role patterns (short)

| Owner | Pattern |
|-------|---------|
| Analyst | Read-mostly; deny edit tools; Bot authors HANDOFF |
| Verifier | Fresh session; edits denied; pass/fail + citations |
| Developer | Coding via packet; still owns merge decisions |

## Three gates

Build does not bypass source, evidence, or action. Irreversible steps stop for Operator approval.
