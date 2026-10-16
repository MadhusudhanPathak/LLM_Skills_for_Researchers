# Skill design

This document records how the five Socratic research skills were designed: the conversation that shaped them, the decisions taken at each step, the reasons given, and the architecture that resulted. `Base_Context.md` describes the material the project started from; this document starts where that one ends.

## 1. The brief

The starting request was to develop skills from all of the material and context provided by Isobel (Bella) Smith GitHub: https://github.com/bgsbgsbgs42 LinkedIn: https://www.linkedin.com/in/bella-smith-/. Her base part was a bit fragmented and als a bit too specific in many angles, and therefore one of the aim was to make it more generic for people with different background and usecases. The first step was an analysis of the existing files before any design work.

## 2. The first analysis

The analysis found two finished skills (`idea-refine` and `socratic-method`) sitting beside the four prompt libraries they had been distilled from, plus a background paper. Its main findings, set out in detail in `Base_Context.md`, were:

- `idea-refine` was already close to domain-general.
- `socratic-method` was well engineered but locked to two subject modes, philosophy and technical AI safety, with a third mode for work that bridges them. Researchers in other fields had no mode that fit.
- The loose prompt libraries duplicated content that had already been absorbed into the skill's reference files, so the folder held the same ideas at two levels of refinement.
- The two skills shared machinery (assumption ranking, stress tests, audits, null-result questions) but each had built its own version.
- Packaging was inconsistent: folder names with spaces and "-v2" suffixes, no top-level README, nothing tying the plugins together.

Two ways of generalising the Socratic skill were put forward: widen the fixed modes into a few broad research types, or drop fixed modes and have the model infer the questioning style from the material. I chose the first, in a more developed form described in section 4.

## 3. Line-by-line feedback on the philosophical prompt bank

I then reviewed `Reusable Socratic Prompts for Philosophical Research.md` and gave six specific changes. These became the core interaction rules for every skill in the final set.

### 3.1 Replace the single question with a themed round

Original rule: "Ask one main question at a time and wait for an answer."

I's objection: a single question "is mostly not able to ask different angles" and "gets harder to write". The replacement is a round built around one central theme, concern or aspect, with four or five questions diverging from it. The researcher answers the round as a whole.

This reverses one of the old skill's strongest principles, which held that several questions let the researcher answer the easiest and drop the hard one. The new design handles that risk differently: every question in a round serves the same theme, so no question can carry the round away from the issue that matters, and the summary that opens the next round records which questions went unanswered so they can be returned to.

### 3.2 Summarise the researcher's answers after every round

New rule: after each round, briefly articulate and summarise what the researcher said, and show it to them before the next round begins. This makes the record of the dialogue visible as it grows, lets the researcher correct a misreading early, and replaces the old "take stock" step with something more explicit.

### 3.3 Remove two judgement-heavy rules

Removed:

- "Do not answer questions on the researcher's behalf."
- "Do not use disguised advice, stacked questions or rhetorical questions whose intended answer is obvious."

I's reason: these "require too much theory of mind on the model's end", and models are not good at applying them. Judging whether a question is leading, or whether a phrase amounts to advice, requires the model to model the researcher's reading of its own words. The final design relies instead on mechanical practices that can be checked on the page: the themed round, the summary, the question labels, and the instruction to stop after the questions.

### 3.4 Let the model decide the length of a session

Original: "Conduct an adaptive dialogue of approximately [NUMBER] substantive turns."

I's change: let the model judge how many turns are needed, and give it the depth required and the purpose, scope and audience of the research instead of a number. Section 5 describes how this developed into the depth dial and the estimate-and-confirm step.

### 3.5 Reorder the arc and remove one stage

The original eight-stage order was: clarify, reconstruct, surface assumptions, test reasons and evidence, introduce counterexamples and rival views, trace implications, question whether the research question is well formed, revise and retest.

Two changes:

