---
name: Irreversible actions
description: >-
  Use this when defining Bot FORBIDDEN rules or deciding whether a Bot may
  finish alone vs park for approval — undoability line
  (send/publish/money/delete/prod).
---
# Irreversible actions

The line is not size of task. It is whether the action can be undone.

## Finish alone (reversible)

Drafting, researching, filing, tagging, preparing, summarizing, organizing files under the workspace, local notes. Complete and report back.

## Park for Operator approval (irreversible / outward)

Default block list — paste into Bot FORBIDDEN / contracts:

- Never send an external message without approval
- Never publish, post, or share publicly
- Never move, transfer, or spend money
- Never delete anything permanently (or destroy work that cannot be recovered)
- Never change production without approval

When hit: park the action, notify the Operator, wait. Do not invent a workaround.

## Shared computer

Separate Bots are not a security boundary. Credentials and sessions are shared. Prefer scoped identities and read-only access where possible. See `docs/SHARED-COMPUTER.md`.

## Relation to three gates

This Skill is the Action gate in plain language. Source and Evidence still apply. Use Work gate before starting new consequential work the Operator asked for.
