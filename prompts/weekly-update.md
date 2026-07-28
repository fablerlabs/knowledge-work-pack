# Weekly update / status report

Turns a messy brain-dump of the week into a crisp update your manager or team
actually reads — in a consistent format, every week, in about two minutes.

> **See it run:** [`examples/example-weekly-update.md`](../examples/example-weekly-update.md)
> shows this prompt on a real Friday brain-dump.

---

## How to use

1. During the week, drop rough notes anywhere (a running text file works).
2. Friday, paste the PROMPT plus your brain-dump into Claude.
3. Edit the one paragraph that needs your judgment; send the rest.

---

## PROMPT

```
You write weekly updates that respect the reader's time: concrete, skimmable,
honest about risk. You lead with outcomes, not activity.

<audience>{{who reads this — e.g. "my manager + skip-level; they care about
delivery risk and headcount, not implementation detail"}}</audience>

<task>
Turn my raw notes (in <braindump>) into a weekly update. Rules:
- Lead with SHIPPED / outcomes, not "worked on".
- Convert activity into impact where the notes support it; if they don't, keep
  it factual and do NOT inflate ("refactored auth" not "dramatically improved
  security").
- Surface risks and blockers honestly — a good update makes bad news easy to
  act on. If I gave none, write "No blockers this week."
- Keep the whole thing under ~200 words. Cut anything the audience wouldn't act on.
- Use plain language; no corporate filler ("synergy", "circle back", "leverage").
</task>

<braindump>
{{PASTE YOUR ROUGH NOTES}}
</braindump>

<output_format>
**Week of {{date}} — {{your name/team}}**

**Shipped**
- ...

**In progress**
- ... (add a % or ETA only if my notes give one)

**Risks / blockers**
- ...

**Next week**
- ...
</output_format>
```

---

## Why this prompt works

- **Audience block** makes the model tailor detail level — an update for a CEO is
  not an update for a tech lead.
- **"Convert activity into impact, but don't inflate"** is the whole game: it
  fixes both the "I worked on stuff" problem and the "AI oversells everything"
  problem in one instruction.
- **Hard word budget** forces prioritization; skimmable structure gets it read.

## Variations

- **Monthly / quarterly:** raise the budget to ~400 words and add a
  `**Metrics**` section: "pull any numbers I mentioned into a small table."
- **Public changelog:** change the audience to "customers" and add "no internal
  jargon, no team names, describe user-visible benefit only."

---

Source: fablerlabs.com/knowledge-pack (free pack)
