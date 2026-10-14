# Claude Skills

The Claude Code skills I use: the ones I wrote live in [`my_skills/`](my_skills/),
grouped by category; the ones I use from others are listed in
[`other_skills/`](other_skills/README.md).

## Installation

Requires [Claude Code](https://claude.com/claude-code).

**As a plugin** (all my skills, from every category, in one install). Run inside
Claude Code:

```
/plugin marketplace add jleitaom/claude-skills
/plugin install jleitaom-skills@jleitaom
```

Plugin skills are namespaced, e.g. `/jleitaom-skills:teach-it <topic>`.

To get updates, including new skills, run `/plugin update`, or turn on
auto-update for the `jleitaom` marketplace in the `/plugin` menu. What changed in
each version is in [`CHANGELOG.md`](CHANGELOG.md).

**Single skills** (pick skills, plain `/teach-it` names), with the
[skills](https://skills.sh) CLI. Requires Node.js:

```bash
npx skills add jleitaom/claude-skills --list               # see what's available
npx skills add jleitaom/claude-skills -g --skill teach-it  # install one skill
```

`-g` installs it for your user (all projects); leave it out to install into the
current project only. Update later with `npx skills update`; new skills need
their own `add`.

## Skills

Each skill's folder has a README with what it does and how to use it.

### [Learning](my_skills/learning/)

- **[teach-it](my_skills/learning/teach-it/)**: Learn a topic in theory: a guide in parts, with interactive figures, diagrams, charts, real-world case studies and quizzes. No projects.
- **[teach-it-with-projects](my_skills/learning/teach-it-with-projects/)**: Learn a topic by building: essentials guide, projects from simple to real-world, interactive lab page, quizzes.

## Other skills and plugins

Skills and plugins by others that I use are listed in
[`other_skills/`](other_skills/README.md).
