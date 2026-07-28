# Summarize a long document (report, contract, thread, spec)

Get the signal out of something long — a 40-page report, a contract, a 200-message
thread, a dense spec — at the depth you actually need, with page/section anchors
so you can verify before you trust.

---

## How to use

1. Paste the PROMPT, then paste (or attach) the document.
2. Choose your **depth** by editing one line. Start with `gist`; go deeper only
   where it matters.
3. Every claim is anchored — spot-check two of them against the source before you
   rely on the summary. AI summaries are a starting map, not the territory.

---

## PROMPT

```
You summarize dense documents for a decision-maker who has no time to read them
but will be held responsible for what's in them. You are faithful to the source
and you flag your own uncertainty.

<depth>{{one of: "gist" = 5 bullets; "brief" = 1 page; "deep" = section-by-section}}</depth>
<lens>{{what I care about — e.g. "obligations and deadlines" for a contract;
"risks and unknowns" for a report; "decisions and disagreements" for a thread}}</lens>

<task>
Summarize the document below at the requested depth, through the requested lens.
Rules:
- Anchor every non-obvious claim with a locator: (p. 12) / (§3.2) / (msg from Ana).
  If you can't locate a claim, don't include it.
- Separate what the document SAYS from what it IMPLIES; label inferences as
  "(inference)".
- Call out anything surprising, contradictory, or that looks like a trap
  (auto-renewal, liability, a buried assumption) under "Watch-outs".
- If the document is truncated or you couldn't read part of it, say so explicitly.
- Do not soften or editorialize; neutral and exact.
</task>

<document>
{{PASTE OR ATTACH}}
</document>

<output_format>
## Bottom line
(1–3 sentences: what this document means for me.)

## Summary
(at the requested depth, anchored)

## Watch-outs
- ... (anchored)

## Questions this raises
- ...
</output_format>
```

---

## Why this prompt works

- **Locators on every claim** turn an un-checkable summary into a verifiable one —
  you can jump to (§3.2) and confirm. This is the difference between a summary you
  can act on and one you can only hope is right.
- **Says vs implies** stops the model from laundering its own inference as the
  document's content.
- **"Watch-outs"** is where the money is for contracts and reports — the
  auto-renewal clause, the liability cap, the assumption the whole plan rests on.
- **Depth switch** keeps you from paying for a section-by-section breakdown when 5
  bullets would do.

## Variations

- **Contract review (non-legal):** set lens to "obligations, termination, money,
  liability" and add `End with: "Not legal advice — here are the 3 clauses I'd
  ask a lawyer about."`
- **Compare two docs:** paste both and ask "what changed between v1 and v2, and
  which changes matter?"
- **Thread → decision:** for a long email/Slack thread, set lens to "what was
  decided and what's still open," reusing the meeting-notes discipline.

---

Source: fablerlabs.com/knowledge-pack (free pack)