- Counterexamples, rival interpretations and opposing perspectives move to just before revision. They become the last and strongest pressure applied before the researcher is asked to revise.
- "Question whether the original research question is well formed" is removed from the arc entirely.

The resulting seven-stage arc is used by every skill:

1. Clarify the central thesis, terms and scope.
2. Reconstruct the argument, model, design or chain, and confirm it.
3. Surface explicit and implicit assumptions.
4. Test reasons, evidence and inferential links.
5. Trace implications, boundary cases and costs.
6. Introduce counterexamples, rival interpretations and opposing perspectives.
7. Invite revision and retest the revised position.

The research-question examination survives as a shared module (`research-question-and-feasibility.md`) that a session draws on only when the intake shows the question itself is unsettled, or when the researcher asks for it. It is not a default stage.

### 3.6 Apply the round rule everywhere

Every instance of "ask one question at a time" in the material was to be replaced by the themed round. In the final design this is enforced in one place, `shared/process/turn-mechanics.md`, which every skill loads.

### 3.7 From thirty-two prompts to one method

I's view of the remaining prompts: the smaller ones "are great when the above changes are made but don't stand independently. Rather they can be modular elements used by the first main prompt to work properly." The extended examination therefore became the backbone of every session, and the narrower prompts became modular research moves that the backbone calls on.

## 4. Five categories instead of two modes

I then set the target: five Socratic questioning skills, "specifically for Claude but also useful in general", usable by "anyone irrespective of their background":

1. Philosophical research
2. Conceptual research
3. Theoretical research
4. Technical research
5. Empirical research

Two constraints came with this:

- **No domain content in the skills.** "The specific use case of such type of research, that is in AI safety, or AI alignment etc. will be done by I at the time of use. Don't embed anything regarding their specific use case in the main skill."
- **Shared modules.** "For all these 5 skills there are a lot of common modular elements. I want you to abstract them and keep them separately that would be called upon on use in each skill."

And one new requirement: when a session starts, I is prompted for all the major placeholders and also for "all the rough work, drafts and base setup work already done in the research project".

## 5. Designing by Socratic dialogue

Before building anything, I asked to be questioned Socratically to settle the remaining design elements. The rounds used the format just agreed: one theme, several diverging questions, then a summary of the answers before the next theme.

### Round 1: what distinguishes the five categories

Questions asked: whether philosophical, conceptual and theoretical form a spectrum or are synonyms; whether technical and empirical are two halves of applied science; whether sessions are single-category; how researchers in unrelated fields would map onto the categories; and whether any mode had been left out.

Answers:

- **A spectrum.** Philosophical work is foundational and normative; conceptual work is definitional and taxonomic; theoretical work builds models and explanations.
- **Technical and empirical mostly pair up.** Technical work builds or formalises the thing; empirical work tests it with experiments and data. Technical work is not limited to this, though: it also covers formal proofs and system or architecture design that may never be tested empirically. "Keep it open."
- **One category per session.** A paper or project normally belongs to one of the five. Work that spans two can be done in parts by running a second skill afterwards. No automatic handoff between skills is needed.
- **General use, not mapped to particular fields.** The skills should serve historians, clinicians, economists and biologists alike without being tailored to any of them. If any domain tuning is wanted later, it would be for AI safety or alignment, but it does not belong in the main skills.
- **Exactly these five, treated as exhaustive for now.** More categories may be added later.

### Round 2: the shared core and the intake

Questions asked: whether the shared mechanics should be one shared file or copied into each skill; whether the proposed intake fields were right; whether the intake should check that the chosen category fits; whether depth should be inferred or dialled; and whether audits should be shared or separate per category.

Answers:

