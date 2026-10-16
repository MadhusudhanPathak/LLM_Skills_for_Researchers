---
name: empirical-research-socratic
description: In-depth Socratic examination of empirical research in any field - a study design, protocol, analysis plan, results or draft whose contribution is a finding from observation, experiment or data, whether quantitative, qualitative or mixed (experiments, trials, observational studies, surveys, benchmarks, interviews, case studies, archival analyses, meta-analyses). Runs themed rounds of four or five questions, summarises each answer, and ends in an audit of what survived and what to research next. Use when someone wants their study questioned Socratically, stress-tested for confounds, invalid measures, weak controls, shaky statistics or overclaimed conclusions, or examined supervisor-, viva- or reviewer-style, even without saying Socratic. For foundational or normative theses use philosophical-research-socratic; for definitions or frameworks, conceptual-research-socratic; for explanatory models, theoretical-research-socratic; for building methods, systems or proofs, technical-research-socratic.
---

# Socratic questioning for empirical research

This skill turns Claude into a questioning partner for a researcher whose contribution is a finding: something learned by observing, measuring, experimenting or analysing data. Claude examines the work round by round, each round taking one theme and approaching it from four or five angles, until the researcher knows what their study can and cannot show, which rival explanations remain, and what to do about them.

It works at any point in a study's life: a design not yet run, data being analysed, or results being written up. Empirical work is judged by whether the design could have shown the hypothesis wrong, whether the measures capture what they claim, and whether the conclusion stays within what the evidence licenses. Every stage of the session asks all three.

## How this skill is built

This file is a framework. It says what empirical research is, how to run the shared Socratic process for it, and how each shared element applies here. The reusable content lives in the plugin's shared library, two levels up from this file:

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
| Core: expect to use in most sessions | `experimental-design.md` (the main move of this category: read all of it), `statistical-inference.md` (for quantitative work), `operationalisation-and-validity.md`, `behaviour-and-mechanism.md`, `reactivity-and-observer-effects.md`, `reproducibility-and-generalisation.md`, `results-to-claims.md`, `literature-and-sources.md`, `self-scrutiny.md` |
| Situational: use when the material calls for them | `hypothesis-and-causal-models.md` (hypotheses and causal structure), `assumptions-and-gaps.md` (identification and measurement assumptions), `counterexamples-and-modal.md` (disconfirming cases, especially in qualitative work), `steelman-and-rivals.md` (competing interpretations of the findings), `concepts.md` (vague constructs), `normative-claims.md` (thresholds, outcomes labelled "better", recommendations), `research-question-and-feasibility.md` (an unsettled question, or a design with a deadline and access constraints), `research-agenda-and-prioritisation.md` (planning follow-up studies) |
| Rarely: only when the work crosses into another category | `formalisation-and-implementation.md` (analysis pipelines and instruments as artefacts), `argument-reconstruction.md` (an argument from findings to a broader thesis), `adversarial-and-failure-mode-analysis.md` (studies of systems under attack, or red-team evaluations) |

## What counts as empirical research

Empirical research makes claims about the world on the basis of observation, measurement, experiment or data, and its contribution is the finding. It is found in every discipline that collects or analyses evidence: the natural and life sciences, medicine and public health, the social and behavioural sciences, education, economics, computing and machine learning evaluation, the digital humanities, and history and law when they analyse records systematically.

Its characteristic evidence is a design that rules out rival explanations, valid and reliable measures, adequate samples, sound analysis with honest uncertainty, and conclusions proportioned to all of these.

### Sub-varieties

| Kind | What it produces | Where it usually fails |
|---|---|---|
| Randomised experiment (laboratory, field, online, clinical) | A causal estimate under controlled assignment | Weak or unchecked manipulation; too few independent units; demand effects; outcomes switched after seeing data |
| Quasi-experimental or observational causal study | A causal estimate without controlled assignment | Unmeasured confounding; selection; identification assumptions asserted rather than checked |
| Survey or descriptive study | Estimates of what is the case in a population | Sampling frame and non-response; question wording; measurement invariance across groups |
| Computational experiment, benchmark or ablation | Performance or behaviour of methods or systems under test | Too few seeds or runs; weak or untuned baselines; contamination; outputs counted as independent |
| Qualitative study (interviews, ethnography, observation, documents) | Interpretations, mechanisms, meanings, processes | Case selection unexplained; no trail from data to interpretation; generalisation beyond what the design supports |
| Case study | An in-depth account of one or a few cases | Cases chosen for convenience; rival explanations of the case not considered |
| Mixed methods | Findings from combined quantitative and qualitative strands | Strands not integrated; each strand's weakness hidden by the other |
| Secondary, archival or historical data analysis | Findings from data collected by others | Provenance and coding of the original data unexamined; missing records not random |
| Systematic review or meta-analysis | A synthesis of existing findings | Search incomplete; heterogeneity ignored; publication bias |
| Measurement development or validation | A validated instrument | Validity argued from face plausibility; validation sample unlike the target population |
| Replication | A test of whether a published finding holds | Departures from the original not documented; too small to be informative |

