# Contributing

Thanks for improving this public template.

## Rules

1. **No personal data.** No real names, emails, hostnames, private paths, tokens, or product internals.
2. **Keep roles generic.** Operator, Chief, Analyst, Product Manager, Architect, Developer; optional Extended only.
3. **Short STE-like English.** Prefer short sentences and tables.
4. **Docs + stubs only.** This is not a runnable app server.
5. **MIT.** By contributing you agree your changes are MIT-licensed.
6. **Linking installs.** Keep `AGENTS.md` + `BOOTSTRAP.md` accurate so pasting the repo URL remains a valid install order.
7. **Hire policy language.** Prefer: hire only for a recurring, evidenced bottleneck — not because a role name sounds useful. Avoid third-party attribution name-drops.

## How to change things

- New playbook → `docs/`
- New Bot role → `roster/` (or `roster/extended/`)
- New Skill stub → `skills/<slug>/SKILL.md` with YAML `name` + `description`
- Install behavior → `AGENTS.md`, `BOOTSTRAP.md`, `skills/install-from-repo/`
- Update `README.md` links when you add a primitive or install step

## Before you open a PR

Scan for private or personal strings (names, mail hosts, machine paths, tokens) and for third-party brand leftovers. Prefer inventing clean public examples over pasting from a private org. Remove anything that could identify a private machine or person.
