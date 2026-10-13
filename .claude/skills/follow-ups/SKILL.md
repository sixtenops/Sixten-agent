---
name: follow-ups
description: Chase what others owe Sixten and flag what Sixten owes — check each open loop against the inbox, close the ones that were delivered, and draft polite nudges for the ones that are late. Use when Sixten says "follow up", "chase", "who owes me", "what's slipping", or during end-of-day and weekly review.
---

# Follow-ups

1. `python3 bin/loops --json --days 1`.
2. For each open item, search Gmail for the thread or person since the item was
   logged. If it was delivered (attachment, "here you go", a reply that resolves
   it) → mark `- [x]` and note the evidence.
3. **Owed to Sixten, overdue:** draft a nudge (Gmail draft, reply on the original
   thread when there is one). First nudge: friendly, one line, restate the ask
   and a new date. Second nudge (item already notes "nudged"): add why it matters.
   Append `nudged YYYY-MM-DD` to the item's source field.
4. **Sixten owes, overdue or due ≤1 day:** list them with a suggestion — do it now
   (and how long it'll take), draft a "running late, new ETA" note, delegate, or
   drop. Draft the note if that's the suggestion.
5. Undated items older than 2 weeks: ask whether to date, drop, or keep.

Output: `Closed: N` · `Nudges drafted: list` · `You owe (late): list with
suggestion`. Never send the nudges — they wait in Drafts for Sixten.