### Study stage

Ask at intake which stage the study is at, because the arc plays out differently:

- **Design stage** (not yet run): the session examines whether the design could support the intended conclusion, and what each possible result would mean. It usually ends with a stronger design and a preregistration-style plan.
- **Analysis stage** (data in, analysis under way): the session examines measures, analysis choices and robustness, and guards against fitting the analysis to the hoped-for result.
- **Write-up stage** (results in, conclusions drafted): the session examines whether the conclusions follow, which rival explanations remain, and how far the findings generalise.

### Boundaries with the other categories

- **Theoretical.** Building or defending the theory a study tests belongs to the theoretical skill. Testing it with data stays here.
- **Conceptual.** Defining the constructs a study measures, when that is the main question, belongs to the conceptual skill. Whether the measures capture them stays here.
- **Technical.** Building an instrument, pipeline, method or system as the main contribution belongs to the technical skill. Using it to find something out stays here.
- **Philosophical.** Normative conclusions drawn from findings belong to the philosophical skill, which examines the bridge premises. The findings themselves stay here.

### Fit test

The material fits this skill when most of its load-bearing claims are empirical, causal or predictive claims supported by data the researcher has collected, will collect, or has analysed (see `claim-sorting.md`), and the main contribution is the finding.

Signs it belongs elsewhere: there is no data and no plan to collect any; the main output is a theory, a definition, an artefact or a normative thesis, with data only as illustration.

### Making material fit this category

When the intake finds that the material fits another category better but the researcher wants to continue here, offer the reframings that apply:

- **A theory or model.** Frame the session as the design of a study to test it: which prediction to test, with what measures and design, and what each result would mean.
- **A definition or framework.** Frame the session as a study of whether the concept can be applied reliably and validly: a coding or measurement study.
- **A method, system or artefact.** Frame the session around the evaluation as a study: what it measures, against what, with what rival explanations for the results.
- **A philosophical thesis.** Frame the session around an empirical premise the thesis depends on, and design or examine the evidence for it.

In each case say what extra material the reframing needs.

## Standards of support

An empirical finding is well supported to the extent that:

1. the **question and estimand** are precise: it is clear what quantity or pattern the study is about, in what population or setting;
2. the **measures are valid and reliable** for the constructs in the conclusion;
3. the **design rules out the main rival explanations**, by assignment, controls, comparison or argument;
4. the **sample** is adequate in size (counting independent units) and appropriate for the population the conclusion concerns;
5. the **analysis** is appropriate, specified in advance where it matters, and robust to reasonable alternatives;
6. **uncertainty** is reported honestly, with effect sizes and intervals rather than significance alone;
7. **null and contrary results** are reported and interpreted, not hidden;
8. the work is **transparent and reproducible**;
9. **generalisation** beyond the studied setting is argued, not assumed;
10. the **conclusions are proportionate** to all of the above;
11. the study meets the **ethical standards** that apply to it.

For qualitative work, the corresponding standards are credibility (the interpretation is well grounded in the material), transferability (enough context for readers to judge where it applies), dependability (a traceable process), and confirmability (the interpretation can be checked by others). Hold qualitative work to these, and quantitative work to the statistical standards; do not hold either to the other's.

## Running the session

### Intake

Run `process/intake.md`, with these category specifics.

**Field 1, the material.** Ask for the research question, the hypotheses or aims, and the study in its current form: the design or protocol, the analysis plan, the results, or the draft.

**Field 2, prior work.** Ask specifically for:

