# ACTION_LOG hygiene

One log. One path. No secrets.

## One-path rule

Append consequential runs only to your org ACTION_LOG (e.g. `workspace/org/ACTION_LOG.md`).

Do not create alternate ACTION_LOG files under phase folders or chat.

## When to append

Append **one TEMPLATE block** when any of these is true:

- You closed a job with a HANDOFF
- You created or changed durable Artifacts on the bus
- You attempted or completed an external side effect (send, publish, purchase, prod, CreateAgent, install)
- A failure or approval gate mattered for later audit

Do **not** append for pure chat acks with no file change.

## Required TEMPLATE block

```text
---

TIMESTAMP <YYYY-MM-DD HH:MM TZ>
BOT <role name>
TRIGGER <who/what started the run>
REQUESTED OUTCOME <one sentence>
SOURCES ACCESSED <paths or URLs>
FILES CREATED OR MODIFIED <exact paths>
IMPORTANT CLAIMS <facts locked this run>
EXTERNAL ACTIONS ATTEMPTED <or none>
EXTERNAL ACTIONS COMPLETED <or none>
APPROVALS REQUESTED <or none>
APPROVALS RECEIVED <or n/a>
FAILURES <or none>
UNVERIFIED ITEMS <or none>
FINAL STATUS <complete | partial | blocked | in_progress> — <next>
```

## No secrets

Never write passwords, tokens, API keys, cookies, or OTPs. Use redacted pointers (`connector X authenticated`).

## Close checklist

- [ ] Appended to the one ACTION_LOG path only  
- [ ] TEMPLATE fields all present  
- [ ] No secrets  
- [ ] Paths match HANDOFF OUTPUT  
