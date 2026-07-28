# The Guide — getting 2× more out of every prompt

The prompts work out of the box. These habits make them noticeably better. Read
once; they become automatic.

---

## 1. Feed voice samples, not adjectives

When a prompt asks for your voice or style (email, updates), don't write
"professional but warm." **Paste two or three real things you've written.** The
model matches patterns far better than it follows descriptions. Three of your own
past emails will make a reply sound like you in a way no adjective can.

Keep a small `my-voice.md` file with 2–3 samples and paste it into the `<voice>`
tag. Reuse it everywhere.

## 2. Verify before you rely — especially summaries

Every summary and brief in this pack is built to be *checkable* (page anchors,
frequency counts, `(inference)` labels, `(unverified)` tags) — because an AI
summary is a **map, not the territory**. The honest workflow:

1. Read the AI output.
2. Spot-check two anchored claims against the source.
3. *Then* act on it.

This takes 30 seconds and is the difference between "AI saved me an hour" and "AI
confidently misled me in a meeting." The prompts do their part by never hiding a
guess as a fact; you do yours by checking the two that matter.

## 3. Give it the real inputs, then get out of the way

The quality ceiling of every prompt is set by what you paste in. A weekly update
from three bullet points will be thin; from a week of running notes it'll be
sharp. The prompts are engineered to **not invent** what you didn't give them —
so the fix for a thin result is always more/better input, not a fancier prompt.

Cheapest habit that pays off: keep a running scratch file during the week/meeting/
project, then paste the whole thing in at the end.

## 4. Chain the prompts

They're designed to hand off to each other:

- **Meeting agenda template → meeting-notes-to-actions → decision-log**: run the
  meeting from the agenda, paste the live notes into the notes prompt, drop the
  resulting decision into your decision log.
- **decision-memo → one-pager template → decision-log**: the memo's "key
  assumption" line drops straight into both the one-pager and the log.
- **summarize-long-doc → decision-memo**: summarize the dense report, then feed the
  bottom-line + watch-outs in as the "what I know so far" for a decision.

## 5. Bend the output format freely

The `<output_format>` block is a suggestion, not a cage. Want the weekly update as
a Slack message instead of sections? Add "format as a single Slack post with
emoji section headers." Want the memo as a table? Ask. The role and guardrails do
the heavy lifting; the format is yours.

## 6. Push back and iterate in the same chat

If the first pass is 80% right, don't re-paste everything — just say what's off:
"the recommendation is too soft, commit harder" or "cut the second option, it's
not real." Claude keeps the context; you're editing, not restarting.

## 7. What NOT to use this for

- **Legal, medical, tax, or financial advice.** The contract-review variation
  ends with "here are the clauses I'd ask a lawyer about" *on purpose*. Use these
  to prepare for an expert, not replace one.
- **Anything you won't read before sending.** Every prompt produces a draft. You're
  the editor and you own what goes out under your name.
- **Fabricating research or reviews.** The competitive and interview prompts
  refuse to invent facts because circulating invented facts is how you lose trust.
  Keep it honest; that's the whole value.

---

## The one-sentence version

Give the prompts real inputs, check the claims that matter before you send, and
let the guardrails keep the output honest — do that and Claude stops being a
fancy search box and starts being the co-worker who drafts the boring documents
so you don't have to.
