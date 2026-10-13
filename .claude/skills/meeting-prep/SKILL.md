---
name: meeting-prep
description: Write a one-page brief for an upcoming meeting — who's attending, history with them, open loops, what Sixten wants out of it, and suggested talking points. Use when Sixten says "prep me for", "brief for my meeting with", "what do I need to know before", or for all of tomorrow's meetings during end-of-day.
---

# Meeting prep

Input: a meeting (name, time, or "next" / "tomorrow's"). Look it up on the calendar.
Skip prep for focus blocks, personal events, and recurring 1:1s with nothing new
since last time — say "no prep needed" instead.

## Gather
- Event: title, time, attendees, description, attached docs (read them).
- For each external or infrequent attendee: their entry in `state/people.md`, the
  last 3 email threads with them, and the last meeting with them on the calendar.
- `state/commitments.md`: anything owed either way with these people.
- Notion / Drive: docs mentioning the meeting topic or attendees in the last 30
  days.

## Write `briefs/YYYY-MM-DD-prep-<slug>.md`

```
# <Meeting> — <time>
**Goal for Sixten:** <one sentence — infer from priorities; mark (inferred)>
**Attendees:** Name (role) — one line of context each

## Since last time
- ...
## Open loops with them
- You owe: ... / They owe: ...
## Talking points
1. ...
## Likely asks of you
- ... → suggested answer
## Watch out for
- ...
```

One page max. If there's no agenda and Sixten organised it, draft a 3-line
agenda for Sixten to send. After the meeting, if Sixten shares notes, run
`capture` on them.
