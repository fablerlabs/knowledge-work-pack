# The Claude Knowledge-Work Pack

**Fourteen carefully engineered prompts and four templates that turn Claude into a
reliable co-worker for the writing and thinking you do every week** — meeting
notes, weekly updates, decision memos, email, doc summaries, specs, SOPs,
customer feedback, and research synthesis.

Not for coding. For the *other* 80% of knowledge work: the recurring documents
that eat your afternoons. Built for PMs, founders, consultants, ops leads, chiefs
of staff — anyone who runs on Claude but isn't shipping code with it.

---

## Why this exists

Most people use Claude like a slightly-smarter search box: they type a vague
request, get a generic wall of text, and quietly do it themselves anyway. The
gap isn't the model — it's the **prompt**. A knowledge-work task has structure
(a meeting has decisions, owners, and open questions), and a prompt that encodes
that structure gets you output you can actually ship.

This pack is that structure, written down. Each prompt is engineered the way
Anthropic recommends prompting Claude — a clear role, XML-tagged inputs, explicit
output format, and **guardrails against the specific way that task goes wrong**
(inventing owners, inflating status, hallucinating a competitor's pricing). You
paste your mess in; you get a clean, honest draft out.

## What's inside

| # | Prompt | Turns… | …into |
|---|--------|--------|-------|
| 1 | `prompts/meeting-notes-to-actions.md` | raw notes / transcript | decisions, owned action items, open questions |
| 2 | `prompts/weekly-update.md` | a Friday brain-dump | a crisp status update your manager reads |
| 3 | `prompts/decision-memo.md` | "we need to decide X" | a one-page memo with a real recommendation |
| 4 | `prompts/inbox-triage-email-draft.md` | a full inbox / one message | a triage table + a reply in your voice |
| 5 | `prompts/summarize-long-doc.md` | a 40-page report or contract | an anchored, verifiable summary + watch-outs |
| 6 | `prompts/competitive-brief.md` | scattered competitor notes | a strategy-ready brief (no invented facts) |
| 7 | `prompts/project-kickoff-brief.md` | "we should do X" | a one-pager with goal + explicit non-goals |
| 8 | `prompts/interview-synthesis.md` | raw user-interview notes | themes with quotes and honest frequencies |
| 9 | `prompts/prd-drafter.md` | a rough "we should build X" | a scoped spec with explicit non-goals |
| 10 | `prompts/status-rollup.md` | many teams' separate updates | one exec summary that leads with what's off-track |
| 11 | `prompts/feedback-to-themes.md` | a dump of reviews / tickets / NPS | prioritized themes with honest counts + a next step |
| 12 | `prompts/sop-writer.md` | a process that lives in your head | a repeatable SOP someone else can follow |
| 13 | `prompts/meeting-prep-brief.md` | a meeting you haven't prepped | a one-screen brief with objections + answers |
| 14 | `prompts/rewrite-for-audience.md` | a blunt or rambling draft | a retargeted version, same meaning, right tone |

Want a one-line **"use this when…"** for every prompt, template, and example in one
place? See **[`INDEX.md`](INDEX.md)**.

**Templates** (`templates/`) — fill-in-the-blanks docs that pair with the prompts:
one-pager, weekly update, decision log, meeting agenda.

**Examples** (`examples/`) — three prompts shown on realistic messy input with the
output to expect, so you can see the quality before you buy your own time back.

**Guides** — `START-HERE.md` (5-minute setup) and `GUIDE.md` (how to get 2× more
out of every prompt: Projects, voice samples, verification habits).

## The through-line: honest output you can send

Every prompt is built around one principle — **an AI draft is only useful if you
can trust it enough to send.** So each one is wired to:

- **Never invent accountability** — missing owners/dates become `OWNER?`/`DATE?`,
  not a plausible guess.
- **Separate fact from inference** — what a document *says* vs what the model
  *infers* is always labeled.
- **Refuse to inflate** — status updates and memos stay factual; "refactored
  auth," not "dramatically improved security."
- **Stay verifiable** — summaries anchor every claim to a page/section so you can
  check before you rely.

That discipline is the product. The prompts are how it's delivered.

## Works with

Any Claude surface — the Claude app, Projects, the API, or Claude in your editor.
No account beyond Claude, no install, no subscription to this pack. Copy a prompt,
paste your content, go. Provider-neutral in spirit, but tuned for Claude's
strengths (long context, XML-tag steering, faithfulness to source).

## Start here

Open **`START-HERE.md`**, do the 5-minute setup, and run prompt #1 on your last
meeting's notes. If it doesn't save you an hour in the first week, you weren't
going to use it anyway.

## If this was useful

This pack is free and MIT-licensed and stays that way. Nothing in the prompts is
crippled, time-limited, or holding back a "pro" version.

The same lab sells five paid packs. They are all for people working **with AI
coding tools**, which is a different job from the document work this pack covers —
so this is worth your money only if that is also you:

| | |
| --- | --- |
| **AI Coding Workflow Pack** — $24 | 26 files: 6 subagents (code-reviewer, debugger, test-writer, refactorer, doc-writer, pr-describer), 8 slash commands, and 6 per-stack rules files for TypeScript+React, Python, Go, Node APIs, Next.js and monorepos |
| **Autonomous Agent Starter Kit** — $29 | Templates, guardrails and field notes for running an AI coding agent unattended |
| **AI Coding Security Pack** — $29 | Subagents, commands and stack-specific rules that give an AI coding tool a dedicated security reviewer |
| **Agent Constitution Pack** — $19 | Seven complete, annotated `CONSTITUTION.md` governance files for autonomous-agent businesses |
| **18-Point Pre-Deploy Security Checklist** — $1 | A compact editable checklist: secrets, config, auth, data handling, dependencies, infrastructure |

All at **<https://fablerlabs.com>** — card or crypto, instant download, no account.

There is also a second free one, the AI-Coding Field Guide and a
`CLAUDE.starter.md`, at <https://fablerlabs.com/field-guide>.

---

_Made by [Fabler Labs](https://fablerlabs.com). These prompts and templates were
**authored by an autonomous AI agent** — they're engineered against each task's
failure modes, but every prompt still produces a *draft*: you're the editor, so
read it before you send it. MIT-licensed — see `LICENSE.md`. Use every file in
your own work, commercial included, no attribution required._
