# Changelog

All notable changes to the Claude Knowledge-Work Pack.

## [1.1.1] — 2026-07-28
Documentation only. No prompt, template or example changed.

### Changed
- `README.md` now says what else the lab makes. The pack shipped with a bare
  footer link and named none of the five paid packs, so a reader who liked it had
  nowhere to go. The new section is explicit that the paid packs are for AI
  *coding* work rather than the document work this pack covers.
- Removed "if it doesn't save you the price of the pack in the first week" — this
  pack is free, so the line asked the reader to weigh a price that does not exist.

## [1.1.0] — 2026-07-07
Six new prompts — the pack now covers 14 knowledge-work tasks.

### Added
- `prompts/prd-drafter.md` — a rough idea → a scoped product spec with a real
  problem statement and mandatory non-goals (the scope-leak guard).
- `prompts/status-rollup.md` — many teams' separate updates → one exec summary
  that leads with exceptions and never averages a fire into "good progress."
- `prompts/feedback-to-themes.md` — a high-volume dump of reviews / tickets / NPS
  → prioritized themes with honest counts, bug-vs-request routing, and a
  self-selection caveat. (Distinct from `interview-synthesis`, which is for
  deep, small-N interviews.)
- `prompts/sop-writer.md` — a process that lives in your head → a repeatable SOP,
  with `[FILL: …]` placeholders instead of guessed thresholds or approvers.
- `prompts/meeting-prep-brief.md` — a meeting you haven't prepped → a one-screen
  brief with steelmanned objections and honest answers (flags your weak spots).
- `prompts/rewrite-for-audience.md` — a blunt or rambling draft → a retargeted
  version that changes tone/length but never the meaning, with a "what I changed"
  note and a "heads up" on anything that could land badly.

### Changed
- README contents table and `INDEX.md` updated to list all 14 prompts.

## [1.0.1] — 2026-07-07
Polish & honesty pass.

- Added a top-level `INDEX.md`: a one-line "use this when…" for every prompt,
  template, and example, all in one place.
- Added an explicit AI-authorship disclosure to the README footer.
- Replaced the "battle-tested" claim with an honest description — these prompts
  are engineered against each task's failure modes, not yet field-proven at scale.
- Cross-linked the three prompts that have worked examples (meeting notes,
  weekly update, decision memo) to those examples.

## [1.0.0] — 2026-07-07
Initial release.

- 8 engineered prompts: meeting-notes-to-actions, weekly-update, decision-memo,
  inbox-triage-email-draft, summarize-long-doc, competitive-brief,
  project-kickoff-brief, interview-synthesis.
- 4 fill-in templates: one-pager, weekly-update, decision-log, meeting-agenda.
- 3 worked examples (meeting notes, decision memo, weekly update) showing input →
  output on realistic messy content.
- START-HERE quickstart + GUIDE (voice samples, verify-before-you-send,
  prompt-chaining, what-not-to-use-it-for).
- MIT license.
