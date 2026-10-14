---
name: teach-it-with-projects
description: Builds a structured learning path for a new topic — an essentials guide, a ladder of hands-on projects (a simple one built by hand, then an optional real-world one), an interactive lab page (a local HTML file) and self-check quizzes, with a PROGRESS.md to resume from. Works step by step with the user, or builds everything at once.
argument-hint: <topic>  (or no argument to resume the topic in the current folder)
disable-model-invocation: true
---

# Teach It With Projects

The user wants to *understand* the topic, not just get working code. Everything
you make should look like what they would meet at work: mainstream tools,
standard project layout, honest results.

## Quick start

`/teach-it-with-projects diffusion models` → show the guide's table of contents,
then the settings (mode, folder, level, tools, quizzes) → write
`DIFFUSION_MODELS_ESSENTIALS.md` → build `01_<name>/` → lab page → ask whether
they want Project 02 (then offer 4–5 problems).
`/teach-it-with-projects` with no topic, inside a topic folder → resume from `PROGRESS.md`.

## How to work with this user

- **Plan first.** Show the plan or a summary before writing any file.
- **Follow the mode** they chose (see Modes below).
- **Ask in conversation, never with a question form** (no AskUserQuestion). Put
  numbered options in your message; they reply casually and may decide later.
- **Open requests = your judgment.** "Make some diagrams" means you pick what is
  worth visualizing.
- **Save things so they can pick them up later**; keep everything in the topic
  folder and linked from the guide.
- **Be honest about results.** Compare against tuned simple baselines. If the
  simple thing wins, say so and present it as a lesson, not a failure.

## Modes

- **Step by step (default).** You build one piece (a guide section group, a
  project module, a results run), then stop. Say what you did and why, and wait.
  They read it, run it, answer the quiz, ask questions or change direction; only
  then move on.
- **All at once.** You build the guide, Project 01 and the lab in one go, then
  give a short tour: what each piece is, Project 01's workflow, how to run it,
  what to read first.

After each project, in either mode, end with the handover message from
[reference/projects.md](reference/projects.md): what was built and how it flows,
not a results report.

In both modes, the first round ends after Project 01 and the lab. Project 02 is
only built if they say yes.

They can switch modes at any time ("just finish the rest", "let's slow down").

## Where things go

Ask in the kickoff, with the current folder as the default:

1. **Here** — `./<topic_slug>/` in the folder they called the skill from (if that
   folder is already named `<topic_slug>`, use it directly).
2. **`~/learning/<topic_slug>/`** — the shared learning folder.
3. **Both** — files live here, and `~/learning/<topic_slug>` is a symlink to them,
   so `~/learning/` stays an index of everything they're learning.

```
<topic folder>/                   # <topic_slug>: lowercase, underscores
├── PROGRESS.md                   # see reference/progress.md
├── <TOPIC>_ESSENTIALS.md         # the guide (links to the lab)
├── <TOPIC>_ESSENTIALS_LAB.html   # the lab: a local HTML file
├── 01_<name>/                    # simple, by hand
└── 02_<name>/                    # optional: real-world problem, industry tools
```

## Workflow

```
- [ ] 0. Start or resume
- [ ] 1. Kickoff: plan, then settings
- [ ] 2. Essentials guide + PROGRESS.md
- [ ] 3. Project 01
- [ ] 4. Lab page
- [ ] 5. Project 02? (ask; if yes, offer 4–5 problems first)
```

The user can reorder steps or ask for the lab earlier — follow them. Update
`PROGRESS.md` at the end of every piece.

**0. Start or resume.** Look for `PROGRESS.md` in the current folder,
`./<topic_slug>/` and `~/learning/<topic_slug>/`. If found, read it, summarize
where they are in 3–5 lines, propose the next step, and stop. If it came from
`teach-it` (theory only), the guide already exists: skip to Project 01 and link
projects to its sections.

**1. Kickoff (one message).** First the guide's table of contents and a one-line
idea for Project 01. Don't propose Project 02 themes yet. Then, at the end, the
settings with defaults filled in, as a numbered list they can correct:

```
Settings (correct anything)

1. Mode: step by step — I build one piece, then stop so you can review it, run it
   and ask questions. Or: all at once — I build everything, then walk you
   through it.
2. Folder: here (./<topic_slug>/). Or: ~/learning/<topic_slug>/, or both.
3. Level: beginner
4. Tools: industry default. Or: your choice.
5. Quizzes: on
```

Stop. Create the folder once they confirm.

**2. Essentials guide.** Follow [reference/essentials-guide.md](reference/essentials-guide.md).
Create `PROGRESS.md` from [reference/progress.md](reference/progress.md).

**3. Project 01.** Simple, built by hand. Follow
[reference/projects.md](reference/projects.md).

**4. Lab page.** Follow [reference/lab-page.md](reference/lab-page.md), using
Project 01's real numbers.

Then **ask whether they want Project 02**: one or two lines on what it adds (a
real problem, industry tools, honest evaluation) and that it takes longer. Stop.
Record the answer in `PROGRESS.md`; "later" is a fine answer.

**5. Project 02** (only if they said yes). **First offer 4–5 real-world problem
options**; wait for their pick or idea. Build it in the mode they chose. Offer to
update the lab with its results.

**Quizzes** (when on): follow [reference/quiz.md](reference/quiz.md) at the end
of each guide section and project README.
