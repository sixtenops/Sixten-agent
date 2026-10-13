---
name: end-of-day
description: Shutdown routine — reconcile what got done against the morning plan, close loops, capture loose ends, and set up tomorrow (prep for tomorrow's meetings, proposed top 3). Use when Sixten says "wrap up", "end of day", "shutdown", "what's left", or on the evening schedule.
---

# End of day

1. Read today's `briefs/YYYY-MM-DD-morning.md`. For each of "Today's 3", ask or
   infer (from sent mail, edited docs, calendar) whether it's done.
2. Sent mail today: capture any new promises Sixten made (→ `capture` rules).
3. Run `follow-ups`.
4. In `state/commitments.md`, move `- [x]` items from Open to the top of Archive
   with today's date appended.
5. Tomorrow: list meetings; run `meeting-prep` for each that needs it. Flag
   conflicts and anything that needs a decision before the first meeting.
6. Propose tomorrow's top 3 (carry over unfinished ones only if still important —
   say if something has carried over 3+ days).

Write `briefs/YYYY-MM-DD-end-of-day.md`:

```
## Done today
## Carried over (and why)
## Loops closed / nudges drafted
## Tomorrow
- First meeting: ...
- Proposed top 3: ...
- Decide before morning: ...
```

Keep it short. Commit and push.
