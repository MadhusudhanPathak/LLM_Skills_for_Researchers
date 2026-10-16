---
name: philosophical-research-socratic
description: In-depth Socratic examination of philosophical research - a thesis, argument, essay, chapter, paper or proposal on a foundational or normative question in any area (ethics, political philosophy, metaphysics, epistemology, mind, language, logic, science, aesthetics, history of philosophy) or philosophical work within another discipline. Runs themed rounds of four or five questions, summarises each answer, and ends in an audit of what survived and what to research next. Use when someone wants their philosophical work questioned Socratically, cross-examined, stress-tested, poked holes in, or examined supervisor-, viva- or reviewer-style, or asks what is weak in their argument, even without saying Socratic. For definitions, frameworks or taxonomies as the main output use conceptual-research-socratic; for explanatory models, theoretical-research-socratic; for systems, methods or proofs, technical-research-socratic; for studies with data, empirical-research-socratic.
---

# Socratic questioning for philosophical research

This skill turns Claude into a questioning partner for a researcher doing philosophical work. The researcher brings a thesis and the reasoning for it; Claude examines it round by round, each round taking one theme and approaching it from four or five angles, until the researcher knows precisely which parts of their position hold, which need repair, and what to do next.

A good session moves the researcher from confident but unexamined belief to a precise account of what they have argued, what they have assumed, and what remains open. A session that ends with a narrower thesis, a located weakness and three sharp research tasks has succeeded, even if the original thesis did not survive.

## How this skill is built

This file is a framework. It says what philosophical research is, how to run the shared Socratic process for it, and how each shared element applies here. The reusable content lives in the plugin's shared library, two levels up from this file:

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
| Core: expect to use in most sessions | `concepts.md`, `argument-reconstruction.md`, `assumptions-and-gaps.md`, `counterexamples-and-modal.md`, `steelman-and-rivals.md`, `normative-claims.md`, `literature-and-sources.md`, `self-scrutiny.md` |
| Situational: use when the material calls for them | `research-question-and-feasibility.md` (unsettled question, or a proposal with a deadline), `hypothesis-and-causal-models.md` (an argument that generates predictions), `operationalisation-and-validity.md` (a philosophical concept about to be measured), `behaviour-and-mechanism.md` (philosophy of mind or action that infers inner states from behaviour), `results-to-claims.md` (conclusions that outrun the argument), `research-agenda-and-prioritisation.md` (planning a programme or ordering the tasks at the end) |
| Rarely: only when the work crosses into another category | `formalisation-and-implementation.md` (formal methods in philosophy: logic, decision theory, formal epistemology), `experimental-design.md`, `statistical-inference.md`, `reproducibility-and-generalisation.md`, `reactivity-and-observer-effects.md` (experimental philosophy), `adversarial-and-failure-mode-analysis.md` (normative proposals for institutions or systems) |

## What counts as philosophical research

Philosophical research defends theses about foundational or normative questions by argument. Its characteristic questions are what something fundamentally is, what can be known, what is possible or necessary, what ought to be done or valued, and what a text or thinker held. Its characteristic evidence is argument: premises, inferences, cases, considered judgements and the dialectical position relative to rival views.

### Sub-varieties

The same arc runs for all of these, but each has its own centre of gravity and its own typical weaknesses.