- **No standalone skills.** The design should consist of "multiple modules of research traits and capabilities", with each category skill using them "as dependencies". The category skills act as frameworks for their kind of research, containing the instructions for how to do that research using the shared modules. "Make it as modular as possible, and abstract out as much general skills useful in all categories as possible."
- **The intake fields are general already.** Material; purpose, stage and output; audience or judge; constraints; prior work. No changes.
- **Yes to the category check, without forcing a switch.** If the material fits another category better, say so, but also invite I to continue with the skill they chose and guide them on how to make their intake fit that category.
- **Depth from every signal, plus a dial, plus a stated estimate.** The model infers depth from everything available (purpose, scope, audience and more), the intake offers an explicit light / standard / deep dial, and after its analysis the model tells I how many rounds it expects to need. I can accept or override.
- **Shared base, category-specific application.** "The base idea and rigour of audits should be shared and general for all categories", but each category skill specifies how to use the shared audit, and the same applies to report variants. Then the principle was generalised: "I want the base idea of point 5 applied to all such elements and traits of research and not just audit."

That last answer fixed the architecture. Every shared element is written once, generally, and every category skill says how that element applies in its own kind of research.

## 6. From proposal to final architecture

### 6.1 First proposal

The first architecture proposal had five short `SKILL.md` files and a shared library: eleven process modules (intake, turn mechanics, arc, contradictions, dialogue safety, checkpoints, audit skeleton, report variants, writing style, evidence integrity, plus a claim-sorting step) and fifteen move modules. It included a table of which moves each category treated as core and which it used lightly.

### 6.2 I's revisions

I accepted most of it and asked for two changes.

1. **Category skills must be comprehensive, not short.** Each `SKILL.md` should "stick to what I mentioned before" (use the shared modules as dependencies and say how to apply them) but should also be "detailed about the things they are concerned with... detailed and comprehensive. The framework should cover each and every aspect of that category of research."
2. **The module list was too thin.** It "doesn't seem to cover major traits and all aspects for all the categories... there can be more of it to make it all robust and reliable."

The response to the first point was to separate two kinds of content. The question stems and mechanics that recur across categories live once in `shared/`. Everything that makes a category distinct lives in full in its own `SKILL.md`: what counts as that kind of research and its sub-varieties, how each arc stage plays out in it, the standards of support it answers to, its characteristic failure modes, its intake specifics, worked example rounds, and how to fill the audit and report templates.

The response to the second was to add modules that the source material covered but the first proposal had left out or locked to AI safety:

| New or expanded module | What it covers | Source in the old material |
|---|---|---|
| `claim-sorting.md` (process) | Sorting material by kind of claim before questioning, so each claim meets the right standard | `combined.md` section 2; the sixty-prompt library's "separate the levels of claim" |
| `research-question-and-feasibility.md` | Research-question examination, contribution, theory of change, feasibility against deadline and resources | Philosophical and technical prompt banks; `idea-refine` stress tests |
| `behaviour-and-mechanism.md` | Separating what was observed from what is inferred about the underlying process | Technical prompt bank; `technical-ai-safety.md` section 6 |
| `reactivity-and-observer-effects.md` | The measurement changing what is measured | Generalised from evaluation awareness and sandbagging |
| `adversarial-and-failure-mode-analysis.md` | Stress-testing against a motivated adversary or worst case | Generalised from security threat models and red-teaming |
| `research-agenda-and-prioritisation.md` | Sequencing projects, decision points, converting uncertainty into an agenda | Technical bank prompt 30; sixty-prompt library prompts 42 and 47 |
| `operationalisation-and-validity.md` (expanded) | Adds validity theory (construct, internal, external, ecological, statistical conclusion) and reliability | Technical bank evaluation prompts |
| `reproducibility-and-generalisation.md` (expanded) | Adds the generalisation ladder and distribution shift | Toy-model audit; distribution-shift prompts |

I approved the expanded plan and asked for this document and `Base_Context.md` to be written before building.

## 7. Final architecture

