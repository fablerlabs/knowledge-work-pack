# Worked example — Decision memo

`prompts/decision-memo.md` run on a common small-team decision. (Illustrative.)

---

## Inputs given

```
Decision: Should we build our own billing/subscriptions or use a payments provider?
Options: build in-house on our DB; use a payments provider's hosted checkout; and
  anything obvious I'm missing.
What matters: we're a team of 3, launching in 6 weeks, low volume at first, cannot
  afford a compliance mistake.
What I know: ~200 expected customers in year one; nobody on the team has done PCI;
  we already use Postgres.
```

## Output from Claude

# Decision: Build billing in-house or use a payments provider?

**TL;DR:** Use a provider's hosted checkout for launch; revisit only if
economics or control needs change materially.

## Options
### Option A — Build in-house on Postgres
For: Full control of data model and edge cases; no per-transaction fee; no new
vendor.
Against: You take on PCI scope with no PCI experience and a 6-week runway;
handling cards, dunning, tax, and failed-payment retries is months of work, not
weeks; a compliance mistake is exactly the risk you said you can't afford.

### Option B — Provider hosted checkout
For: Card data never touches your servers (PCI scope minimized); tax, retries,
invoicing, and dunning are handled; days to integrate, not months; fits the
6-week deadline.
Against: Per-transaction fee; you depend on a vendor and their UI; some
advanced flows need their APIs learned.

## Recommendation
Use hosted checkout. At ~200 customers/year the transaction fees are trivial
against months of engineering and the compliance risk of DIY card handling. Your
constraints (tiny team, hard deadline, zero PCI experience, can't afford a
mistake) all point the same way.

## Key assumption
This holds if volume and pricing stay modest so per-transaction fees remain
immaterial. It flips if you reach a scale where fees exceed the cost of a
dedicated billing engineer, or you need billing logic no provider supports.

## What I'd want to know before committing
- Expected average transaction size and take rate (to size the fee honestly).
- Whether any target customer requires invoicing/terms a hosted flow can't do.
- Data-residency or contractual constraints that might rule out a given vendor.

---

### What to notice
- **Both options are steelmanned** — the in-house case gets its real upside
  (control, no fees) before the memo rejects it. That's what makes the
  recommendation trustworthy rather than a foregone conclusion.
- The **key assumption** names the exact condition (scale/fees) under which the
  answer flips — so a reader who disagrees knows precisely where to push.
- The model **asked for the two facts it lacked** (transaction size, invoicing
  needs) instead of inventing them.
