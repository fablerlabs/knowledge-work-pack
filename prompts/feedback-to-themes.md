# Customer feedback → prioritized themes

Turns a high-volume dump of short customer signals — app-store reviews, support
tickets, NPS verbatims, cancellation reasons, sales-call objections — into a
ranked, deduplicated list of themes with real counts and a suggested action per
theme. The thing that turns "everyone's complaining" into "here are the four
things to fix, in order."

> Not the same as [`interview-synthesis.md`](interview-synthesis.md): that's for
> deep, small-N interviews where quotes carry the weight. This is for *many short
> signals across channels* where frequency and prioritization carry the weight.

---

## How to use

1. Paste the PROMPT and dump the feedback below it — one item per line is ideal,
   mixed sources are fine (label the source if you have it).
2. Read the top three themes and their suggested actions. The **counts** are your
   defense when someone says "but my one angry customer said…".

---

## PROMPT

```
You cluster raw customer feedback for a team that will prioritize work from your
output. Your integrity rule: counts must reflect what's actually in the data, and
you never promote a handful of loud items into a "top issue" they aren't.

<context>
Product / area: {{what this feedback is about}}
Sources included: {{e.g. "support tickets + app-store reviews + churn survey"}}
What we're trying to decide: {{e.g. "what to put on next quarter's roadmap"}}
</context>

<feedback>
{{PASTE all feedback items, ideally one per line. Include the source in [brackets]
if you have it, e.g. "[review] app crashes when I upload a big file". Rough is fine.}}
</feedback>

<task>
Cluster into themes and prioritize. Rules:
- Group items into THEMES by the underlying problem, not by surface wording
  ("can't find the export button" and "where do I download my data" = one theme).
- For each theme: a count (how many items fall in it), a one-line description, and
  1–2 representative verbatim snippets. Counts must be honest — if you're unsure
  an item belongs, don't force it in to pad the number.
- Rank themes by a simple, stated rubric: frequency first, then severity (does it
  block the user or just annoy them?). Show your ranking logic in one line.
- Separate BUGS/BROKEN (something doesn't work) from REQUESTS (something's missing)
  from PERCEPTION (pricing, trust, confusion) — they get handled by different people.
- For each top theme, suggest ONE concrete next action, marked "(suggested)".
  Don't overreach into a full solution; propose the next step.
- Note the SILENT MAJORITY caveat: feedback is self-selected, so state that these
  are the views of people who bothered to write in, not necessarily all users.
- Anything that appears once or twice goes under "Long tail (n≤2)", not the main list.
</task>

<output_format>
## Top themes (ranked: frequency, then severity)
### 1. {{theme}} — n={{count}} · {{Bug|Request|Perception}} · severity {{high/med/low}}
- What people are saying: "snippet" ; "snippet"
- Suggested next step: ... (suggested)

## Long tail (n≤2)
- ...

## Read-with-caution
This is self-selected feedback — the views of people who chose to write in.
{{one line on any obvious skew, e.g. "heavy on angry churned users, light on happy ones"}}
</output_format>
```

---

## Why this prompt works

- **Cluster by underlying problem, not wording** is what separates real synthesis
  from a word-frequency count — it merges the ten ways people describe the same
  broken thing into one countable theme.
- **Honest counts + "don't force items to pad the number"** is the guardrail
  against the most common feedback-analysis lie: inflating a theme to justify the
  work someone already wanted to do.
- **Bug vs Request vs Perception** routes each theme to the team that can act on
  it, and stops "customers are confused by pricing" from landing in an engineer's
  backlog.
- **The self-selection caveat** is the honesty most feedback decks omit — a
  reminder that inbound feedback over-represents the loud and the unhappy.

## Variations

- **Churn deep-dive:** restrict the input to cancellation reasons and add "estimate
  which themes are addressable by us vs out of our control (price, wrong-fit)."
- **Sentiment split:** add "tag each theme as coming mostly from happy, neutral, or
  unhappy users" if the source data carries a rating or NPS score.
- **Quarter-over-quarter:** paste last period's themes too and add "flag which
  themes are growing, shrinking, or new since last time."
</content>

---

Source: fablerlabs.com/knowledge-pack (free pack)
