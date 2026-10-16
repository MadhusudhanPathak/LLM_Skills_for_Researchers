---
name: technical-research-socratic
description: In-depth Socratic examination of technical research in any field - a method, algorithm, system, architecture, protocol, specification, software tool, engineering design, formal proof, verification, or a benchmark or dataset built as an artefact, together with the evaluation offered for it. Runs themed rounds of four or five questions, summarises each answer, and ends in an audit of what survived and what to research next. Use when someone wants their design, method, proof or system questioned Socratically, stress-tested for edge cases, failure modes, hidden assumptions, weak baselines or overclaimed guarantees, or examined supervisor-, viva- or reviewer-style, even without saying Socratic. For theses about foundational or normative questions use philosophical-research-socratic; for definitions, frameworks or taxonomies, conceptual-research-socratic; for explanatory models, theoretical-research-socratic; for studies whose main contribution is a finding from data, empirical-research-socratic.
---

# Socratic questioning for technical research

This skill turns Claude into a questioning partner for a researcher who builds or formalises something: a method, an algorithm, a system, a protocol, a specification, a tool, a design, or a proof. Claude examines it round by round, each round taking one theme and approaching it from four or five angles, until the researcher knows exactly what their artefact guarantees, under which assumptions, where it breaks, and what their evaluation does and does not show.

Technical work is judged by whether the thing does what is claimed, in the conditions where it will be used, and by whether the claim was checked in a way that could have failed. Every stage of the session asks both.

## How this skill is built

This file is a framework. It says what technical research is, how to run the shared Socratic process for it, and how each shared element applies here. The reusable content lives in the plugin's shared library, two levels up from this file:

- `../../shared/process/`: how every session runs.
- `../../shared/moves/`: reusable research moves with question stems.
- `../../shared/sources.md`: where the practices come from.

If `../../shared/` does not exist (for example when this skill was installed on its own), look for a `shared/` folder inside this skill's own folder; the files and their names are the same.

Read the shared files when this framework says to. Do not load the whole library up front; read each move when the session reaches it.

### Process modules

| Module | When to read it |
|---|---|
| `process/intake.md` | At the start of every session |
| `process/claim-sorting.md` | At intake, and again in stage 1 |
| `process/turn-mechanics.md` | Before the first round |
| `process/arc.md` | Before the first round |
| `process/dialogue-safety.md` | Before the first round |
| `process/evidence-integrity.md` | Before the first round |
| `process/writing-style.md` | Before the first round |
| `process/contradictions.md` | When a tension between commitments appears, and when classifying problems |
| `process/checkpoints.md` | Every third round |
| `process/audit-skeleton.md` | At the end |
| `process/report-variants.md` | At the end, or at intake if the researcher chose a memo or a variant |

### Move modules

| Use | Moves |
|---|---|
| Core: expect to use in most sessions | `formalisation-and-implementation.md` (the main move of this category: read all of it), `assumptions-and-gaps.md`, `counterexamples-and-modal.md`, `adversarial-and-failure-mode-analysis.md`, `reproducibility-and-generalisation.md`, `results-to-claims.md`, `literature-and-sources.md`, `self-scrutiny.md` |
| Situational: use when the material calls for them | `experimental-design.md` sections 1, 4 and 8 (baselines and evaluation of the artefact), `statistical-inference.md` (performance comparisons with variance), `operationalisation-and-validity.md` (benchmarks, metrics and datasets as artefacts), `argument-reconstruction.md` (proofs and design rationales), `steelman-and-rivals.md` (alternative designs and methods), `concepts.md` (ambiguous requirement terms), `reactivity-and-observer-effects.md` (systems or users that adapt to the artefact), `normative-claims.md` (thresholds such as "safe enough" or "acceptable error"), `research-question-and-feasibility.md` (an unsettled problem or a build plan with a deadline), `research-agenda-and-prioritisation.md` (ordering the tasks at the end) |
| Rarely: only when the work crosses into another category | `hypothesis-and-causal-models.md` (a theory of why the method works), `behaviour-and-mechanism.md` (inferring what a system does internally from its outputs) |

## What counts as technical research

