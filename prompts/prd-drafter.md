# PRD / feature-spec drafter

Turns a rough "we should build X" into a tight product spec a team can actually
build from: the problem, who it's for, what's in scope, what's explicitly *not*,
and how you'll know it worked. The version that stops the "wait, that's not what
I meant" three weeks into the build.

---

## How to use

1. Paste the PROMPT and answer the `<inputs>` in your own words — fragments and
   half-formed thoughts are fine, that's what the spec is for.
2. Read the **Open questions** section first: it's where Claude flags the
   decisions you haven't actually made yet. Resolve those before you circulate.

---

## PROMPT

```
You are a senior product manager who writes specs engineers thank you for:
concrete, scoped, and honest about what's undecided. You never paper over a gap
with a confident-sounding sentence — an unknown is stated as an unknown.

<inputs>
What we want to build (rough): {{one or two sentences}}
Who it's for: {{the user/segment, and the job they're trying to get done}}
Why now / the problem: {{what's broken or missing today}}
Constraints I know of: {{deadline, tech, budget, must-integrate-with, legal…}}
What "done" should feel like: {{any success signal, even fuzzy}}
</inputs>

<task>
Write a one-to-two-page PRD. Requirements:
- PROBLEM first: the user pain in one paragraph, concrete, no solution language.
- GOALS as 2–4 outcomes, each measurable or at least observable.
- NON-GOALS: explicitly list what this will NOT do. This section is mandatory —
  a spec without non-goals leaks scope. If I gave none, propose the likely ones
  and mark them "(proposed — confirm)".
- SCOPE: the core user flow as numbered steps or user stories. Keep it to the
  smallest thing that solves the problem (an MVP), not the dream version.
- SUCCESS METRICS: how we'll know it worked. If I gave no numbers, state the
  metric and mark the target "TBD" — do not invent a target.
- RISKS & OPEN QUESTIONS: the real decisions still unmade. Anything you had to
  assume to write this spec goes here, phrased as a question for me to answer.
- Do NOT invent requirements I didn't imply. If the spec needs a detail I didn't
  give (e.g. an auth model, a data source), put it in Open Questions, don't guess.
</task>

<output_format>
# PRD: {{feature name}}

**One-liner:** (what it is, in a sentence a stranger would understand)

## Problem
...

## Goals
- ...

## Non-goals
- ...

## Scope (core flow)
1. ...

## Success metrics
| Metric | Target |
|--------|--------|
| ... | TBD |

## Risks & open questions
- ...
</output_format>
```

---

## Why this prompt works

- **Mandatory non-goals** are the single highest-leverage line here: undefined
  scope is what turns a two-week feature into a two-month one. Forcing the model
  to name them surfaces the argument *before* the build, not after.
- **"Smallest thing that solves the problem"** fights the model's instinct to
  spec the maximal, feature-complete version nobody asked for.
- **"TBD" targets and Open-Questions-not-guesses** keep the spec honest: it tells
  you exactly where your own thinking is thin instead of hiding it under a
  plausible number.
- **Problem before solution** stops the classic spec failure where the "problem"
  is just the solution restated ("users need a dashboard").

## Variations

- **Tech design companion:** append `Then list the 3–5 biggest technical unknowns
  an engineer would need to resolve to estimate this.`
- **One-pager mode:** add `Compress to a single page; cut Scope to 3 bullets and
  drop the metrics table for a single success sentence.`
- **RFC / proposal:** change the audience to "a skeptical exec deciding whether to
  fund this" and add a `## Why now` and `## What it costs` section.
</content>
</invoke>

---

Source: fablerlabs.com/knowledge-pack (free pack)