```text
socratic-research/                       the plugin
  .claude-plugin/plugin.json
  skills/
    philosophical-research-socratic/SKILL.md
    conceptual-research-socratic/SKILL.md
    theoretical-research-socratic/SKILL.md
    technical-research-socratic/SKILL.md
    empirical-research-socratic/SKILL.md
  shared/
    process/                             how every session runs
      intake.md
      claim-sorting.md
      turn-mechanics.md
      arc.md
      contradictions.md
      dialogue-safety.md
      checkpoints.md
      audit-skeleton.md
      report-variants.md
      writing-style.md
      evidence-integrity.md
    moves/                               reusable research moves
      concepts.md
      argument-reconstruction.md
      assumptions-and-gaps.md
      counterexamples-and-modal.md
      steelman-and-rivals.md
      normative-claims.md
      research-question-and-feasibility.md
      hypothesis-and-causal-models.md
      operationalisation-and-validity.md
      behaviour-and-mechanism.md
      formalisation-and-implementation.md
      experimental-design.md
      statistical-inference.md
      reproducibility-and-generalisation.md
      reactivity-and-observer-effects.md
      adversarial-and-failure-mode-analysis.md
      results-to-claims.md
      literature-and-sources.md
      research-agenda-and-prioritisation.md
      self-scrutiny.md
    sources.md                           where the practices come from
```

### 7.1 The three layers

- **Process modules** define how a session runs, identically in every category. They are loaded at the start (intake, claim sorting, turn mechanics, arc, dialogue safety, evidence integrity, writing style) or at the moment they are needed (contradictions when a tension appears, checkpoints every few rounds, the audit and report variants at the end).
- **Move modules** are banks of reusable research moves. Each one says when to use it, offers question stems grouped by angle so that a themed round can draw four or five different angles from it, lists what to watch for, and names the artefact it feeds into the audit. Moves are written without reference to any field or category.
- **Category skills** are the frameworks. Each one tells Claude what its kind of research is, how to run the shared process for it, which moves are core, situational or rarely needed, and how each shared element (intake, arc, audit, variants and so on) applies in that category.

### 7.2 How a session runs

1. **Intake.** One message asking for the material and all the rough work behind it (notes, drafts, outlines, data, code, set-up, earlier feedback), the purpose, stage and intended output, the audience or judge, the constraints, what has already been read or tried, a depth setting (light, standard, deep, or "you decide"), and dialogue or written memo.
2. **Intake summary.** Claude restates what it received, lists the assumptions it is making for anything missing, sorts the claims by kind, and checks the category fit. If the material belongs better in another category, Claude says which and why, and also explains how to reframe the material to continue in the chosen skill.
3. **Plan.** Claude states its estimated number of rounds, how they divide across the arc, and where checkpoints fall. I accepts or changes it.
4. **Rounds.** Each round opens with a summary of the last answers, names one theme and the stage it belongs to, says why the theme matters now, asks four or five labelled questions that approach the theme from different angles, and stops.
5. **Checkpoints.** Every three rounds, a ledger of what is established, still open, in tension and revised, the next most consequential theme, and rounds used against the estimate, with a revised estimate if needed.
6. **Ending.** An audit built from the shared skeleton plus the category's own sections, with every item tagged by origin, and open questions converted into research tasks with completion criteria. A report variant (supervision note, examiner's report, reviewer's report) replaces or follows it if I asked for one.

### 7.3 How the categories differ