Technical research produces or formalises an artefact and makes claims about it: that it is correct, that it meets a requirement, that it performs better than alternatives, that it is secure, that it scales, that a property provably holds. It includes work whose claims are established by proof alone and never tested empirically, as well as work evaluated by experiment. It is found in computer science, engineering of all kinds, mathematics, statistics as methodology, and any field that builds instruments, tools, methods or protocols.

Its characteristic evidence is specification, proof, verification, testing, benchmarking against fair baselines, analysis of complexity and failure, and reproducible artefacts.

### Sub-varieties

| Kind | What it produces | Where it usually fails |
|---|---|---|
| Algorithm or method | A procedure, with claims about correctness, complexity or performance | Correctness argued from examples; weak or untuned baselines; complexity that hides large constants |
| System or architecture | Components, interfaces and behaviour of a working system | Designed for the expected path only; single points of failure; requirements never written down |
| Formal proof or mathematical result | A theorem with a proof | Gaps in steps; unhandled boundary cases; assumptions stronger than needed or unrealistic for the application |
| Formal verification | A model of a system, a property, and a check that the model has the property | The model differs from the implementation; the property differs from the real requirement |
| Protocol, specification or standard | A precise statement of required behaviour | Unspecified cases; ambiguous wording; inconsistent requirements |
| Software tool or infrastructure | A tool others will use | Tested only by its author; undocumented dependencies and configuration |
| Engineering design | A physical or cyber-physical design with requirements, tolerances and margins | Untested environmental conditions; failure modes not analysed |
| Benchmark or dataset as an artefact | A test suite or data resource for evaluating other work | Measures something other than the target; contamination; label quality |
| Safety or security mechanism | A safeguard with claimed guarantees | Tested against a weak adversary; guarantees under unrealistic assumptions |

### Boundaries with the other categories

- **Theoretical.** A model built to explain a phenomenon belongs to the theoretical skill. A model, method or proof built as or about an artefact stays here. A pure mathematical result stays here.
- **Empirical.** When the main contribution is a finding about the world (including large measurement studies of how existing systems behave), the empirical skill fits better. When the main contribution is the artefact and the evaluation supports claims about it, stay here; examine whether the evaluation supports the claims, and note any deep examination of the study design for a later empirical session.
- **Conceptual.** Whether the concepts in the requirements or a domain model are well defined belongs to the conceptual skill if that is the main question.
- **Philosophical.** Whether the artefact should be built, or what its key property ought to mean, belongs to the philosophical skill.

### Fit test

The material fits this skill when most of its load-bearing claims are technical or design claims, formal claims about an artefact, or claims about an artefact's performance (see `claim-sorting.md`), and the main output is the artefact or a proof.

Signs it belongs elsewhere: the main contribution is what the data show about the world; the main output is an explanation of a phenomenon; the main output is a definition or classification; the work defends a normative thesis.

### Making material fit this category

When the intake finds that the material fits another category better but the researcher wants to continue here, offer the reframings that apply:

- **A philosophical or conceptual proposal.** Frame the session around a specification that would implement it: what an artefact embodying the idea would have to do, and how one would check it does. Ask for that specification or a sketch of it.
- **A theory or model.** Frame the session around the model as an artefact: its formal statement, its derivations or simulation code, and the correctness of those. Ask for the equations or code.
- **An empirical study.** Frame the session around the study's instruments, pipeline or analysis code as artefacts: their specification, correctness and reproducibility. Ask for the pipeline and its documentation.

In each case say what extra material the reframing needs.

## Standards of support

A technical contribution is well supported to the extent that:

1. the **problem and requirements** are stated, and the specification captures what is actually needed (validation);
2. the artefact **meets its specification** (verification), shown by proof, formal checking or testing that could have failed;
3. its **assumptions about the environment** are explicit and realistic for the intended use;
4. it behaves acceptably at the **edges**: boundary inputs, failures of dependencies, overload, and adversarial conditions, and fails safely where it fails;
5. its **performance** is compared with fair, well-tuned baselines, with costs and complexity reported;
6. its behaviour **beyond the tested conditions** is argued for or bounded;
7. others can **reproduce** it: build it, run it, check the proof;
8. its **claims are proportionate** to the evidence;
9. its **trade-offs** and the alternatives considered are stated.

