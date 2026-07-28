# Worked example — Meeting notes → actions

This shows the `prompts/meeting-notes-to-actions.md` prompt on a realistic messy
input, and the kind of output to expect. (Illustrative — your results will vary.)

---

## Input pasted into `<notes>`

```
q3 planning call. ana ben carla + me. today is jun 12.
talked forever about the onboarding redesign. ben thinks we should ship the new
flow before the marketing push, carla worried it's not tested on mobile. ended up
agreeing we ship the redesign but ONLY after carla signs off on mobile — she said
she can test by end of next week. ben will have the flow code-complete by friday.
marketing push moves to whenever redesign is live, tim to reschedule (tim wasn't
on the call, someone tell him).
also random: coffee machine broken lol. and we might need another designer at
some point, parked that.
oh and the analytics thing - nobody knows if the events are even firing. ana
gonna check. no date given.
```

## Output from Claude

> **Context given:** Ana=PM, Ben=eng, Carla=design, Tim=marketing · Today: 2026-06-12

## Decisions
- Decided to ship the onboarding redesign, but **only after** Carla signs off on
  mobile testing.
- Decided to move the marketing push to after the redesign is live (no longer
  before it).

## Action items
| Owner | Task | Due |
|-------|------|-----|
| Ben | Onboarding flow code-complete | 2026-06-19 (Fri) |
| Carla | Mobile testing + sign-off on redesign | 2026-06-26 (end of next week) |
| Ana | Verify analytics events are actually firing | DATE? |
| Tim | Reschedule marketing push to after redesign is live | DATE? |
| OWNER? | Notify Tim of the reschedule decision (he wasn't on the call) | DATE? |

## Open questions
- Are the analytics events firing at all? (Ana investigating.)
- Do we need to hire another designer? (Parked, no decision.)

## One-line summary
Redesign ships once Carla clears mobile; marketing push and analytics check
follow, with a couple of owners/dates still to nail down.

---

### What to notice
- The **coffee machine** line was correctly dropped — not a decision, action, or
  open question.
- Missing dates became **`DATE?`**, missing owners **`OWNER?`** — nothing was
  invented. The "tell Tim" side-task was surfaced as its own unowned action rather
  than silently folded into Tim's row.
- "Friday" and "end of next week" were **resolved to real dates** using the
  supplied Today value.
