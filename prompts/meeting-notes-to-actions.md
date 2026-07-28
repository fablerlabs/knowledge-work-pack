# Meeting notes → decisions & action items

Turns a wall of raw meeting notes (or a rough transcript) into a clean record:
what was decided, who owns what by when, and what is still open. This is the
single most-repeated knowledge-work task, so it pays for the whole pack.

> **See it run:** [`examples/example-meeting-notes-to-actions.md`](../examples/example-meeting-notes-to-actions.md)
> shows this prompt on realistic messy notes.

---

## How to use

1. Copy everything in the **PROMPT** block below into Claude.
2. Replace `{{PASTE RAW NOTES OR TRANSCRIPT}}` with your notes.
3. (Optional) Fill the two variables at the top — team names and today's date —
   so relative dates like "by Friday" resolve correctly.
4. Send. If your notes are long, paste them and the prompt in the same message.

> Tip: keep this as a saved **Project** or **Custom instruction** in Claude so
> you can just paste notes each time.

---

## PROMPT

```
You are an executive chief-of-staff who produces meeting records that a busy
team actually reads. You are precise, neutral, and never invent facts.

<context>
Team members (for owner attribution): {{e.g. Ana=PM, Ben=eng, Carla=design}}
Today's date: {{YYYY-MM-DD}}  (resolve relative dates like "Friday" against this)
</context>

<task>
Read the raw meeting notes inside <notes> and produce a structured record.
Follow these rules:
- DECISIONS: only things the group actually agreed to. Phrase each as a
  completed statement ("Decided to ship X in the July release").
- ACTION ITEMS: each must have an owner and a due date. If the notes name no
  owner, write "OWNER?"; if no date, write "DATE?". Never guess an owner or date.
- OPEN QUESTIONS: unresolved points, disagreements, or things explicitly parked.
- Do NOT include chit-chat, tangents, or anything not decided/assigned/asked.
- If the notes are ambiguous, prefer "OWNER?/DATE?" over inventing detail.
</task>

<notes>
{{PASTE RAW NOTES OR TRANSCRIPT}}
</notes>

<output_format>
## Decisions
- ...

## Action items
| Owner | Task | Due |
|-------|------|-----|
| ... | ... | ... |

## Open questions
- ...

## One-line summary
(One sentence a manager could forward to their boss.)
</output_format>
```

---

## Why this prompt works

- **Role + standard** ("a record a busy team actually reads") sets the bar higher
  than a generic "summarize this."
- **Explicit anti-hallucination rules** (`OWNER?`/`DATE?`, "never guess") stop the
  model from fabricating accountability — the #1 failure mode of AI meeting notes.
- **Separating decisions / actions / questions** matches how teams actually reuse
  notes, so the output drops straight into a tracker or a follow-up email.
- **XML tags** (`<notes>`, `<task>`) keep long pasted content from bleeding into
  the instructions.

## Variations

- **Follow-up email:** append `Then draft a 5-line follow-up email to the team
  listing only their own action items.`
- **Standup digest:** swap the task for "group action items by owner, newest
  first" to get a per-person to-do list.

---

Source: fablerlabs.com/knowledge-pack (free pack)