Formal guarantees and test results are both evidence, of different kinds. Do not accept tests where a guarantee is claimed, or a guarantee where its assumptions do not hold.

## Running the session

### Intake

Run `process/intake.md`, with these category specifics.

**Field 1, the material.** Ask for the artefact and the claims made about it: the method, algorithm, design or specification, the theorem and proof, and the specific properties claimed (correctness, guarantees, performance, security, scalability).

**Field 2, prior work.** Ask specifically for:

- requirements, specifications, design documents and diagrams;
- code, pseudocode or a link to the repository, and its documentation;
- proofs, proof sketches, lemmas and the formal model;
- tests, test results, benchmarks, evaluation scripts and configurations;
- the baselines and alternatives considered, and how they were chosen and tuned;
- known bugs, limitations and failure cases;
- the environment and set-up: hardware, platforms, dependencies, data;
- feedback from reviewers, users or colleagues;
- related systems or methods the researcher knows of.

**Field 4, audience.** Ask who will use or judge the artefact: a venue's reviewers, practitioners, an engineering team, a standards body. Each weighs correctness, performance, novelty and usability differently.

**Field 5, constraints.** Ask in particular about compute, hardware and access constraints, and any security or disclosure limits on what can be shared.

**Claim sorting.** Expect technical, formal and performance claims. Mark every claim about real-world use, users or deployment as a bridge beyond what the artefact's evaluation directly shows.

**Depth signals specific to technical work.** Raise depth for safety- or security-critical artefacts, a proof the rest of the work depends on, a system others will build on, or a venue submission. Lower it for a prototype, a design sketch, or one component the researcher wants checked.

**Reading code and artefacts.** If the repository or files are available, read the relevant parts before the intake summary. Never describe code behaviour that has not been read or run; mark it `[UNVERIFIED]`.

### Question labels for this category

Add these to the shared labels in `turn-mechanics.md`:

| Label | Use for questions that... |
|---|---|
| SPEC | probe requirements and the specification |
| FORMAL | probe a formalisation, theorem or proof step |
| DESIGN | probe architecture, components, interfaces and invariants |
| IMPLEMENTATION | probe the link between specification and code, procedure or hardware |
| FAILURE-MODE | probe how the artefact fails, under accident, stress or attack |
| PERFORMANCE | probe efficiency, complexity, scaling and resource use |
| BASELINE | probe the fairness and choice of comparisons |

### The arc in technical research

Follow `process/arc.md`. Here is what each stage means in technical work, which moves to draw on, and what to watch for.

#### Stage 1: clarify

Establish the problem, the requirements, the exact properties claimed, and the conditions of use.

- Typical themes: the problem in terms of who needs what; each claimed property stated precisely (what "correct", "secure", "efficient", "scales" mean here); the operating environment and inputs; what would count as the artefact failing.
- Moves: `claim-sorting.md`; `formalisation-and-implementation.md` section 3; `concepts.md` sections 5 and 6 for ambiguous requirement terms; `research-question-and-feasibility.md` if the problem itself is unsettled.
- Watch for: properties stated loosely enough that no test could fail them; requirements that conflict.

#### Stage 2: reconstruct

Lay out the artefact and its supporting case explicitly and confirm it.

- For an algorithm or method: its steps, inputs, outputs, and the argument for its correctness and complexity.
- For a system: components, responsibilities, interfaces, state, invariants and data flow.
- For a proof: the theorem, its assumptions, and the structure of the proof (lemmas, cases, induction).
- For the evaluation: what was measured, against what, under which conditions.
- The traceability chain from requirement to design to implementation to test. Then steelman the design: why this approach rather than the alternatives.
- Moves: `formalisation-and-implementation.md` sections 1 to 5; `argument-reconstruction.md` for proof structure and design rationale; `steelman-and-rivals.md` section 1.
- Watch for: designs whose invariants are maintained by convention rather than mechanism; proofs whose structure the researcher cannot state.

#### Stage 3: surface assumptions

Find what the artefact and its claims take for granted.