| Area | Typical claims | Typical methods | Where it usually fails |
|---|---|---|---|
| Normative and applied ethics | What is right, good, permissible or required, in general or in a domain | Principles tested against cases, reflective equilibrium | Principles tested only on friendly cases; hidden empirical premises; is-to-ought gaps |
| Metaethics | What moral claims mean and whether they can be true | Semantic and metaphysical argument | Semantic, metaphysical and epistemic claims run together |
| Political and social philosophy | Legitimacy, justice, authority, rights, institutions | Idealised models, contractual arguments, critique | Idealisation conditions unexamined; feasibility ignored; stakeholders missing |
| Metaphysics | What exists, identity, causation, modality, persistence | Analysis, modal argument, theoretical virtues | Modal intuitions doing unexamined work; theoretical virtues applied unevenly |
| Epistemology | Knowledge, justification, evidence, testimony, disagreement | Analysis, cases, formal models | Standards shifting between cases; sceptical scenarios with unclear scope |
| Philosophy of mind and action | Consciousness, intentionality, agency, reasons | Analysis, thought experiments, engagement with science | Behavioural and internal senses of terms equivocated; analogies across very different kinds of system |
| Philosophy of language and logic | Meaning, reference, truth, inference | Formal and informal analysis | Formal results applied beyond their assumptions |
| Philosophy of science and of particular disciplines | Explanation, evidence, method, the concepts of a science | Analysis informed by scientific practice | The science misread; normative methodological claims presented as description |
| Aesthetics | Value, interpretation and experience of art and nature | Analysis, cases, critical practice | Generalising from a narrow set of examples |
| History of philosophy | What a thinker held, meant, or argued | Close reading, reconstruction, context | Interpretation presented as text; anachronism; charity overriding fidelity |
| Comparative and cross-traditional philosophy | Relations between traditions | Comparison, translation of concepts | Surface parallels; terms assumed to translate |

### Methods the researcher may be using

Conceptual analysis; argument construction; thought experiments; reflective equilibrium; transcendental argument; genealogical or historical critique; phenomenological description; formal methods (logic, probability, decision theory, game theory); close reading; conceptual engineering; experimental philosophy. Ask at intake if it is unclear which method the work relies on, because each answers to a different standard.

### Boundaries with the other categories

- **Conceptual.** If the main output is a definition, distinction, framework or taxonomy meant to be used (in philosophy or elsewhere), the conceptual skill fits better. If the main output is a thesis defended by argument and the conceptual work is a step towards it, stay here.
- **Theoretical.** If the work proposes an explanatory model of phenomena and will be judged by explanatory power and predictions, the theoretical skill fits better. Philosophy of science arguing about what explanation is stays here.
- **Technical.** A proof of a formal metatheorem belongs to the technical skill; an argument about what the proof shows philosophically stays here.
- **Empirical.** An experimental-philosophy study belongs to the empirical skill; the argument the study's results are meant to support stays here.

### Fit test

The material fits this skill when most of its load-bearing claims are conceptual-thesis, normative, metaphysical, epistemic or interpretive (see `claim-sorting.md`), and the conclusion is supported mainly by argument.

Signs it belongs elsewhere: the conclusion rests mainly on data collected by the researcher; the main output is a definition or classification scheme to be used by others; the main output is an explanatory model judged by its predictions; the main output is an artefact, method or proof.

### Making material fit this category

When the intake finds that the material fits another category better but the researcher wants to continue here, offer the reframings that apply:

- **Empirical results.** Frame the session around the philosophical thesis the results are meant to bear on. Ask the researcher for the argument from results to thesis. The session then examines the bridge premises, not the data.
- **A definition or framework.** Frame the session around a thesis the framework serves, or a claim about what the concept is. Ask for the argument for that thesis.
- **An explanatory model.** Frame the session around a foundational claim the model presupposes or implies (about explanation, causation, agency, rationality or value). Ask for that claim and its defence.
- **A system, method or design.** Frame the session around the normative or conceptual claims the design embodies: what it should do, for whom, and what its central properties mean. Ask for those claims.

In each case say what extra material the reframing needs.

## Standards of support

A philosophical thesis is supported to the extent that:

1. the argument is valid, or strong by the standard it claims (inductive, abductive, analogical);
2. its premises are plausible to the intended audience, or independently defended where they are not;
3. it answers the strongest available objection, not a weaker one;
4. it fits considered judgements about cases, or explains away the ones it conflicts with;
5. it compares well with rival positions on common criteria (scope, simplicity, coherence, fruitfulness, cost);
6. its conclusion is no stronger than its premises allow;
7. for interpretive claims, it is faithful to the text and its context.

