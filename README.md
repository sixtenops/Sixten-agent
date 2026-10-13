# Sixten-agent — Chief of Staff

A chief of staff built on Claude Code. It reads your mail, calendar, Drive and
Notion through connectors, keeps a memory of priorities, people and promises in
plain markdown files, and runs a daily and weekly operating rhythm. It **drafts**
emails and **suggests** calendar changes; it never sends, accepts or deletes
anything without asking.

## Getting started

Open a Claude Code session on this repo (with the Gmail and Google Calendar
connectors enabled) and say:

> onboard me

It scans the last two weeks of mail and calendar and asks you about six
questions, then fills in `state/`.

## Daily use

| Say | Routine |
| --- | --- |
| "brief me" / "morning" | `morning-brief`: today's plan, triaged inbox, due items, top 3 |
| "triage my inbox" | `inbox-triage`: sorts mail, drafts replies, logs promises |
| "prep me for my 2pm" | `meeting-prep`: one-page brief per meeting |
| "remember I promised Alex the deck by Friday" | `capture`: logs it in the right file |
| "who owes me what?" | `follow-ups`: closes delivered items, drafts nudges |
| "wrap up" | `end-of-day`: closes loops, preps tomorrow |
| "weekly review" | `weekly-review`: scorecard, time audit, next week's top 3 |

## Layout

```
CLAUDE.md                 role, authority limits, operating rules
.claude/skills/*/SKILL.md the routines above
state/                    memory: priorities, commitments, people, preferences, decisions
briefs/                   dated output of every routine (history)
bin/loops                 computes overdue / due-soon items from state/commitments.md
```

`bin/loops` uses only the Python standard library: `python3 bin/loops [--days N] [--json]`.

## Running it on a schedule

Each routine can run as a scheduled Claude Code Routine (for example
`morning-brief` at 07:45 on weekdays, `end-of-day` at 17:15, and `weekly-review`
on Friday afternoon). Its output lands in `briefs/` and Gmail Drafts.
