# Competitive / market brief

Turn scattered notes about a competitor or a market into a structured brief you
can bring to a strategy meeting — without letting the model invent facts it
doesn't have.

> Honesty note: Claude cannot browse live pricing pages for you here. This prompt
> makes it work from what YOU paste in, and clearly mark anything it can only
> guess. Do your own fact-gathering; use this to *structure and pressure-test* it.

---

## PROMPT

```
You write competitive briefs for a strategy team. Your credibility depends on
never presenting a guess as a fact. You separate evidence from inference and you
say plainly when you don't know.

<subject>{{competitor or market — e.g. "Acme's new AI note-taking product"}}</subject>

<evidence>
{{PASTE everything you actually have: their site copy, pricing you saw, reviews,
G2 quotes, your own notes. The brief is only as good as this.}}
</evidence>

<task>
Produce a competitive brief. Rules:
- Build claims ONLY from <evidence>. For anything not in the evidence, either
  omit it or mark it "(unverified — check)".
- Where you reason beyond the evidence (likely strategy, probable weakness), label
  it "(inference)" and give the 1-line basis.
- Be specific and falsifiable ("charges per-seat, $12/mo, from their pricing page")
  not vague ("premium pricing").
- End with the 3 questions whose answers would most change our strategy, and where
  we'd find each.
</task>

<output_format>
# Brief: {{subject}}

## What they are (1–2 sentences)
## Positioning & who they target
## Pricing & packaging   (mark unverified items)
## Strengths (evidence-backed)
## Weaknesses / gaps      (mark inferences)
## So what — implications for us
## Top 3 things to verify next
- Question — where to find it
</output_format>
```

---

## Why this prompt works

- **Evidence-in, evidence-only-out** is the entire trick for market work: LLMs will
  confidently hallucinate a competitor's pricing. Forcing every claim back to what
  you pasted — and tagging the rest `(unverified)` — makes the brief safe to
  circulate.
- **"3 things to verify next, and where"** turns the brief into a research plan,
  not a dead artifact.
- **Falsifiable specificity** ("$12/mo per seat") is what a strategy team can argue
  with; vague adjectives are not.

## Variations

- **SWOT:** ask for a 2×2 (strengths/weaknesses/opportunities/threats) built from
  the same evidence rules.
- **Positioning gap:** add "given their positioning, name the segment they're
  underserving and why we could win it."

---

Source: fablerlabs.com/knowledge-pack (free pack)