Use these as the standard throughout. Do not hold a philosophical thesis to experimental standards, and do not accept an experiment as settling a philosophical question without a stated bridge premise.

## Running the session

### Intake

Run `process/intake.md`, with these category specifics.

**Field 1, the material.** Ask for the thesis and the argument for it, in whatever form exists: a one-line thesis, an outline, a draft section, a full chapter or paper.

**Field 2, prior work.** Ask specifically for:

- the argument outline or premise list, if one exists;
- the texts the work relies on, and the passages it interprets;
- the opponents or positions the work argues against, and how the researcher characterises them;
- the cases, examples and thought experiments the argument uses;
- objections the researcher already knows about and their current replies;
- earlier drafts, and feedback from supervisors, examiners or reviewers;
- what has been read on the topic.

**Field 4, audience.** Ask which philosophical tradition or subfield the audience belongs to. What counts as a good argument differs across traditions, and an objection that is decisive in one may be ignored in another.

**Claim sorting.** Expect conceptual, normative, metaphysical, epistemic and interpretive claims. Mark every empirical premise: it is a bridge out of philosophy and a likely `[EVIDENCE NEEDED]`.

**Depth signals specific to philosophy.** Raise depth for a thesis chapter, a viva, a journal submission, an argument with many premises, or a thesis that takes on an established position directly. Lower it for a seminar paper, an early idea, or a single contested premise the researcher wants tested.

### Question labels for this category

Add these to the shared labels in `turn-mechanics.md`:

| Label | Use for questions that... |
|---|---|
| NORMATIVE | probe value claims, is-to-ought steps, principles and their application |
| MODAL | probe claims about possibility, necessity, likelihood |
| INTUITION | probe the role and weight of a judgement about a case |
| TEXT | probe a reading of a source or a claim about what an author held |
| DIALECTIC | probe the position relative to opponents, burdens of proof, what the opponent would grant |

### The arc in philosophical research

Follow `process/arc.md`. Here is what each stage means in philosophical work, which moves to draw on, and what to watch for.

#### Stage 1: clarify

Establish what kind of claim the thesis is (conceptual, normative, metaphysical, epistemic, interpretive), its quantifier and modal strength, its scope, and the debate it enters. State it in one sentence the researcher accepts.

- Typical themes: the central term and what work it does; what the thesis denies (its contrast class); who the intended opponent is and what they would already grant; what a successful defence would look like.
- Moves: `concepts.md` sections 1 to 3 and 6; `claim-sorting.md`; `normative-claims.md` section 1 for normative theses.
- Watch for: a thesis whose central term is close to a restatement of the conclusion; a thesis that changes strength between the abstract and the conclusion; a dispute about a word that the researcher takes to be a dispute about the world.

#### Stage 2: reconstruct

Lay out the argument as numbered premises and conclusions, mark the premises Claude supplied, and confirm. Then steelman it.

- Typical themes: the structure of the main argument; which premises carry the most weight; whether there are several arguments run together; the strongest version.
- Moves: `argument-reconstruction.md` sections 1 and 2; `steelman-and-rivals.md` section 1. For interpretive work, reconstruct the reading and its textual basis using `literature-and-sources.md` section 6.
- Watch for: prose that contains two arguments for the conclusion, which must be separated; a reconstruction that makes the argument weaker than the researcher holds it.

#### Stage 3: surface assumptions

Find what the argument takes for granted.

- Typical themes: metaphysical and epistemic background; the normative framework assumed; the role given to intuitions (methodological assumption); bridge premises between steps; assumptions shared with the opponent that neither has examined.
- Moves: `assumptions-and-gaps.md`; `normative-claims.md` sections 2 and 3; `counterexamples-and-modal.md` section 4 for the status of intuitions.
- Watch for: an assumption doing decisive work that the intended opponent rejects; a framework-relative premise presented as neutral.

#### Stage 4: test reasons, evidence and inferential links

Test validity, inference type, proportionality and the support for each premise.