| Category | What it produces | Core moves | Standard of support |
|---|---|---|---|
| Philosophical | Theses about foundational or normative questions, defended by argument | concepts, argument-reconstruction, assumptions-and-gaps, counterexamples-and-modal, steelman-and-rivals, normative-claims, literature-and-sources | Validity and soundness of argument, fit with considered judgements, dialectical strength against the best opposing view |
| Conceptual | Definitions, distinctions, frameworks and taxonomies | concepts, assumptions-and-gaps, counterexamples-and-modal, steelman-and-rivals, operationalisation-and-validity | Clarity, coverage of cases, discrimination between cases that matter, usefulness for the stated purpose |
| Theoretical | Explanatory models and theories | hypothesis-and-causal-models, argument-reconstruction, assumptions-and-gaps, counterexamples-and-modal, steelman-and-rivals, results-to-claims | Explanatory power, coherence, scope, testable consequences, robustness of conclusions to modelling assumptions |
| Technical | Methods, algorithms, systems, specifications and proofs | formalisation-and-implementation, assumptions-and-gaps, counterexamples-and-modal, adversarial-and-failure-mode-analysis, reproducibility-and-generalisation, results-to-claims | Correctness against specification, adequacy of the specification, performance against fair baselines, behaviour at the edges |
| Empirical | Findings from observation, experiment and data | experimental-design, statistical-inference, operationalisation-and-validity, behaviour-and-mechanism, reactivity-and-observer-effects, reproducibility-and-generalisation, results-to-claims | Validity of measures, strength of design against rival explanations, calibrated inference, honest generalisation |

`literature-and-sources`, `self-scrutiny` and `research-question-and-feasibility` are available in every category.

## 8. Decisions and reasons

| Decision | Reason |
|---|---|
| Themed rounds of four or five questions | One question cannot approach a concern from several angles, and is harder to write well |
| Summary at the start of every round | Makes progress visible, lets the researcher correct misreadings, gives the audit a running record |
| No rules that require judging one's own phrasing | Models apply theory-of-mind rules unreliably; mechanical structure is checkable |
| Depth inferred, dialled and confirmed | Researchers cannot guess a turn count; the model can estimate from signals, and I keeps the final say |
| Counterexamples and rivals placed just before revision | Strongest pressure comes last, immediately before the researcher is asked to revise |
| Research-question examination moved out of the default arc | The arc examines the work as it stands; questioning the question is available on demand |
| Five categories, one per session | Projects normally belong to one category; cross-category work is done in parts |
| Category check offers rather than forces a switch | The researcher may have reasons for their choice; the skill should help them use it well |
| Shared modules written once, applied per category | Removes the duplication that fragmented the original material; keeps every category consistent |
| Comprehensive category skills | Each kind of research has its own sub-varieties, standards and failure modes, which a short pointer file cannot carry |
| No domain content in the skills | Users from any field supply their own domain context at intake |
| Collaborative rather than adversarial stance | Evidence collected for the old skill shows adversarial questioning tends to entrench rather than revise belief |
| Never invent sources; tag every audit item by origin | A fabricated citation survives into the researcher's draft; untagged suggestions read as the researcher's own conclusions |

## 9. Tensions noted during design

- **Maieutics without the rule against answering for the researcher.** The method's aim is for the researcher to produce the ideas. With the explicit rule removed, the design protects that aim structurally: rounds end in questions and stop, summaries report only what the researcher said, and Claude gives its own view only when asked, labelled as its own.
- **Several questions per round versus the risk of dodging the hard one.** Handled by keeping every question on one theme and by recording unanswered questions in the next summary.
- **Domain neutrality versus I's own field.** I works in AI safety and alignment. The skills contain no domain material; the intake asks for the field and its conventions, and a domain-specific companion could be added later without changing the core.
- **One category per session versus mixed material.** The claim-sorting step identifies the parts of the material that belong elsewhere and records them as open items for a later session with another skill.
- **Shared files and single-skill installation.** Category skills reach the shared library by relative path (`../../shared/`). That works when the whole plugin is installed. Each skill also falls back to a `shared/` folder inside its own folder, so a skill installed on its own works if `shared/` is copied into it; the README explains how.

## 10. Possible extensions

- Further categories if the five prove insufficient, for example interpretive or historical research treated separately from philosophical work.
- Domain companions that add field-specific failure modes and examples (AI safety and alignment was named as the first candidate) loaded alongside a category skill.
- Evaluation prompts for testing whether each skill triggers correctly and follows the round format.
- A packaging script that bundles `shared/` into each skill for platforms that install skills one at a time.
