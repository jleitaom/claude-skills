# teach-it-with-projects

Learn a topic by building: an essentials guide, a ladder of projects from simple
to real-world, an interactive lab page and self-check quizzes.

You choose how to work: **step by step** (Claude builds one piece, you review it,
run it and ask questions, then move on) or **all at once** (Claude builds
everything, then walks you through it). The lab is a local HTML
file you open in your browser.

The first round is the guide, a simple Project 01 and the lab. Claude then asks
whether you want Project 02, a real-world problem built with industry tools.

Files go in a `<topic>/` folder where you call the skill, in `~/learning/<topic>/`,
or both (Claude asks). A `PROGRESS.md` lets you stop and resume. The folder format
is shared with [`teach-it`](../teach-it/), so you can start with theory and add
projects to the same topic later.

## Usage

Manual-only (Claude won't trigger it on its own):

```
/teach-it-with-projects <topic>     # start a new topic
/teach-it-with-projects             # inside a topic folder: resume from PROGRESS.md
```

## Install

```bash
npx skills add jleitaom/claude-skills -g --skill teach-it-with-projects
```

To install all skills as a plugin, see
[Installation](../../../README.md#installation).