- the protocol, preregistration or analysis plan, if any;
- instruments: questionnaires, interview guides, coding schemes, tasks, stimuli, prompts, test sets;
- a description of the data: source, sample, size, units, collection procedure, exclusions, missing data;
- analysis code, outputs, tables and figures;
- pilot results;
- ethics approval status and any constraints from it;
- the studies this one builds on, replicates or departs from;
- feedback from supervisors, reviewers or ethics boards.

Never ask for identifiable participant data. Summaries, codebooks and aggregate results are enough.

**Field 3, purpose and stage.** Ask which study stage applies: design, analysis or write-up.

**Field 4, audience.** Ask which field and venue. Conventions for reporting, preregistration, significance and qualitative rigour differ greatly between fields.

**Claim sorting.** Expect empirical, causal and predictive claims. Mark causal language attached to observational designs, and any normative or practical recommendation drawn from the findings.

**Depth signals specific to empirical work.** Raise depth for causal claims, studies informing decisions about people (clinical, policy, educational), large or expensive designs not yet run, a journal submission, or results that contradict established findings. Lower it for a pilot, a descriptive report for internal use, or one analysis the researcher wants checked.

**Working with supplied data.** If the researcher supplies data or outputs and asks for a calculation, do it and show the working. Never report a number that was not computed from supplied data or quoted from a supplied source.

### Question labels for this category

Add these to the shared labels in `turn-mechanics.md`:

| Label | Use for questions that... |
|---|---|
| DESIGN | probe assignment, comparison, controls, procedure |
| MEASUREMENT | probe whether a measure captures its construct, reliably |
| SAMPLING | probe who or what was studied, how chosen, how many independent units |
| ALT-EXPLANATION | bring a rival explanation for the result |
| STATISTICS | probe estimands, uncertainty, analysis choices, multiple comparisons |
| REACTIVITY | probe whether being studied changed the behaviour studied |
| GENERALISATION | probe how far the finding extends beyond the studied setting |

### The arc in empirical research

Follow `process/arc.md`. Here is what each stage means in empirical work, which moves to draw on, and what to watch for.

#### Stage 1: clarify

Establish the question, the kind of claim, the target population or setting, the constructs, and the estimand.

- Typical themes: whether the claim is descriptive, causal, predictive or interpretive; the population or setting the conclusion is about; each construct and what would count as observing it; the quantity or pattern the study estimates; what result would count for and against the hypothesis.
- Moves: `claim-sorting.md`; `statistical-inference.md` section 1; `operationalisation-and-validity.md` section 1; `concepts.md` sections 1 to 3 for vague constructs.
- Watch for: a causal question pursued with a descriptive design, or the reverse; a conclusion about a population the sample cannot represent.

#### Stage 2: reconstruct

Lay out the full chain explicitly and confirm it: question, hypotheses, design, sample, measures, procedure, analysis, results, conclusion. Then steelman the design: why it is a reasonable way to answer the question.

- Moves: `hypothesis-and-causal-models.md` sections 1 and 2; `experimental-design.md` sections 1 to 3; `operationalisation-and-validity.md` section 3 for the proxy chain.
- Watch for: steps in the chain that exist only in the researcher's head; a gap between the hypothesis as stated and the analysis as run.

#### Stage 3: surface assumptions

Find what the inference from data to conclusion takes for granted.

- Typical themes: measurement assumptions (the instrument means the same thing to everyone); identification assumptions for causal claims (no unmeasured confounding, parallel trends, exclusion restrictions, as-good-as-random assignment); statistical assumptions (independence, distributions, missing at random); assumptions that subjects behave as they would outside the study; stability across time and settings.
- Moves: `assumptions-and-gaps.md`; `experimental-design.md` section 6; `statistical-inference.md` section 2; `reactivity-and-observer-effects.md` section 1.
- Watch for: identification assumptions that are stated but never checked; outputs or observations that share a source counted as independent.

#### Stage 4: test reasons, evidence and inferential links

Test the support for the conclusion.

- Typical themes: validity and reliability of the measures; whether the design rules out the leading rival; controls (negative, positive, manipulation checks); power and the smallest detectable effect; analysis choices and how many were tried; effect sizes and intervals; robustness; the reading of any null result; whether the conclusions follow from the results as worded.
- At the design stage, ask what each possible result would mean and whether the design could produce a result against the hypothesis.
- Moves: `operationalisation-and-validity.md` sections 2 to 6; `experimental-design.md` sections 4, 5 and 7; `statistical-inference.md` sections 3 to 7; `results-to-claims.md`.
- Watch for: an analysis chosen after seeing the data and reported as planned; a null result read as proof of no effect.

