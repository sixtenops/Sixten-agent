---
name: capture
description: Record something Sixten says in passing — a promise, a request of someone else, a decision, a fact about a person, a priority change — into the right state/ file. Use when Sixten says "remember", "note that", "log", "I promised", "X will send me", "we decided", or pastes meeting notes.
---

# Capture

Route each item to exactly one place:

| What | Where | Format |
| --- | --- | --- |
| Sixten promised something | `state/commitments.md` → Open | `- [ ] DUE \| me -> Who \| what \| source` |
| Someone promised Sixten | `state/commitments.md` → Open | `- [ ] DUE \| Who -> me \| what \| source` |
| A decision | `state/decisions.md` (top) | the template in that file |
| Fact about a person | `state/people.md` | add to their section; create one if needed |
| Priority change | `state/priorities.md` | edit, and note the old one under "Not now" if parked |
| Preference / rule | `state/preferences.md` | the matching section |

Rules:
- Resolve relative dates ("Friday", "next week") to an absolute date in Sixten's
  timezone. "Next week" with no day → that Friday. No date given → `????-??-??`
  and ask once if it matters.
- For meeting notes: extract every action item with an owner. Ambiguous owner →
  list it and ask.
- Run `python3 bin/loops` afterwards to confirm the line parses (no warnings).
- Confirm in one line per item: `Logged: <what> → <file>`.
- Commit and push.
