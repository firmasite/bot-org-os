---
name: install-from-repo
description: >-
  Use this when the Operator pastes a Grok Bot Organization OS repo URL
  (e.g. firmasite/GrokBot) or asks to stand up the org from GitHub —
  run BOOTSTRAP.md end-to-end.
---
# Install from repo

## Detect

Trigger when the Operator:

- Pastes a GitHub URL for this template (e.g. `https://github.com/firmasite/GrokBot`) or an equivalent fork
- Says to stand up / install / bootstrap the org from GitHub
- Shares this repository's contents as an install source

Treat the paste as an **install order**. Do not ask "want me to install?"

## Run

1. **Fetch** the repo (prefer `gh repo clone firmasite/GrokBot`, or raw/`gh api`, or the account's fetch tools).
2. **Follow** root [`BOOTSTRAP.md`](../../BOOTSTRAP.md) end-to-end (Steps 0–7).
3. **Write** `workspace/org/INSTALL-STATUS.md` and tell the Operator what exists.

## After install

- Do **not** DIY specialist product work (research, PRD, architecture, coding) when Core owners exist.
- Become **Chief**, or hand off to the Chief Bot you just created/updated.
- Further hire / Extended wake only via `docs/BOTTLENECKS.md`.

## Failure

If CreateAgent is missing, install Skills + docs only and list Operator taps in STATUS. If rate-limited, resume from STATUS.
