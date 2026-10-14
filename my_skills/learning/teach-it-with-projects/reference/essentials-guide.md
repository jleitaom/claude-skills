# Essentials guide — outline

File: `<TOPIC>_ESSENTIALS.md`. Plain English, no prior knowledge assumed (adjust
to the level setting). Read top to bottom once, then used as a reference while
doing the projects.

## Header

```markdown
# <Topic> — The Essentials

> A <level> guide. Read top to bottom once, then use it as a reference while
> working through the projects.
>
> **Interactive companion:** [`<TOPIC>_ESSENTIALS_LAB.html`](<TOPIC>_ESSENTIALS_LAB.html)
> — open it in your browser. It has live figures for <concept> (§n), <concept> (§n), …
```

Leave the companion block as a placeholder until the lab exists, then fill it in.

## Sections (adapt names to the topic; keep the order of ideas)

1. **What is <topic>?** — one-paragraph intuition plus an everyday analogy.
2. **How it differs from nearby fields** — a comparison table.
3. **Core vocabulary** — a table: term, meaning, example.
4. **The core loop / mechanism** — the one diagram everything else hangs on (ASCII
   or Mermaid in the .md).
5–7. **The key concepts**, one section each, building on each other. Include the
   one or two equations worth knowing, each explained in words.
8. **Your first algorithm or method, worked by hand** — a tiny example with real
   numbers, every step shown.
9. **The family tree** — map of the main methods, with when to use each.
10. **How a real project is structured** — folder layout and why it is split that
    way (the projects follow it).
11. **Is it working? Evaluation** — metrics, baselines, seeds, domain metrics.
12. **Common pitfalls** — table: pitfall, symptom, fix.
13. **When NOT to use <topic>** — honest, with simpler alternatives.
14. **Glossary**
15. **Where to go next** — books, courses, papers, and the projects in this folder.

Add a table of contents with anchor links. Number the sections (§n) so the
projects and the lab can refer to them.

## Style

- Short paragraphs, tables over prose where it helps, bold for key terms.
- Every abstract idea gets a concrete example.
- Mention the projects where they apply ("you'll build this in Project 01").
- Quizzes (if on): a short self-check at the end of each section, per `quiz.md`.
