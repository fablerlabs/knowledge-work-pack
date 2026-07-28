# Decision memo (one-pager)

Turns a fuzzy "we need to decide X" into a tight one-page memo that forces a
real decision: the question, the options, the trade-offs, and a recommendation.
The format executives trust because it exposes the reasoning, not just the answer.

> **See it run:** [`examples/example-decision-memo.md`](../examples/example-decision-memo.md)
> shows this prompt on a build-vs-buy call, both options steelmanned.

---

## How to use

1. Paste the PROMPT and answer the four `<inputs>` in your own words — bullet
   fragments are fine, Claude will structure them.
2. Read the draft critically: the **recommendation** is yours to own. Claude
   proposes; you decide.

---

## PROMPT

```
You write decision memos in the style of a sharp operator: one page, no filler,
reasoning visible. You steelman every option before recommending one, and you
name the assumption that would flip the decision if it were wrong.

<inputs>
Decision to make: {{the question — e.g. "Do we build billing in-house or use Stripe?"}}
Options I'm weighing: {{list 2–4; add "and anything obvious I'm missing"}}
What matters most: {{constraints/criteria — cost, speed, risk, hiring, reversibility}}
What I know so far: {{any facts, numbers, or prior context — rough is fine}}
</inputs>

<task>
Write a one-page decision memo. Requirements:
- State the decision as a crisp question at the top.
- For each option: 2–3 line summary, then its strongest case FOR and the honest
  case AGAINST. Steelman even the option you'll reject.
- Make one clear recommendation and say why in 2–3 sentences.
- Name the KEY ASSUMPTION behind the recommendation and what evidence would
  change it. ("This holds only if volume stays under X.")
- If you lack a fact needed to decide well, list it under "What I'd want to know"
  rather than inventing it.
- Neutral, concrete language. No hedging like "it depends" without saying on what.
</task>

<output_format>
# Decision: {{question}}

**TL;DR:** (recommendation in one sentence)

## Options
### Option A — name
For: ...
Against: ...
### Option B — name
For: ...
Against: ...

## Recommendation
...

## Key assumption
This recommendation holds if __. It flips if __.

## What I'd want to know before committing
- ...
</output_format>
```

---

## Why this prompt works

- **"Steelman every option"** kills the model's tendency to strawman the loser to
  flatter the winner — the failure that makes AI memos untrustworthy.
- **"Name the key assumption that would flip it"** is what separates a memo from
  an opinion; it tells the reader exactly where to push.
- **"What I'd want to know" instead of inventing facts** keeps the memo honest
  when your inputs were thin.

## Variations

- **Pre-mortem:** append `Then write a 4-line pre-mortem: assume we picked the
  recommendation and it failed in 6 months — what most likely went wrong?`
- **Two-way vs one-way door:** add to the task `Classify this as a reversible or
  irreversible decision and adjust how much certainty we should demand.`

---

Source: fablerlabs.com/knowledge-pack (free pack)
