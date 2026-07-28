# Decision Log

A running record of decisions that matter — so six months from now you know
_what_ you decided, _why_, and _what assumption_ it rested on. The cheapest way
to stop re-litigating settled questions.

> One row per decision. Newest at top. Keep it terse.

| Date | Decision | Why (1 line) | Key assumption | Owner | Revisit if… |
|------|----------|--------------|----------------|-------|-------------|
| {{YYYY-MM-DD}} | {{what we decided}} | {{the deciding reason}} | {{what must stay true}} | {{name}} | {{trigger to reopen}} |
|  |  |  |  |  |  |

---

## How to use
- Log a decision the moment it's made, while the reasoning is fresh.
- The **key assumption** and **revisit if…** columns are what make this more than
  a diary: they tell future-you when a past decision has expired.
- Feed a decision straight in from `prompts/decision-memo.md` — the memo's "key
  assumption" line drops right into this table.

## Example row
| 2026-06-14 | Use a hosted email provider instead of self-hosting | Team of 3, no ops bandwidth | Volume stays under free-tier limit | Ana | We exceed 50k sends/mo |
