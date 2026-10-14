# Projects

Every project has a `README.md` (what problem, why, how it fits together, how to
run, results, what you learned), a `results/` folder with saved plots/metrics, and
a quiz at the end of the README when quizzes are on. Link each project to the
guide sections it exercises (§n).

"How it fits together" is a diagram of the workflow: which script or module runs
first, what it writes, what reads it next, up to the results.

## Handover message

When a project is built, the chat message is a quick tour of what was built, not a
results report (results live in the README):
1. **What's there** — the project's files and folders, one line each.
2. **The workflow** — the pipeline as a small diagram (e.g. `simulate.py → data/ →
   analyze.py → results/`), with one line per step on what it does and which §
   it puts into practice.
3. **How to run it** — the commands.
4. **Where to look first** — the README section and lab figures worth opening,
   and one sentence on the headline finding.
5. Anything you couldn't fix or check.

## Project 01 — simple, by hand

- Goal: see the core mechanism with nothing hidden. Implement the core algorithm
  yourself; use only basic libraries (e.g. NumPy, matplotlib).
- Small toy problem that runs in seconds on a laptop.
- Simple layout is fine: `config.py` with all settings, separate modules for the
  main parts (e.g. env/agent, data/model), `train.py` / `evaluate.py` or the
  topic's equivalent, `results/`.
- Compare against a trivial baseline (random, mean, rule).

## Project 02 — optional, a real problem

### Choosing the problem (once they say yes, always do this first)
Offer **4–5 options** as a numbered list. Each option has:
- **Problem** — one line, concrete (a realistic business or engineering task).
- **Why <topic> fits** — one line.
- **Data** — a public dataset, or a realistic synthetic generator you will write.
- **Tools** — the mainstream libraries it would use.
- **Difficulty** — relative to the user's level.

Vary the options across industries and kinds of task. Don't assume a domain. Mark
the one you'd recommend and say why in a sentence. They can pick one, mix them, or
bring their own idea.

### Building it
- Mainstream frameworks for the topic (what teams use at work).
- Standard layout:
  ```
  02_<name>/
  ├── README.md
  ├── pyproject.toml
  ├── configs/        # YAML: default.yaml + variants
  ├── src/<package>/  # code
  ├── tests/          # pytest
  ├── data/           # raw + processed (or the generator)
  ├── models/         # saved models
  ├── results/        # metrics CSVs, plots
  └── runs/           # TensorBoard / experiment logs, if relevant
  ```
- Show the plan (pieces and order) before writing; build one piece at a time.
- **Honest evaluation:** compare against tuned simple baselines on held-out data,
  report domain metrics, use several seeds when results are noisy.
- README ends with a **"Should we ship it?"** conclusion. If the simple baseline
  wins, say so — that is the lesson.