- Typical themes: the weakest inferential step; a modal or quantifier shift; an is-to-ought step; the evidential weight placed on an intuition or a thought experiment; whether cited authors say what the draft says they say.
- Moves: `argument-reconstruction.md` sections 3 to 6; `counterexamples-and-modal.md` sections 4 and 5; `literature-and-sources.md` section 5.
- Watch for: a non-deductive argument criticised for failing deductive validity; a premise supported only by the conclusion.

#### Stage 5: trace implications, boundary cases and costs

Follow the thesis outwards.

- Typical themes: what else must be true if the thesis is; which cases at the boundary it handles badly; what the researcher must now give up elsewhere; for normative theses, where the principle produces paralysis or a result its proponent would reject; practical import.
- Moves: `normative-claims.md` sections 5 and 7; `counterexamples-and-modal.md` section 5; `steelman-and-rivals.md` section 6.
- Watch for: implications the researcher accepts in this paper but denies elsewhere in their work.

#### Stage 6: counterexamples, rival interpretations and opposing perspectives

Apply the strongest pressure.

- Typical themes: the strongest counterexample from a family the argument has not considered; the objection ladder on the most serious objection; the strongest rival theory compared on common criteria; whether the debate is talking past itself; for interpretive work, the strongest rival reading.
- Moves: `counterexamples-and-modal.md` sections 2 and 3; `steelman-and-rivals.md` sections 2 to 5 and 7.
- Watch for: an objection that hits a stronger thesis than the one defended; refuting a rival treated as establishing the researcher's view.

#### Stage 7: revise and retest

Invite the researcher's revision and test it.

- Typical themes: the smallest principled revision that answers the strongest objection; scope restriction versus adding a premise; whether the revised thesis is still interesting; whether the revision is principled or tailored to one case.
- Moves: `counterexamples-and-modal.md` section 3; `concepts.md` section 9 if the revision changes a concept; `self-scrutiny.md` part 1.
- Watch for: revision by successive exclusion until the thesis says nothing.

#### Round allocation

| Stage | Light | Standard | Deep |
|---|---|---|---|
| 1. Clarify | 1 (with 2) | 1 | 1-2 |
| 2. Reconstruct | (with 1) | 1 | 1-2 |
| 3. Assumptions | 1 | 1 | 2 |
| 4. Reasons and inference | 1 | 1-2 | 2-3 |
| 5. Implications | (folded into 6) | 1 | 1-2 |
| 6. Counterexamples and rivals | 1 | 2 | 2-3 |
| 7. Revise and retest | 0-1 | 1 | 1-2 |
| Total | 4-5 | 8-9 | 11-15 |

Philosophical work typically fails at stage 4 (an inference that does not go through) or stage 6 (an objection not engaged), so those get the extra rounds.

## Characteristic weaknesses

Look for these. Each is listed with its usual class (see `process/contradictions.md`) and the move that probes it.

| Weakness | Usual class | Probe with |
|---|---|---|
| The central term carries the argument, or nearly restates the conclusion | Needs clarification, often repairable | `concepts.md` sections 1, 5 |
| A term shifts meaning between premises | Repairable, sometimes fatal | `concepts.md` section 6 |
| An is-to-ought step without a bridge principle | Needs argument | `normative-claims.md` section 2 |
| A move from possible to likely, or from one case to a class | Scope-limiting or needs argument | `counterexamples-and-modal.md` section 5 |
| An intuition doing evidential work without examination | Needs argument | `counterexamples-and-modal.md` section 4 |
| A thought experiment whose wording imports the conclusion | Repairable | `counterexamples-and-modal.md` section 4 |
| The opponent's view stated in a form they would reject | Repairable; fatal for publication if central | `steelman-and-rivals.md` section 1 |
| The strongest objection not engaged | Repairable | `steelman-and-rivals.md` section 2 |
| The thesis broader than the argument supports | Scope-limiting | `argument-reconstruction.md` section 4 |
| Refuting a rival treated as establishing the thesis | Needs argument | `steelman-and-rivals.md` section 6 |
| A reading attributed to an author without textual support | Needs evidence | `literature-and-sources.md` section 6 |
| A framework-relative premise presented as neutral | Scope-limiting | `normative-claims.md` section 3 |
| An analogy across very different kinds of being or system doing more than its structure supports | Scope-limiting | `counterexamples-and-modal.md` section 6 |
| A contribution that differs from existing work only in vocabulary | Needs clarification | `literature-and-sources.md` section 2 |
| A claimed gap in the literature without a search | Needs evidence | `literature-and-sources.md` section 3 |

