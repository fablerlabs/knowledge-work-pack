# Interview / user-research synthesis

Turn a pile of raw interview notes (user calls, customer feedback, candidate
debriefs) into themes with evidence — the honest way, where every theme is
backed by real quotes and you can see how common it actually was.

---

## PROMPT

```
You synthesize qualitative interviews for a team that will make decisions from
your output. Your integrity rule: every theme must be grounded in actual quotes,
and you never overstate how common something was.

<context>
What these interviews were about: {{e.g. "why trial users don't convert"}}
Number of interviews included: {{N}}  (so frequency claims are honest)
</context>

<notes>
{{PASTE all interview notes. Separate each interview with === so frequency can
be counted. Rough notes are fine.}}
</notes>

<task>
Synthesize into themes. Rules:
- Each THEME needs: a plain-language name, how many of the {{N}} interviews it
  appeared in, and 1–2 verbatim (or near-verbatim) quotes as evidence.
- Order themes by how many interviews mention them (most common first).
- Do NOT merge distinct pain points to inflate a theme, and do NOT report a
  one-off as a pattern — if only one person said it, put it under "Signals worth
  watching (n=1)".
- Separate what people SAID from what you INFER they need; label inferences.
- End with the single most decision-relevant finding and what it implies.
</task>

<output_format>
## Themes (most common first)
### Theme — name  (n=X/{{N}})
- Evidence: "quote" ; "quote"
- What it likely means: (inference)

## Signals worth watching (n=1)
- ...

## The one finding that should change what we do
...
</output_format>
```

---

## Why this prompt works

- **Frequency counts (n=X/N)** are the honesty backbone: they stop the
  ever-present "users hate X!" overstatement when only one of nine said it.
- **Verbatim quotes as required evidence** make every theme auditable — you can
  trace it back to a real person, not a model's vibe.
- **"Don't merge distinct pains, don't promote a one-off"** guards the two ways
  synthesis lies: false consolidation and false generalization.
- **Said vs infer** keeps the user's words separate from your interpretation of
  their needs — critical for research you'll defend in a room.

## Variations

- **Jobs-to-be-done:** add "frame each theme as a job: when ___, I want to ___, so
  I can ___."
- **Opportunity sizing:** ask it to tag each theme high/med/low on frequency ×
  severity to help prioritize.

---

Source: fablerlabs.com/knowledge-pack (free pack)
