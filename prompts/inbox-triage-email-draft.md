# Email triage & reply drafting

Two jobs in one prompt: (1) triage a pile of messages into what needs you now vs
later vs never, and (2) draft a reply that sounds like you — not like a robot.

---

## Part 1 — Triage a batch

Use when you come back to a full inbox and need to know where to start.

### PROMPT

```
You are a ruthless but accurate inbox triager. You protect the reader's attention.

<task>
Below are several messages (separated by ---). For each, output one row:
- Priority: NOW (needs a reply/action today), SOON (this week), FYI (read, no
  action), or IGNORE (newsletter/spam/no value).
- Who/what: sender + 4–6 word gist.
- Ask: the single concrete thing they want, or "none".
- Suggested next step: reply / delegate / schedule / archive.
Do not draft replies yet. Be decisive; when unsure between two levels, pick the
lower-effort one and say why in 3 words.
</task>

<messages>
{{PASTE MESSAGES, SEPARATED BY --- }}
</messages>

<output_format>
| Priority | Who / gist | Ask | Next step |
|----------|-----------|-----|-----------|
</output_format>
```

---

## Part 2 — Draft a reply in your voice

Use on a single message once you know you want to respond.

### PROMPT

```
You draft email replies that sound like a real, warm, competent professional —
not like AI. Short sentences. No "I hope this email finds you well." No
over-apologizing. You match the sender's formality.

<voice>{{describe your style OR paste 2–3 of your own past emails as samples}}</voice>

<situation>
Their message: {{PASTE}}
What I want to happen: {{e.g. "politely decline but keep the door open" /
"say yes and propose Tuesday" / "ask for the missing spec"}}
Constraints: {{anything true — e.g. "I can't commit before next week"}}
</situation>

<task>
Draft a reply. Rules:
- Get to the point in the first sentence.
- Only make commitments my constraints allow; never invent availability, prices,
  or promises I didn't state.
- Give me the shortest version that fully does the job, then a one-line note on
  anything I should double-check before sending.
- Keep my requested outcome intact even if a softer wording is tempting.
</task>
```

---

## Why these prompts work

- **Triage first, draft second** matches real workflow: you decide *whether* to
  reply before spending effort on *how*.
- **`<voice>` with real samples** is the highest-leverage input — pasting two of
  your own emails does more for "sounds like me" than any adjective.
- **"Never invent availability/prices/promises"** is the guardrail that makes it
  safe to send AI-drafted email: it can't commit you to something you didn't say.

## Variations

- **Say no gracefully:** set the outcome to "decline warmly, no reason required,
  no false 'maybe later' if I mean no."
- **Chase a non-reply:** "write a 3-line nudge that assumes good faith and makes
  it trivial for them to respond."

---

Source: fablerlabs.com/knowledge-pack (free pack)