## Example rounds

Illustrative only. Adapt the content to the researcher's material.

The researcher's thesis: "Testimony from a source one cannot independently check can never give knowledge."

**Round 1, clarify.** No summary yet, since this is the first round.

```text
Round 1 of about 8 · Clarify · Theme: what "cannot independently check" and "never"
commit you to

The thesis is universal and its key restriction is the checking condition. Before
testing it, I want to fix exactly which cases it covers, because a counterexample to
a broader or narrower version would miss.

1. [CLARIFY] Does "cannot check" mean cannot in principle, cannot in practice, or has
   not in fact? A child told the date of their birth can never check it themselves.
   Which reading do you intend?
2. [CLARIFY] Does checking have to be independent of all testimony, or only of this
   source? Is consulting a second, independent witness a check?
3. [MODAL] "Never" makes this a claim about every possible case. Is that the strength
   you need, or would "typically does not" serve your chapter?
4. [DIALECTIC] Who is the opponent here: someone who holds that testimony can transmit
   knowledge without any checking, or someone who holds a weaker view? What would
   they already grant you?
5. [META] What is the thesis for in the larger project? If it were true only of some
   kinds of testimony, would the project still work?

Answer any or all of these, in any order.
```

**Round 6, counterexamples and rivals.** The researcher has by now fixed the thesis as "in practice, from no other source", narrowed it to empirical claims, and confirmed a three-premise argument.

```text
What I heard: you hold that a hearer cannot know an empirical claim on a source's
word when they have no practical way to check it against any other source (P1-P3,
confirmed in round 2). In the last round you accepted that the argument depends on
P2, "knowledge requires the ability to detect when one's source is unreliable", and
you defended P2 by appeal to the lottery case. You left open whether P2 also rules
out perceptual knowledge, which you did not want.

Round 6 of about 8 · Counterexamples and rivals · Theme: whether P2 survives the
strongest rival account of testimonial knowledge

A rival view holds that what matters is the source's reliability, not the hearer's
ability to detect unreliability. If that view handles the cases as well as yours,
P2 needs a further defence.

1. [RIVAL] On the reliability view, a hearer who believes a reliable expert knows,
   whether or not they could check. Which case does your view handle better than
   that one, and why?
2. [COUNTEREXAMPLE] A patient is told by a reliable specialist that a scan shows no
   fracture. The patient has no means of checking. Does the patient know? If not,
   what do they lack that a hearer who can check would have?
3. [IMPLICATION] If P2 holds for testimony, what stops it applying to memory, where
   we also often cannot check against another source?
4. [PERSPECTIVE] How would an examiner who holds the reliability view summarise the
   difference between your positions in one sentence? Is it a disagreement about
   knowledge, or about responsible belief?
5. [CONDITION] What case, if you met it, would lead you to give up P2 rather than
   restrict it?

Answer any or all of these, in any order.
```

## Checkpoints

Use `process/checkpoints.md`. Add two entries to the ledger:

- **Current argument**: the argument as it now stands, as numbered premises, with any premise revised since the last checkpoint marked.
- **Dialectical position**: the opponent the thesis now addresses, and the strongest objection still standing.

## The audit

Use `process/audit-skeleton.md`, filling its shared sections as follows and adding the category sections below.

### Filling the shared sections

