---
name: morning-brief
description: Start-of-day brief — today's calendar with prep notes, triaged inbox, due and overdue commitments, and the 3 things that matter today. Use when Sixten says "morning", "brief me", "what's my day", "start my day", or on the morning schedule.
---

# Morning brief

Read `state/priorities.md`, `state/preferences.md`, `state/commitments.md` first.
If the timezone is unset, ask once and stop. All times in Sixten's timezone.

## Gather
1. `python3 bin/loops --days 2` — overdue and due-soon items.
2. Calendar: today's events, plus anything before 10:00 tomorrow. For each, note
   attendees, whether a doc/agenda is linked, and if Sixten has accepted.
3. Inbox: run the `inbox-triage` procedure (classification only — don't redo it
   in full if it ran in the last 2 hours; reuse its output).
4. Yesterday's `briefs/*-end-of-day.md`, if present, for carry-overs.

## Analyze
- **Conflicts:** overlapping events, back-to-backs without a break, meetings in
  protected focus time, events with no agenda that Sixten owns.
- **Alignment:** what share of today's time serves this week's top 3? If < 30%,
  say so.
- **Today's top 3:** pick from overdue commitments, this week's top 3, and urgent
  mail. Each must be finishable today.

## Output — `briefs/YYYY-MM-DD-morning.md`, and the same content in chat

```
# <Weekday, date>

## Decide / do first
1. ... (why it's urgent — one clause)

## Today's 3
1. ...

## Calendar
- 09:30–10:00 Name — w/ people. Prep: <one line, or "brief ready" / "none needed">
  ⚠ <conflict or issue, if any>
Focus time available: <blocks>

## Inbox (N need you)
- Reply: <sender> — <subject> — draft ready ✅ / needs your input
- FYI: ...

## Open loops
- Overdue (you owe): ...
- Waiting on others: ...

## Heads-up
- <one or two candid observations, or omit>
```

Keep it under one screen. Draft any reply that's obviously needed (Gmail drafts
only). For meetings that need it, run `meeting-prep` and link the brief.
Commit and push the brief file.
