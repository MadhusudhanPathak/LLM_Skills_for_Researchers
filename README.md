# LLM Skills for Researchers

Socratic questioning skills that help researchers in any field examine their own work: find the weak premise, the hidden assumption, the rival explanation or the overclaimed conclusion before a supervisor, examiner or reviewer does.

The skills are written for [Claude](https://claude.com) (as Claude Code plugin skills), but every file is plain Markdown and the method works with any capable LLM.

## The five skills

Each skill is a framework for one kind of research. Pick the one that matches the main contribution of your work.

| Skill | Use it for | Examples |
|---|---|---|
| `philosophical-research-socratic` | Theses about foundational or normative questions, defended by argument | An ethics chapter, a metaphysics paper, an interpretation of a historical thinker |
| `conceptual-research-socratic` | Definitions, distinctions, frameworks, typologies, taxonomies | A construct definition before measurement, a classification scheme, a conceptual review |
| `theoretical-research-socratic` | Explanatory theories and models | A set of propositions, a mathematical or simulation model, a proposed mechanism |
| `technical-research-socratic` | Methods, algorithms, systems, specifications, proofs | A new algorithm and its evaluation, a system design, a formal proof |
| `empirical-research-socratic` | Findings from observation, experiment or data | A study design, an analysis plan, results and their write-up, qualitative or quantitative |

Philosophical, conceptual and theoretical work form a spectrum from foundational to explanatory. Technical work builds or formalises things; empirical work tests them against data. If your project spans two categories, run one skill for each part.

The skills contain no field-specific content. You supply your field, its conventions and your audience when a session starts.

## How a session works

1. **Intake.** The skill asks for your material and everything behind it: notes, drafts, data, code, earlier feedback, what you have read and tried. It also asks for your purpose, audience, constraints, and a depth setting (light, standard, deep, or "you decide").
2. **Plan.** It summarises what it received, checks that the category fits (and tells you how to adapt if it does not), and proposes a number of rounds. You accept or change the plan.
3. **Rounds.** Each round opens with a summary of your last answers, names one theme, and asks four or five questions about it from different angles. You answer whichever you like, at any length.
4. **Checkpoints.** Every three rounds, a short ledger of what is established, open, in tension and revised.
5. **Audit.** At the end, a structured audit of what survived, what changed, what the work does not yet license, and a list of research tasks with completion criteria. You can ask for a supervision note, examiner's report or reviewer's report instead or as well, or for a single written memo in place of the dialogue.

The questioning is collaborative, not adversarial. Every item in the audit is tagged by origin, so Claude's suggestions never read as your conclusions, and Claude never invents citations or results.

## Installation

### Claude Code (recommended)

Add this repository as a plugin marketplace and install the plugin:

```text
/plugin marketplace add MadhusudhanPathak/LLM_Skills_for_Researchers
/plugin install socratic-research@llm-skills-for-researchers
```

To try it from a local clone instead:

```text
/plugin marketplace add ./path/to/LLM_Skills_for_Researchers
/plugin install socratic-research@llm-skills-for-researchers
```

### Claude Code, without the plugin system

Copy the skills and the shared library so that the shared folder sits two levels above each `SKILL.md`:

```text
~/.claude/skills/philosophical-research-socratic/SKILL.md
~/.claude/skills/conceptual-research-socratic/SKILL.md
~/.claude/skills/theoretical-research-socratic/SKILL.md
~/.claude/skills/technical-research-socratic/SKILL.md
~/.claude/skills/empirical-research-socratic/SKILL.md
~/.claude/shared/            <- copy socratic-research/shared/ here
```

The same layout works inside a project's `.claude/` folder.

### Claude.ai or other platforms that install skills one at a time

Each skill looks for the shared library at `../../shared/` first, and falls back to a `shared/` folder inside its own folder. To package one skill on its own, copy `socratic-research/shared/` into the skill's folder and zip it:

```text
empirical-research-socratic/
  SKILL.md
  shared/
    process/...
    moves/...
    sources.md
```

### Other LLMs

Paste the relevant `SKILL.md` into the conversation, or add it to a project's knowledge, together with the files in `shared/process/` and the `shared/moves/` files the skill lists as core. Then share your material and ask it to begin.

## Using the skills

In Claude Code, the skills trigger on requests such as:

- "Grill my argument in chapter 3."
- "Stress-test this study design before I submit it for ethics review."
- "Poke holes in my definition of resilience."
- "Examine my model like a viva examiner would."
- "Review this proof as a reviewer would."

You can also name a skill directly, for example "use empirical-research-socratic on this draft".

## Repository layout

```text
LLM_Skills_for_Researchers/
  README.md
  LICENSE
  Base_Context.md                 what the project started from
  Skill_Design.md                 how and why the skills were designed
  .claude-plugin/marketplace.json
  socratic-research/              the plugin
    .claude-plugin/plugin.json
    skills/                       the five category frameworks
    shared/
      process/                    how every session runs (11 modules)
      moves/                      reusable research moves (20 modules)
      sources.md                  where the practices come from
```

The original prompt libraries, the two earlier skills they were distilled from, and the background paper are not part of this repository; they are described in `Base_Context.md`.

### The shared library

**Process modules** run every session the same way: `intake`, `claim-sorting`, `turn-mechanics`, `arc`, `contradictions`, `dialogue-safety`, `checkpoints`, `audit-skeleton`, `report-variants`, `writing-style`, `evidence-integrity`.

**Move modules** are banks of reusable research moves, each with question stems grouped by angle, what to watch for, and the artefact it produces: concepts, argument reconstruction, assumptions and gaps, counterexamples and modal reasoning, steelmanning and rivals, normative claims, research question and feasibility, hypotheses and causal models, operationalisation and validity, behaviour and mechanism, formalisation and implementation, study design, statistical inference, reproducibility and generalisation, reactivity and observer effects, adversarial and failure-mode analysis, results to claims, literature and sources, research agenda, and self-scrutiny.

Each category skill says which moves are core for its kind of research, and how every shared element (intake, arc, audit, report variants) applies to it.

## Extending

- **A new category**: add a folder under `socratic-research/skills/` with a `SKILL.md` that follows the structure of the existing five, drawing on the shared modules.
- **A new move**: add a file under `shared/moves/` and reference it from the category skills that should use it.
- **Domain tuning** (for example AI safety and alignment): keep it out of the core skills. A domain companion file listing field-specific failure modes and examples can be supplied at intake.

`Skill_Design.md` records the design decisions and the reasoning behind them, and lists possible extensions.

## Background

These skills consolidate four earlier Socratic prompt libraries and two earlier Claude skills. `Base_Context.md` describes that material in full; the source files themselves are not included in this repository. The sources behind the method, including work on how Socratic questioning can entrench rather than revise belief, are recorded in `socratic-research/shared/sources.md`.

## Licence

MIT. See `LICENSE`.
