# Bottlenecks — hire freeze

Hire only for a recurring, evidenced bottleneck — not because a role name sounds useful.

## Policy (freeze)

1. **No new Bots** until Chief ticks the freeze checklist.
2. **Do not wake Extended** (UX Designer, QA, Tech Writer, Verifier) unless a table row has **Times seen ≥ 2** **or** Operator explicitly assigns that specialist.
3. **Routines stay at 0** until a Skill has two clean earn runs.
4. Prefer smallest owner set: Core first, then wake idle Extended, then CreateAgent.

## Standing roster (template)

- **Core (5):** Chief, Analyst, Product Manager, Architect, Developer
- **Extended (4, idle until bottleneck):** UX Designer, QA, Tech Writer, Verifier
- **Routines:** 0 until earned

## Evidence table (copy into your live org)

| Bottleneck | Times seen | Last seen | Evidence path | Proposed owner | Status |
|---|---|---|---|---|---|
| Closed Artifact loop unproven | 0 | — | — | Chief routes · specialists deliver | watching |
| Chief does specialist work when owner exists | 0 | — | — | Chief (self-enforce) — not a new Bot | watching |
| UI/UX ambiguity blocking SPEC | 0 | — | — | UX Designer only if ≥2 | watching |
| Regressions / test debt blocking delivery | 0 | — | — | QA only if ≥2 | watching |
| Docs drift | 0 | — | — | Tech Writer only if ≥2 | watching |
| Claims/numbers fail trust | 0 | — | — | Verifier only if ≥2 | watching |

Do not invent recurrence. Empty Extended wake pain is fine.

## Freeze checklist (before CreateAgent)

Chief must tick **all**:

- [ ] Pain written as a row with **Evidence path**
- [ ] **Times seen ≥ 2** on separate dates/runs **or** Operator explicit assign
- [ ] Proposed owner is a **role bottleneck**, not an app name (no "Mail Bot")
- [ ] Core set cannot absorb it (Chief asked Analyst/PM/Architect/Developer first)
- [ ] Prefer wake existing Extended over CreateAgent
- [ ] No permanent "Build runner" Bot whose only job is to invoke a CLI
- [ ] After create: update roster + ACTION_LOG

## Wake Extended checklist

- [ ] Matching row Times seen ≥ 2 **or** Operator names that Bot
- [ ] Closed assignment packet + Artifact path on the bus
- [ ] HANDOFF required; chat-only handoff refused
- [ ] Append ACTION_LOG when consequential

## Do not

- Wake Extended to "try the Skill"
- Create Routines from unproven Skills
- Count Skill ports as bottlenecks solved
