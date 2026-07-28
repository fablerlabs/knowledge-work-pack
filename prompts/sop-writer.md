# SOP / runbook writer (get it out of your head)

Turns "the way I do this thing every time" — a process that lives only in your
head — into a clean, repeatable SOP someone else can follow without asking you.
The one that lets you delegate, onboard, or go on vacation without the process
breaking.

---

## How to use

1. Talk it through, badly. Paste the PROMPT and brain-dump the steps in whatever
   order they come to you — Claude will sequence and structure them.
2. Answer the **Gaps** section it hands back: those are the steps you do on
   autopilot and forgot to mention. That's where SOPs usually break.

---

## PROMPT

```
You write standard operating procedures that a competent newcomer can follow with
zero prior context and no chance to ask you a question. You are ruthless about
implicit steps: if a human would need to know something to do this correctly, it
must be written down.

<context>
Process name: {{what this procedure accomplishes}}
Who will run it: {{e.g. "a new ops hire, first week" — sets how much to spell out}}
How often / when it's triggered: {{e.g. "every time a refund request comes in"}}
Tools/systems involved: {{the apps, logins, files, or people it touches}}
</context>

<braindump>
{{DUMP the steps as they come to you, out of order is fine. Include the gotchas,
the "oh and don't forget", the "if X then Y" branches — everything you know.}}
</braindump>

<task>
Turn this into a followable SOP. Requirements:
- Start with WHEN TO USE THIS and WHAT YOU NEED (access, tools, info) before step 1.
- Number the steps in the real order of execution. Each step is one concrete
  action starting with a verb ("Open…", "Check…", "Send…").
- Make decision points explicit as "If X, do A. If Y, do B." — don't bury a branch
  inside a sentence.
- Call out anything IRREVERSIBLE or risky with a clear ⚠️ warning and what to
  double-check first.
- Do NOT invent steps, tool names, or values you weren't given. Where the process
  clearly needs a detail I didn't provide (a threshold, an approver, a template),
  insert "[FILL: …]" so I complete it — never guess it.
- End with HOW TO KNOW IT WORKED (the success check) and WHO TO ASK if stuck.
- Keep each step skimmable; a person mid-task should find their place in 2 seconds.
</task>

<output_format>
# SOP: {{process name}}

**When to use:** ...
**You'll need:** (access / tools / info)

## Steps
1. ...
2. ⚠️ ... (what to double-check)
3. If {{condition}} → ... ; otherwise → ...

## Done when
- ...

## If you get stuck
- [FILL: who to ask / where the escalation path is]
</output_format>
```

---

## Why this prompt works

- **"Zero prior context, no chance to ask you"** sets the exact bar an SOP must
  clear. It forces out the implicit knowledge — the login you always use, the box
  you always check — that lives in your hands, not your notes.
- **"[FILL: …]" instead of guessing** is the critical honesty move: a fabricated
  threshold or approver in a runbook is worse than a blank, because someone will
  follow it. This makes the gaps visible and yours to close.
- **Explicit branches and ⚠️ on irreversible steps** are where real procedures
  live — the refund that can't be un-issued, the "if it's a VIP account, escalate"
  path that only you knew about.
- **"Done when" success check** turns a list of actions into a procedure someone
  can actually complete with confidence, not just perform.

## Variations

- **Checklist mode:** append `Also output a stripped checkbox version (just the
  actions, no explanation) for someone who's run it before.`
- **Troubleshooting runbook:** reframe as "when {{system}} breaks" and structure
  it as symptom → likely cause → fix, most-common-first.
- **Onboarding doc:** for a role rather than a task, add "group the steps into
  Day 1 / Week 1 / Month 1 and note what they should be able to do unassisted by each."
</content>

---

Source: fablerlabs.com/knowledge-pack (free pack)
