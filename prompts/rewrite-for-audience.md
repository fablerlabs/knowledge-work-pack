# Rewrite for a specific audience

Takes something you've already written — a rambling email, a too-technical
explainer, a blunt Slack message you shouldn't send as-is — and retargets it for a
specific reader: right length, right tone, right level of detail, same meaning.
The prompt for the last 10% of polish, without losing what you actually meant.

---

## How to use

1. Paste the PROMPT, then your draft, then say who it's *really* for and how you
   want to come across.
2. Claude returns the rewrite **plus a short note on what it changed and why** —
   read that note; it tells you whether it shifted your meaning or just your tone.

---

## PROMPT

```
You are an editor who sharpens other people's writing for a specific reader. You
change how something is said, never what it means. You do not add facts, claims,
or commitments the original didn't make, and you flag it if the original says
something you suspect the writer didn't intend.

<audience>
Who this is really for: {{e.g. "our biggest customer's CFO — skeptical, busy"}}
How I want to come across: {{e.g. "confident but not defensive; warm, not chummy"}}
Format & length: {{e.g. "an email under 120 words" / "a Slack message, 3 lines"}}
</audience>

<draft>
{{PASTE what you've already written — however rough or blunt}}
</draft>

<task>
Rewrite the draft for that audience. Rules:
- Preserve every fact, commitment, and ask in the original. Do NOT invent details,
  soften a hard "no" into a "maybe", or add promises I didn't make.
- Match the requested tone and length. If hitting the length means cutting a real
  point (not just filler), tell me which point you cut rather than dropping it silently.
- Lead with what the reader most needs; move throat-clearing and context to the end
  or out entirely.
- Kill filler, hedging, and corporate cliché — but keep any nuance that carries
  meaning ("we can't commit to a date" must stay uncertain if it was uncertain).
- If the original contains something that will land badly with this audience (a
  buried insult, an over-promise, an ambiguous ask), REWRITE it well but note it
  under "Heads up" so I know it was there.
- Neutral, natural human voice. Not stiff, not sycophantic, no exclamation-mark
  enthusiasm I didn't ask for.
</task>

<output_format>
## Rewrite
...

## What I changed
- (tone / length / structure — one or two lines)

## Heads up (only if relevant)
- (anything in the original that could land badly, or a real point I had to cut)
</output_format>
```

---

## Why this prompt works

- **"Change how it's said, never what it means"** is the core constraint. The
  danger of an AI rewrite isn't bad prose — it's a version that reads beautifully
  but quietly softened your "no," dropped your caveat, or promised a date you
  never gave. This locks the meaning in place.
- **The "What I changed" note** makes the edit auditable in five seconds: you see
  whether it moved your tone or your substance, so you can trust the rewrite
  without re-reading your original line by line.
- **"Heads up" on things that land badly** turns the editor into a second pair of
  eyes — it catches the buried insult or the accidental over-promise you were too
  close to see.
- **"Tell me what you cut" instead of dropping it** keeps the length constraint
  from silently deleting your actual point.

## Variations

- **Level-shift:** set the audience to "a smart 12-year-old" or "a non-technical
  exec" to strip jargon while keeping the substance.
- **Register-shift:** add "make it more formal / more casual by exactly one notch"
  when the tone is close but not quite right.
- **Translate the vibe, keep the spine:** for a hard message, add "keep it direct
  and honest — I want it kinder, not vaguer."
</content>

---

Source: fablerlabs.com/knowledge-pack (free pack)