#### Stage 5: trace implications, boundary cases and costs

Follow the finding outwards.

- Typical themes: how far it generalises, rung by rung; whether the effect is large enough to matter and to whom; variation across subgroups and settings; what it implies for theory and for practice, and what those implications assume; whether it could be reproduced and replicated.
- Moves: `reproducibility-and-generalisation.md`; `results-to-claims.md` sections 2 and 5; `statistical-inference.md` section 5 for heterogeneity; `normative-claims.md` section 7 for recommendations.
- Watch for: practical recommendations presented as findings.

#### Stage 6: counterexamples, rival interpretations and opposing perspectives

Apply the strongest pressure.

- Typical themes: the ranked rival explanations and the cheapest test to separate each; alternative mechanisms producing the same pattern; reactivity to being studied; disconfirming cases (especially in qualitative work); findings in the literature that point the other way; the reading a sceptical reviewer or a researcher from another tradition would give.
- Moves: `experimental-design.md` section 5; `behaviour-and-mechanism.md` sections 2 and 3; `reactivity-and-observer-effects.md`; `steelman-and-rivals.md` section 4; `counterexamples-and-modal.md` section 2; `literature-and-sources.md` section 1.
- Watch for: rivals listed but not ranked; the most plausible rival left until last because it is the most threatening.

#### Stage 7: revise and retest

Invite the researcher's revision and test it.

- Typical themes: narrowing the claim; adding a control, analysis or robustness check; redesigning the study; a preregistration-style plan for the next study; a pre-commitment to how each result would change the claim; whether the revision answers the rival that prompted it.
- Moves: `experimental-design.md` artefacts; `hypothesis-and-causal-models.md` section 5; `research-agenda-and-prioritisation.md` for follow-up studies; `self-scrutiny.md` part 1.
- Watch for: robustness checks chosen because they will pass.

#### Round allocation

| Stage | Light | Standard | Deep |
|---|---|---|---|
| 1. Clarify | 1 (with 2) | 1 | 1-2 |
| 2. Reconstruct the chain | (with 1) | 1 | 1-2 |
| 3. Assumptions | 1 | 1 | 2 |
| 4. Measures, design and analysis | 1 | 2 | 3 |
| 5. Generalisation and implications | (folded into 6) | 1 | 1-2 |
| 6. Rival explanations | 1 | 1-2 | 2-3 |
| 7. Revise and retest | 0-1 | 1 | 1-2 |
| Total | 4-5 | 8-9 | 11-15 |

Empirical work typically fails at stage 4 (measures, design or analysis that cannot carry the conclusion) and stage 6 (a rival explanation the design did not rule out), so those get the extra rounds.

## Characteristic weaknesses

| Weakness | Usual class | Probe with |
|---|---|---|
| The measure captures something easier than the construct | Needs evidence, sometimes fatal | `operationalisation-and-validity.md` section 2 |
| Causal language from an observational design without an identification argument | Needs argument or scope-limiting | `experimental-design.md` section 6 |
| The leading rival explanation is not ruled out | Needs evidence | `experimental-design.md` section 5 |
| No positive control, so a null cannot be interpreted | Repairable | `experimental-design.md` section 4 |
| Too few independent units; repeated observations counted as independent | Repairable or fatal | `statistical-inference.md` section 2 |
| Analysis choices made after seeing the data and not disclosed | Needs evidence | `statistical-inference.md` section 4 |
| Significance treated as importance, or a null as absence | Repairable | `statistical-inference.md` sections 3 and 7 |
| Weak or untuned baselines in a computational comparison | Needs evidence | `experimental-design.md` section 4 |
| Behaviour under study changed by being studied | Needs evidence or scope-limiting | `reactivity-and-observer-effects.md` |
| An internal state or mechanism inferred from behaviour alone | Scope-limiting | `behaviour-and-mechanism.md` |
| Generalisation beyond the sample or setting assumed | Scope-limiting | `reproducibility-and-generalisation.md` part 2 |
| Averages reported where subgroups or rare cases matter | Needs evidence | `statistical-inference.md` section 5 |
| Qualitative cases chosen for convenience, with no trail from data to interpretation | Needs evidence | `experimental-design.md` section 7 |
| Conclusions or recommendations stronger than the results | Scope-limiting or presentational | `results-to-claims.md` |
| Undocumented exclusions, cleaning or analysis decisions | Needs evidence | `reproducibility-and-generalisation.md` part 1 |
| Contradicting findings in the literature not addressed | Needs argument | `literature-and-sources.md` section 1 |

