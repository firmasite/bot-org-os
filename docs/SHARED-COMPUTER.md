# Shared-computer limits

**Separate Bot ≠ security boundary.** Every Bot on an org shares one computer, one workspace, and (when present) the same browser/CLI logins. Audit what exists on the **machine**, not which Bot "owns" it.

Treat the box as a **coworker desk you share** — never as a private vault. Put durable truth in workspace files + VCS + Skills. Never paste tokens into chat, HANDOFF, or ACTION_LOG.

## Four hard limits

1. **No dry-run.** A "test" run still navigates, edits files, and calls tools. First run = live.
2. **Bot ≠ security boundary.** Same computer, files, sessions, and logins for every Bot.
3. **Approvals prevent; they do not reverse.** Sensitive steps can pause for Operator / 2FA, but the session stays live for every Bot after. Auto-review is a model checking a model.
4. **The far end sees you as Operator.** Bots act in the Operator's sessions; far-end logs show the Operator's identity.

## Spend caution

Token use can spike. Treat weekly allowances and overage as real cost. Prefer thin packets and read-mostly Build for research.

## Minimum-access habits

1. Prefer read-only connectors and scoped service accounts.
2. No master personal login for outbound mail/post when a Bot identity exists.
3. Consequential / irreversible actions → human approval (Action gate).
4. Re-audit after any new login, connector, or computer refresh.
5. Bot contracts and Skills are durable; shell history and ephemeral sessions are not source of truth.

See also Skill `irreversible-actions`.
