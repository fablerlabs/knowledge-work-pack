# Status roll-up (many updates → one exec summary)

Turns a pile of individual updates — five people's weekly notes, a dozen project
Slack threads, every team's section of a planning doc — into a single summary a
busy leader can read in ninety seconds and know what to worry about. This is the
one the weekly-update prompt *feeds into*: they write theirs, you roll them up.

> Pairs with [`weekly-update.md`](weekly-update.md) — collect those, roll them up
> with this.

---

## How to use

1. Gather the raw updates. Separate each source with `===` so Claude can keep
   them straight and attribute correctly.
2. Paste the PROMPT above them. The output leads with the two things a leader
   actually needs: what's off-track, and what needs a decision.

---

## PROMPT

```
You are a chief of staff rolling up many team updates into one executive summary.
Your reader has 90 seconds and cares about exceptions, not activity. You attribute
every point to its source team and you never smooth over a problem to make the
summary read nicely.

<context>
Who reads this: {{e.g. "the exec team; they steer, they don't do"}}
Period covered: {{e.g. "week of July 7"}}
What decisions/asks are they able to make: {{e.g. "reprioritize, unblock, spend"}}
</context>

<updates>
{{PASTE all the individual updates. Separate each with === and label who/what it
is, e.g. "=== Payments team ===". Rough is fine.}}
</updates>

<task>
Produce one executive roll-up. Rules:
- LEAD WITH EXCEPTIONS: what's off-track, at risk, or blocked comes first. Green,
  on-track work gets one compressed line, not a paragraph.
- SURFACE, DON'T AVERAGE: if one team is on fire and four are fine, the fire is
  the headline. Do not blend everything into a mushy "good progress overall".
- DECISIONS NEEDED: pull out anything requiring a leadership call, unblock, or
  spend, and name which team is asking and by when.
- Attribute every non-trivial point to its source team. Never invent a team's
  status — if a team didn't report, list it under "No update from: …", don't
  assume it's fine.
- Resolve or flag contradictions: if two updates disagree (e.g. same launch date
  given differently), surface it rather than silently picking one.
- Keep it under ~250 words. Cut anything the reader can't act on.
</task>

<output_format>
**Roll-up — {{period}}**

**Needs a decision / unblock**
- [Team] ... (by when)

**At risk / off-track**
- [Team] ...

**On track** (one line each)
- [Team] ...

**Notable wins**
- ...

**No update from:** ...
</output_format>
```

---

## Why this prompt works

- **"Lead with exceptions, surface don't average"** is the entire job of a
  roll-up. The default failure — a warm bath of "solid progress across the board"
  — hides the one thing the leader needed to see. This forces the fire to the top.
- **Mandatory attribution + "No update from"** keeps the summary trustworthy: the
  reader can trace any line back to a team, and silence is shown as silence, not
  quietly rounded up to "fine."
- **"Decisions needed" as its own section** turns a status doc into an action
  doc — the reader knows exactly what they're on the hook for.
- **Contradiction flagging** catches the thing roll-ups routinely bury: two
  sources that don't agree, which is usually the most important signal in the pile.

## Variations

- **Board / investor update:** raise the budget, drop team names for functional
  areas, and add a `**Metrics**` table pulling any numbers the updates mention.
- **Portfolio view:** if the sources are projects not teams, add "tag each as
  🟢/🟡/🔴 and sort worst-first" for a scannable health dashboard.
- **Trend-aware:** paste last period's roll-up too and add "note what changed
  since last period — what got better, what got worse."
</content>

---

Source: fablerlabs.com/knowledge-pack (free pack)