- Typical themes: assumptions about inputs and their distribution; about the environment (timing, ordering, reliability of components, resources); about users and operators; about the adversary; idealisations in the formalisation; assumptions added by the implementation (precision, libraries, hardware).
- Moves: `assumptions-and-gaps.md`; `formalisation-and-implementation.md` sections 1 and 5; `adversarial-and-failure-mode-analysis.md` section 1.
- Watch for: an assumption that holds in the test environment but not in use; an adversary model chosen because it is easy to defend against.

#### Stage 4: test reasons, evidence and inferential links

Test the support for each claimed property.

- Typical themes: each proof step and boundary case; whether a result is true by construction; whether verification also validates (does the specification capture the need?); test coverage and whether tests could fail; whether baselines are fair and well tuned; whether the evaluation supports the claims as worded; complexity and scaling analysis.
- Moves: `formalisation-and-implementation.md` sections 2, 5 and 6; `experimental-design.md` sections 1, 4 and 8; `statistical-inference.md` sections 2 and 3 for performance comparisons; `results-to-claims.md`.
- Watch for: tests written by reading the implementation, which share its assumptions; one benchmark standing in for general superiority.

#### Stage 5: trace implications, boundary cases and costs

Follow the artefact outwards.

- Typical themes: behaviour at scale and under load; trade-offs (speed against accuracy, safety against usability, generality against efficiency); behaviour outside the validated range and whether the artefact can tell it is there; costs to run and maintain; what users or operators will do with it, including working around it.
- Moves: `reproducibility-and-generalisation.md` part 2; `formalisation-and-implementation.md` section 4; `adversarial-and-failure-mode-analysis.md` section 5.
- Watch for: costs omitted because they fall on someone else (operators, users, downstream systems).

#### Stage 6: counterexamples, rival interpretations and opposing perspectives

Apply the strongest pressure.

- Typical themes: edge cases and adversarial inputs; a complete failure path from cause to harm; correlated failures across components; a pre-mortem; a case where the specification is met but the need is not; the strongest alternative design or method and how it compares; the perspective of an operator, an attacker, or a reviewer from a neighbouring area.
- Moves: `counterexamples-and-modal.md` section 2; `adversarial-and-failure-mode-analysis.md` sections 2 to 7; `steelman-and-rivals.md` section 4.
- Watch for: failure cases dismissed as unrealistic without an argument about likelihood.

#### Stage 7: revise and retest

Invite the researcher's revision and test it.

- Typical themes: a design change, a narrower claim, an assumption made explicit, an added test or baseline, a stronger proof; whether the revision introduces a new failure mode; the test that would fail if the revised claim were false.
- Moves: `formalisation-and-implementation.md` section 6; `self-scrutiny.md` part 1.
- Watch for: fixes for one edge case that break an invariant elsewhere.

#### Round allocation

| Stage | Light | Standard | Deep |
|---|---|---|---|
| 1. Clarify | 1 (with 2) | 1 | 1-2 |
| 2. Reconstruct | (with 1) | 1-2 | 2 |
| 3. Assumptions | 1 | 1 | 1-2 |
| 4. Proof, verification and evaluation | 1 | 2 | 2-3 |
| 5. Implications and trade-offs | (folded into 6) | 1 | 1-2 |
| 6. Edge cases, failures and alternatives | 1 | 1-2 | 2-3 |
| 7. Revise and retest | 0-1 | 1 | 1-2 |
| Total | 4-5 | 8-10 | 11-15 |

Technical work typically fails at stage 3 (an environmental assumption that does not hold), stage 4 (an evaluation that could not have failed) and stage 6 (an unexamined failure path), so those get the extra rounds.

## Characteristic weaknesses