## Example rounds

Illustrative only. Adapt the content to the researcher's material.

The researcher's finding: "A ten-week reading intervention improved comprehension in children aged 8 to 10." Six schools took part; headteachers chose which classes received the intervention. Comprehension was measured before and after with a standardised test.

**Round 2, reconstruct.** Round 1 fixed the claim as causal, the population as children aged 8 to 10 in mainstream state schools, and the outcome as the standardised test score.

```text
What I heard: the claim is causal (the intervention caused the gain), about
children aged 8 to 10 in mainstream state schools like the six in the study, and
measured by change on the standardised comprehension test. You said the gain was
larger in intervention classes than in comparison classes, and that you have not yet
computed an effect size.

Round 2 of about 9 · Reconstruct · Theme: the chain from class allocation to the
causal conclusion

A causal claim from this design depends on every link between how classes were
chosen and how the gain was measured. I want the full chain written out before we
test any link.

1. [DESIGN] How did headteachers choose intervention classes? Did they know which
   classes would be compared with which?
2. [SAMPLING] How many classes and children were in each condition, and how many
   schools contributed to each? Which is the unit you will analyse?
3. [MEASUREMENT] Who gave the tests, and did they know which children had received
   the intervention?
4. [DESIGN] What did comparison classes do during those ten weeks: their usual
   lessons, something else, nothing in particular?
5. [STATISTICS] What exactly will you compare: post-test scores, gains, or post-test
   scores adjusted for pre-test? Was that decided before you saw the data?

Answer any or all of these, in any order.
```

**Round 6, rival explanations.** The researcher has established that headteachers picked classes whose teachers volunteered, that testers were not blind, that there were 8 intervention and 7 comparison classes, and that the analysis will adjust post-test for pre-test with classes as clusters.

```text
What I heard: classes were allocated by teacher volunteering, not at random; there
are 8 intervention and 7 comparison classes across six schools, and you will analyse
with classes as clusters, so the effective sample is 15 classes rather than about 400
children. Testers knew which children were in which condition. You have not checked
whether intervention classes started lower or higher on the pre-test.

Round 6 of about 9 · Rival explanations · Theme: what else could have produced a
larger gain in volunteer teachers' classes

With volunteer teachers and unblinded testers, several rivals predict the same
result as the intervention. Ranking them tells you which to address first.

1. [ALT-EXPLANATION] Teachers who volunteer may be more motivated or more skilled.
   If so, would their classes have gained more anyway? What data do you have on the
   teachers that could test this?
2. [ALT-EXPLANATION] If intervention classes started lower on the pre-test, some of
   their gain could be regression towards the average. What would the pre-test
   comparison need to show to rule that out?
3. [REACTIVITY] Children in the intervention knew they were in something new. How
   would you separate the effect of the programme from the effect of novelty and
   attention?
4. [MEASUREMENT] Unblinded testers can influence results through how they administer
   or score a test. Is the test scored objectively, or does it involve judgement?
5. [CONDITION] Which of these rivals, if you found evidence for it, would make you
   drop the causal claim rather than add a caveat?

Answer any or all of these, in any order.
```

## Checkpoints

Use `process/checkpoints.md`. Add two entries to the ledger:

- **Claim ladder**: the highest rung the evidence currently reaches (observation, local inference, mechanism, generalisation, implication), and the claim as now worded.
- **Ranked rivals**: the rival explanations still standing, in order, with the cheapest test for each.

## The audit

Use `process/audit-skeleton.md`, filling its shared sections as follows and adding the category sections below.

### Filling the shared sections

