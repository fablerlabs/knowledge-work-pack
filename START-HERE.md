# Start here (5 minutes)

You don't need to read the whole pack. Do this, get one win, come back for the
rest later.

## 1. Pick your surface (30 sec)
Any of these work — use whatever you already have Claude in:
- **Claude app** (claude.ai) — simplest. Paste and go.
- **A Claude Project** — best if you'll reuse a prompt weekly (see step 4).
- **Claude in your editor / API** — same prompts, paste into your system or user message.

## 2. Run your first prompt (2 min)
1. Open `prompts/meeting-notes-to-actions.md`.
2. Copy the block under **## PROMPT**.
3. Paste it into Claude. Replace `{{PASTE RAW NOTES OR TRANSCRIPT}}` with the
   notes from your most recent meeting (rough is fine — that's the point).
4. Fill the two small variables at the top (team names, today's date) and send.

You should get back clean decisions, owned action items, and open questions —
with `OWNER?`/`DATE?` wherever your notes were silent, and nothing invented.

## 3. Notice the pattern (1 min)
Every prompt in `prompts/` has the same shape:
- a **role** line (who Claude is being),
- **`<...>` tagged inputs** you fill in,
- a **task** with guardrails against how that job goes wrong,
- an **output format** you can tweak.

Once you see it, you can bend any prompt to your exact need — that's what `GUIDE.md`
is for.

## 4. Make it stick (90 sec) — optional but high-leverage
For the prompts you'll run weekly (meeting notes, weekly update), save the PROMPT
block as a **Claude Project** (set it as the project's custom instructions) or a
saved snippet. Then each week you just paste your raw content — no re-pasting the
prompt.

## 5. Where to go next
- `examples/` — see three prompts run on realistic messy input, so you know what
  "good" looks like.
- `GUIDE.md` — the habits that double the output quality: voice samples, the
  verify-before-you-send rule, chaining prompts together.
- `templates/` — fill-in docs (one-pager, weekly update, decision log, agenda)
  that pair with the prompts.

That's it. One good meeting summary and you're ahead.
