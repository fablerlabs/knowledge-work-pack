# Meeting prep brief (walk in ready)

Turns "I have a meeting in an hour and haven't thought about it" into a one-screen
briefing: your objective, who's in the room and what they want, the three
questions that matter, and the objections you'll likely face — with your answer to
each ready. The prep that makes you the most prepared person in the meeting.

> This is the front half of the loop; [`meeting-notes-to-actions.md`](meeting-notes-to-actions.md)
> is the back half. Prep with this, capture with that.

---

## How to use

1. Paste the PROMPT and tell Claude what the meeting is and who's coming — even a
   few lines. The more you say about the *other people's* goals, the sharper the
   objection-handling gets.
2. Skim the **Likely objections** section last, out loud. If an answer feels thin,
   that's the part of your case to shore up before you walk in.

---

## PROMPT

```
You prepare executives for high-stakes meetings. You think from the other side of
the table: what each attendee wants, fears, and will push back on. You are candid
about where the ask is weak, because a brief that only flatters the plan gets its
owner ambushed in the room.

<context>
The meeting is about: {{topic / why it's happening}}
My objective — what I want to walk out with: {{the concrete outcome}}
Who's attending and what I know about them: {{names, roles, their goals/leanings}}
What I'm bringing / proposing: {{the ask, decision, or update}}
Time I have / format: {{e.g. "20 min, 4 people, decision meeting"}}
</context>

<task>
Write a one-screen prep brief. Sections:
- OBJECTIVE: my desired outcome in one sentence, plus my realistic fallback if I
  can't get it.
- WHO'S IN THE ROOM: for each attendee, one line on what they likely care about
  and what would win or lose them. If I gave no info on someone, say
  "(unknown — find out)" rather than inventing a personality.
- THE 2–3 THINGS THAT MATTER: the points that actually decide the outcome. Cut
  everything else; a brief that lists ten priorities has none.
- LIKELY OBJECTIONS: the strongest pushbacks I'll face, each with a crisp, honest
  response. Steelman the objections — the real ones, not easy ones I can swat.
  Where my answer is genuinely weak, say so and suggest how to shore it up.
- OPENING LINE: one sentence to start the meeting that frames it toward my objective.
- Do NOT fabricate facts about attendees, prior meetings, or data. Work only from
  what I gave you; flag what you'd want to know as "Before the meeting, find out: …".
</task>

<output_format>
## Objective
Want: ...  ·  Fallback: ...

## Who's in the room
- **{{Name}}** — cares about ... ; wins them by ...

## The 2–3 things that decide this
1. ...

## Likely objections → your answer
- **"{{objection}}"** → ...
  (⚠ weak spot: ... — shore up by ...)

## Opening line
"..."

## Before the meeting, find out
- ...
</output_format>
```

---

## Why this prompt works

- **"Think from the other side of the table"** flips the default self-centered
  prep ("here's my great plan") into the prep that actually works: modeling what
  the other people want and will resist.
- **Steelmanned objections with honest answers — including "this one's weak"** is
  the whole value. A brief that only rehearses your strengths is exactly how smart
  people get blindsided; naming your soft spot lets you fix it beforehand.
- **"The 2–3 things that matter, cut the rest"** enforces the discipline meetings
  reward: knowing what you'll trade away and what you won't.
- **"(unknown — find out)" instead of invented personalities** keeps the brief
  from confidently mischaracterizing a real colleague — a fabrication that could
  actively mislead you into the wrong approach.

## Variations

- **Negotiation:** add "identify my BATNA and theirs, and the zone of possible
  agreement" for a deal or vendor conversation.
- **Interview / hiring panel:** reframe attendees as "the candidate" and generate
  the 5 questions that best test the one thing you most need to learn.
- **1:1 or performance conversation:** soften to "the outcome I want for them,"
  and add a section on how to open a hard message directly but kindly.
</content>

---

Source: fablerlabs.com/knowledge-pack (free pack)