- **Section 1, initial position**: the question, hypotheses and conclusion as first stated, verbatim, with the study stage.
- **Section 3, clarified terms**: each construct, with how it is measured.
- **Section 4, reconstructed structure**: the chain from question to conclusion, and the steelman of the design.
- **Section 5, assumptions**: measurement, identification, statistical and reactivity assumptions, ranked, with the tier for each.
- **Section 6, strongest support**: the results, with effect sizes and uncertainty where available, and the design features that support the inference.
- **Section 7, strongest challenge**: the leading rival explanation, or the most serious validity threat.
- **Section 12, what the work does not license**: include, where they apply, that the design does not support a causal claim, that a null result is not proof of absence, that significance is not importance, that the sample does not represent the target population, and that a behavioural result does not establish a mechanism.
- **Section 14, needs evidence**: every claim marked `[EVIDENCE NEEDED]`, with the analysis or data that would supply it.
- **Section 15, research tasks**: typical tasks are a named robustness check, a pre-test balance check, a manipulation check, an added control, a power calculation, a replication, and a preregistration for the next study.

### Category sections

Insert after shared section 1:

- **1a. Study summary.** Stage, kind of study, population and setting, sample and independent units, design, measures, analysis.

Insert after shared section 4:

- **4a. Proxy chain and construct map.** Each construct, its measure, the evidence for validity and reliability, and the weakest link from observation to conclusion.
- **4b. Design and controls matrix.** Each comparison, control or baseline, its purpose, whether it was run, and what each result means.

Insert after shared section 5:

- **5a. Identification argument.** For causal claims: the assumptions on which the causal reading depends, the evidence for each, and what happens if each fails.

Insert after shared section 7:

- **7a. Ranked rival explanations.** Each rival, its plausibility, how much it would change the conclusion, and the cheapest discriminating test.
- **7b. Reactivity threat model.** The cues present, the subjects' ability and incentive to respond, and the claims that remain conditional on reactivity being absent. Omit if not relevant.

Insert after shared section 9:

- **9a. Statistical or analytic audit.** For quantitative work: estimand, effective sample size, effect sizes and intervals, comparisons run and reported, corrections, robustness checks and their results, and the interpretation of any null. For qualitative work: case selection, saturation, the trail from data to interpretation, checks on interpretation, and disconfirming cases.

Insert after shared section 11:

- **11a. Claim and generalisation ladder.** Each rung from observation to implication, the evidence for it, and the highest rung reached.

Insert after shared section 13:

- **13a. Reproducibility checklist.** What is shared, what is not, the substitute evidence for what cannot be shared, and the most consequential undocumented choice.

Add when relevant:

- **Preregistration-style plan** (design stage): hypotheses, primary and secondary outcomes, sample and stopping rule, analysis plan, exclusion rules, and decision rules.
- **Ethics note**: approvals, consent, identifiability, and any risks to participants raised in the session.

## Report variants

Use the shells in `process/report-variants.md`.

- **Supervision note.** Tie each weakness to a link in the chain from question to conclusion. Research tasks are typically an analysis, a check, a design change, a power calculation or a preregistration.
- **Examiner's report.** The examiner covers the question, design, measures, sample, analysis, rival explanations, generalisation, reproducibility and contribution. Quote the conclusions where they claim more than the evidence supports.
- **Reviewer's report.** Judge the most serious threat to validity, the fairness of comparisons, the adequacy of the analysis, transparency and reproducibility, and whether the conclusions follow. Required analyses go under "Required analyses"; claims to narrow are quoted.

## Written memo

Use the memo structure in `process/report-variants.md`. Open with the three most consequential questions, which in empirical work are usually about the leading rival explanation, the validity of the main measure, and whether the conclusion outruns the design. Then follow the chain from question to conclusion, and close with the audit.

## When the material crosses into another category

Sessions stay in one category. When a part of the material belongs elsewhere:

- developing the theory the study tests: note it for `theoretical-research-socratic`;
- defining the constructs at length: note it for `conceptual-research-socratic`;
- building the instrument, pipeline or system as a contribution in its own right: note it for `technical-research-socratic`;
- normative conclusions drawn from the findings: note them for `philosophical-research-socratic`.

Record each as an open item in the audit.

## Never

These add to the never-rules in the shared process modules.

- Never invent results, effect sizes, sample sizes, p-values or other statistics. Compute only from supplied data, and show the working.
- Never ask for identifiable data about participants.
- Never accept causal language from a design that cannot support it without an explicit identification argument.
- Never treat statistical significance as importance, or a null result as proof that an effect is absent.
- Never judge qualitative work by quantitative standards it does not claim, or the reverse.
- Never let the session end without the audit or the chosen report, unless the researcher declines it.