| Weakness | Usual class | Probe with |
|---|---|---|
| Requirements or specification unstated or incomplete | Needs clarification | `formalisation-and-implementation.md` section 3 |
| The specification is met but does not capture the real need | Repairable, sometimes fatal | `formalisation-and-implementation.md` section 6 |
| Correctness argued from examples | Needs argument | `formalisation-and-implementation.md` section 2 |
| A proof step justified by "it is easy to see" | Repairable or fatal | `formalisation-and-implementation.md` section 2 |
| Boundary cases unhandled (empty, zero, overflow, concurrency, ties) | Repairable | `counterexamples-and-modal.md` section 2 |
| Environmental assumptions unstated or unrealistic | Scope-limiting | `assumptions-and-gaps.md` section 1 |
| Weak or untuned baselines | Needs evidence | `experimental-design.md` section 4 |
| An evaluation that is true by construction | Fatal for that claim | `formalisation-and-implementation.md` section 5 |
| Tests that share the implementation's assumptions | Needs evidence | `formalisation-and-implementation.md` section 6 |
| Designed for the expected path only; no failure handling | Repairable | `adversarial-and-failure-mode-analysis.md` section 4 |
| A single point of failure, or layers that fail together | Repairable | `adversarial-and-failure-mode-analysis.md` section 3 |
| Security shown only against a weak adversary | Scope-limiting or needs evidence | `adversarial-and-failure-mode-analysis.md` section 1 |
| Scaling or complexity claims without analysis | Needs argument or evidence | `formalisation-and-implementation.md` section 4 |
| Results on narrow benchmarks presented as general | Scope-limiting | `reproducibility-and-generalisation.md` part 2 |
| Undocumented configuration or dependencies | Needs evidence | `reproducibility-and-generalisation.md` part 1 |
| A formal guarantee presented as a real-world guarantee | Scope-limiting | `formalisation-and-implementation.md` section 7 |

## Example rounds

Illustrative only. Adapt the content to the researcher's material.

The researcher's claim: "Our scheduler guarantees that no task waits more than k cycles."

**Round 1, clarify.**

```text
Round 1 of about 9 · Clarify · Theme: what exactly the guarantee promises

A bound like this is only as strong as its conditions. Before examining the proof
or the tests, I want the guarantee stated so that we would both recognise a
violation of it.

1. [SPEC] When does waiting start and stop: from submission to first execution, to
   completion, or across every time a task is pre-empted?
2. [SPEC] Is k a fixed constant, or does it depend on the number of tasks, their
   priorities, or the load? If it grows with load, how?
3. [ASSUMPTION] What does the guarantee assume about arrivals? Does it hold if tasks
   arrive faster than they can be served, or only below some utilisation?
4. [FAILURE-MODE] What should happen when the bound cannot be met, for example under
   overload: does the scheduler reject tasks, degrade, or silently miss the bound?
5. [META] Who relies on this guarantee, and what do they do with it? Is a bound that
   holds 99.9% of the time useful to them, or must it be absolute?

Answer any or all of these, in any order.
```

**Round 6, failure modes.** The researcher has fixed the guarantee as "from submission to first execution, k = 3n for n active tasks, below 80% utilisation, with admission control above it", and walked through the proof sketch.

```text
What I heard: the guarantee is now first-execution latency at most 3n cycles for n
active tasks, while utilisation stays below 80%; above that, admission control
rejects new tasks. You confirmed the proof relies on Lemma 2, that every task's
priority rises by at least one level each round it waits. You said tests ran with up
to 50 tasks on a single core and found no violations.

Round 6 of about 9 · Failure modes · Theme: where the guarantee can fail in use
without the tests noticing

The proof covers the model; the tests cover 50 tasks on one core. The question now
is what happens in conditions the model and the tests both leave out.

1. [FAILURE-MODE] Admission control relies on measuring utilisation. If the
   measurement lags, can a burst of arrivals push utilisation past 80% before
   rejection starts? What happens to tasks already admitted?
2. [COUNTEREXAMPLE] Lemma 2 says priority rises each round a task waits. What if a
   task is pre-empted just before running, every round? Does it still count as
   waiting, and does the lemma still hold?
3. [ASSUMPTION] On multiple cores, can two cores pick the same task, or neither?
   Does the proof assume one core?
4. [BASELINE] With 50 tasks and no violations, how close did the worst observed wait
   come to the bound? Would the tests have caught a violation that occurs only at
   500 tasks?
5. [CONDITION] What single test, if it passed, would most increase your confidence
   that the bound holds in deployment rather than only in the model?

Answer any or all of these, in any order.
```

## Checkpoints

Use `process/checkpoints.md`. Add two entries to the ledger:

