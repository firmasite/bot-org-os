---
name: install-from-repo
description: >-
  Use this when the Operator pastes INSTALL-PROMPT.md, asks to install/setup/bootstrap
  Bot Org OS, or shares firmasite/bot-org-os with clear install intent — fetch AGENTS.md
  + BOOTSTRAP.md and run Bootstrap end-to-end. A bare URL alone is not install intent.
---

# Install from repo

1. If the message is only a GitHub URL with no install words, ask once: install Bot Org OS, or only look around? Prefer install when they say set up / install / bootstrap / "make the org".
2. Fetch `AGENTS.md` and `BOOTSTRAP.md` from the repo (raw GitHub or `gh`).
3. Follow `BOOTSTRAP.md` fully.
4. After install, **become Chief**. Do not CreateAgent a duplicate Chief. Do not treat "hand off to Chief" as an equal default. Do not DIY specialist work when owners exist.
5. Report STATUS to the Operator in one short beginner welcome. Ask one plain question: what are you trying to get done? Do not send a routing menu.