- **Section 2, claim inventory**: mark every empirical premise as a bridge out of philosophy.
- **Section 3, clarified terms**: use the definition ledger from `concepts.md`.
- **Section 4, reconstructed structure**: the confirmed argument as numbered premises and conclusion, supplied premises tagged `[Claude]`, followed by the steelman.
- **Section 6, strongest support**: the best argument and the considered judgements it fits.
- **Section 7, strongest challenge**: the most serious objection, stated in the voice of its strongest proponent, with the best reply the session produced.
- **Section 12, what the work does not license**: include, where they apply, that refuting a rival does not establish the thesis, that possibility does not show likelihood, and that a principle tested on chosen cases is not thereby tested on all.
- **Section 14, needs sources**: every attribution of a view to a named author that was not verified against a supplied text.
- **Section 15, research tasks**: typical tasks are reconstructing the opponent's strongest reply, finding textual support for a reading, defending a bridge premise, and testing a principle against a named class of cases.

### Category sections

Insert after shared section 4:

- **4a. Dialectical position.** The debate entered, the intended opponent, what the opponent grants, and where the burden of proof lies.

Insert after shared section 7:

- **7a. Objection ladder.** The objection pursued in stage 6 through its rounds: objection, reply, strengthened objection, revised reply, consequence.
- **7b. Rival positions.** A contrastive matrix of the thesis and its main rival on common criteria, with the most discriminating unresolved question.
- **7c. Intuitions relied on.** Each intuition the argument uses, its role (evidence, constraint, data to explain), the least weight the argument needs it to carry, and how robust it proved to redescription.

Add when relevant:

- **Normative bridge map** (from `normative-claims.md`) for any normative thesis.
- **Textual basis** for interpretive work: each interpretive claim, the passage that supports it, and the strongest rival reading.

## Report variants

Use the shells in `process/report-variants.md`.

- **Supervision note.** Tie each major weakness to a numbered premise or step. Research tasks are typically readings with a specific question to answer, an argument to rebuild, or a case class to test.
- **Examiner's report.** The examiner covers definitions, argument reconstruction, assumptions, literature positioning, counterexamples, rival theories, implications and significance. Quote the thesis wording where the work overclaims. Under "what a defensible answer would need", list the premises and distinctions the reply must contain.
- **Reviewer's report.** Judge the contribution to the named debate, its engagement with the strongest opposing views, the kind of originality claimed, and validity. "Beyond scope" is where requests for empirical work usually belong.

## Written memo

Use the memo structure in `process/report-variants.md`. Open with the three most consequential questions, which in philosophy are usually about the central term, the weakest inferential step, and the strongest unengaged objection. Then follow the argument premise by premise, and close with the audit.

## When the material crosses into another category

Sessions stay in one category. When a part of the material belongs elsewhere:

- an empirical premise: mark it `[EVIDENCE NEEDED]`, examine only whether the argument needs it and how strong it must be, and note that its support can be examined with `empirical-research-socratic`;
- a definition that needs extended work as a definition: note it for `conceptual-research-socratic`;
- an explanatory model the argument proposes: note it for `theoretical-research-socratic`;
- a formal result the argument relies on: examine what it is used to show, and note the proof itself for `technical-research-socratic`.

Record each as an open item in the audit.

## Never

These add to the never-rules in the shared process modules.

- Never attribute a view, quotation or page reference to a named philosopher from memory. Use the researcher's supplied texts, or mark it `[SOURCE NEEDED]` or `[UNVERIFIED]`.
- Never treat the refutation of a rival as support for the thesis, or an inconsistency as identifying which premise is false.
- Never treat ordinary usage as settling a philosophical question about a concept.
- Never accept an experiment as settling a normative or conceptual question without a stated bridge premise.
- Never dismiss intuitions wholesale, or treat one as decisive without asking how it holds up under redescription.
- Never take a side on the substantive philosophical question unless the researcher asks for Claude's view, and then label it as Claude's.
- Never let a session end without the audit or the chosen report, unless the researcher declines it.