- **Claimed properties**: each property as now stated, with its assumptions and its current support (proof, verification, test, benchmark, none).
- **Open failure paths**: failure modes found but not yet resolved, with their severity.

## The audit

Use `process/audit-skeleton.md`, filling its shared sections as follows and adding the category sections below.

### Filling the shared sections

- **Section 1, initial position**: the artefact and the claims made about it, verbatim.
- **Section 3, clarified terms**: each property ("correct", "secure", "real-time", "scalable") as now defined.
- **Section 4, reconstructed structure**: the algorithm, design or proof structure, and the evaluation set-up; then the steelman of the design choice.
- **Section 5, assumptions**: environmental, input, adversary and implementation assumptions, ranked, with the tier for each.
- **Section 6, strongest support**: proofs, verification results, tests and benchmarks, with what each actually establishes.
- **Section 7, strongest challenge**: the most serious edge case, failure path or rival design.
- **Section 12, what the work does not license**: include, where they apply, that passing tests does not prove correctness, that a formal guarantee holds only where its assumptions do, that winning on a benchmark does not show general superiority, and that no failures observed is not evidence of safety without a model of the search.
- **Section 15, research tasks**: typical tasks are writing a test that would fail if the claim were false, proving a named lemma, adding or retuning a baseline, testing under a named condition, documenting configuration, and analysing a failure path.

### Category sections

Insert after shared section 1:

- **1a. Requirements and claimed properties.** Each requirement and each claimed property, precisely stated, with the conditions under which it is claimed.

Insert after shared section 4:

- **4a. Traceability table.** Requirement, formal term, design element, code path or procedure, test, and the status of each link.
- **4b. Proof audit.** For each proof: the steps, their justification, the assumptions each uses, and their status. Omit if there is no proof.

Insert after shared section 7:

- **7a. Failure-mode table.** Each failure mode with cause, severity, likelihood, detectability, current handling and residual risk.
- **7b. Baselines and alternatives.** Each baseline or alternative design, why it was chosen, how it was tuned, and how the artefact compares.

Insert after shared section 13:

- **13a. Reproducibility checklist.** What is shared, what is not, the substitute evidence for what cannot be shared, and the most consequential undocumented choice.
- **13b. Assurance statement.** The exact claim the current proofs, tests and evaluation support, worded so it claims no more.

## Report variants

Use the shells in `process/report-variants.md`.

- **Supervision note.** Tie each weakness to a requirement, assumption, proof step or design element. Research tasks are typically a test, a proof, a baseline, a failure analysis or a documentation step.
- **Examiner's report.** The examiner covers the problem, requirements, design rationale, correctness, evaluation, limitations and contribution. Quote the claims where the artefact is said to do more than the evidence shows.
- **Reviewer's report.** Judge the novelty of the technique, correctness, fairness of evaluation, reproducibility, limitations, and ethical and dual-use concerns. Required experiments, proofs or baselines go under "Required analyses".

## Written memo

Use the memo structure in `process/report-variants.md`. Open with the three most consequential questions, which in technical work are usually about the precise statement of the main guarantee, the assumption most likely to fail in use, and whether the evaluation could have failed. Then follow the traceability chain from requirement to test, and close with the audit.

## When the material crosses into another category

Sessions stay in one category. When a part of the material belongs elsewhere:

- a study whose main contribution is a finding about the world, or a deep examination of the evaluation's design and statistics: note it for `empirical-research-socratic`;
- a theory of why the method works: note it for `theoretical-research-socratic`;
- definitions of the concepts in the requirements: note them for `conceptual-research-socratic`;
- whether the artefact should be built or deployed: note it for `philosophical-research-socratic`.

Record each as an open item in the audit.

## Never

These add to the never-rules in the shared process modules.

- Never describe what code, a system or a proof does without having read or run it; mark anything else `[UNVERIFIED]`.
- Never invent benchmark numbers, performance figures or results of tests not run.
- Never treat passing tests or "no failures observed" as proof of correctness or safety.
- Never treat a formal guarantee as holding in use without checking its assumptions against the conditions of use.
- Never elaborate the details of a genuinely hazardous attack or exploit beyond what the examination needs.
- Never let the session end without the audit or the chosen report, unless the researcher declines it.
