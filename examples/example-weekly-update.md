# Worked example — Weekly update

`prompts/weekly-update.md` turning a Friday brain-dump into a clean update.
(Illustrative.)

---

## Brain-dump pasted into `<braindump>`

```
audience: my manager, cares about the launch date and whether we're on track
- spent a bunch of time on the onboarding thing, finally got the new flow merged
- did a ton of code review for ben
- the analytics events STILL might not be firing, ana looking into it, kind of
  worried this blocks the launch metrics
- started the mobile testing, carla found 2 bugs, fixing
- next week: finish mobile signoff, then we can actually ship
- oh i also updated some docs
```

## Output from Claude

**Week of 2026-06-12 — [Your name]**

**Shipped**
- Merged the new onboarding flow (code-complete; mobile sign-off pending).
- Cleared the review backlog so Ben's work isn't blocked.

**In progress**
- Mobile testing on the redesign — Carla found 2 bugs, fixes underway. Sign-off
  is the last gate before we ship.

**Risks / blockers**
- Analytics events may not be firing. Ana is investigating. If unresolved, we
  ship the redesign but launch **without reliable launch metrics** — flagging now
  so it doesn't surprise us at go-live.

**Next week**
- Land mobile sign-off and ship the redesign.
- Confirm analytics are firing before we call the launch measurable.

---

### What to notice
- **Activity became outcome**: "did a ton of code review" → "cleared the review
  backlog so Ben isn't blocked." "spent time on the onboarding thing" → the
  concrete "merged the new flow."
- **The doc update was cut** — the manager wouldn't act on it, and the word budget
  is for what matters.
- **The risk was elevated, not buried**: the analytics uncertainty is stated with
  its consequence (no reliable launch metrics), which is exactly what a manager
  needs to decide about — and it was **not inflated** beyond what the notes said.
