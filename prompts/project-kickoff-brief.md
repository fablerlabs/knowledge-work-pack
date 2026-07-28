# Project kickoff brief

Turn "we should do X" into a one-page brief that aligns everyone before work
starts: the goal, why now, what's in and out of scope, who owns it, and how
you'll know it worked. Kills the most expensive kind of rework — building the
wrong thing.

---

## PROMPT

```
You write project kickoff briefs that prevent scope creep and misalignment. You
push for a sharp goal and an explicit non-goals list, because that's where
projects go wrong.

<inputs>
What we want to do: {{one sentence}}
Why now: {{the trigger — a customer ask, a deadline, a metric}}
Who's involved: {{names/roles, or "TBD"}}
Rough constraints: {{time, budget, must-not-break, dependencies}}
</inputs>

<task>
Write a one-page kickoff brief. Requirements:
- Force a single, measurable GOAL. If my input is vague, propose a sharper one and
  mark it "(proposed — confirm)".
- Include an explicit NON-GOALS section (what we are deliberately NOT doing). If I
  gave none, propose 2–3 likely scope traps to rule out.
- Define SUCCESS as something observable ("X drops below Y", "Z ships by date"),
  not "improve" or "better".
- List OPEN QUESTIONS and RISKS honestly; a brief that hides risk is worse than none.
- Keep to one page. Every line should reduce a real disagreement.
</task>

<output_format>
# Kickoff: {{project}}

**Goal:** (one measurable sentence)
**Why now:** ...
**Success looks like:** (observable criteria)

## In scope
- ...
## Non-goals (explicitly out)
- ...

## Owner & roles
| Role | Who |
|------|-----|

## Milestones (if datable)
- ...

## Open questions & risks
- ...
</output_format>
```

---

## Why this prompt works

- **The forced non-goals list** is the highest-value part. Most project failures
  are scope failures; making the model *propose scope traps to rule out* surfaces
  them before they cost weeks.
- **"Measurable goal or mark it (proposed)"** stops fuzzy goals ("improve
  onboarding") from surviving kickoff, without letting the model silently invent
  targets.
- **One-page limit** keeps it a tool people actually read and reference.

## Variations

- **RACI:** expand the roles table into Responsible / Accountable / Consulted /
  Informed.
- **Lean charter:** collapse to goal + non-goals + success + one owner for tiny
  projects.

---

Source: fablerlabs.com/knowledge-pack (free pack)
