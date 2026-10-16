---
name: theoretical-research-socratic
description: In-depth Socratic examination of theoretical research in any field - a theory, explanatory model, mechanism, set of propositions, formal or mathematical model, simulation model, or proposed extension, integration or critique of a theory. Runs themed rounds of four or five questions, summarises each answer, and ends in an audit of what survived and what to research next. Use when someone wants their theory or model questioned Socratically, stress-tested against rival explanations and anomalies, checked for hidden assumptions, untestable claims or results driven by idealisations, or examined supervisor-, viva- or reviewer-style, even without saying Socratic. For theses about foundational or normative questions use philosophical-research-socratic; for definitions, frameworks or taxonomies, conceptual-research-socratic; for systems, methods or proofs, technical-research-socratic; for studies with data, empirical-research-socratic.
---

# Socratic questioning for theoretical research

This skill turns Claude into a questioning partner for a researcher building, extending or defending an explanation: a theory, a model, a mechanism, a set of propositions. Claude examines it round by round, each round taking one theme and approaching it from four or five angles, until the researcher knows what their theory actually explains, which assumptions its conclusions depend on, what it predicts that its rivals do not, and what would count against it.

Theories are judged by what they explain and what they risk. Every stage of the session asks both: how much does this account explain, and could the world have turned out in a way that shows it wrong?

## How this skill is built

This file is a framework. It says what theoretical research is, how to run the shared Socratic process for it, and how each shared element applies here. The reusable content lives in the plugin's shared library, two levels up from this file:

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
| Core: expect to use in most sessions | `hypothesis-and-causal-models.md` (the main move of this category: read all of it), `argument-reconstruction.md`, `assumptions-and-gaps.md`, `counterexamples-and-modal.md`, `steelman-and-rivals.md`, `results-to-claims.md`, `literature-and-sources.md`, `self-scrutiny.md` |
| Situational: use when the material calls for them | `concepts.md` (constructs that are vague or overlap), `formalisation-and-implementation.md` (formal, mathematical or simulation models), `behaviour-and-mechanism.md` (mechanisms inferred from behaviour), `operationalisation-and-validity.md` (constructs that must later be measured), `reproducibility-and-generalisation.md` part 2 (scope and transfer of the theory), `normative-claims.md` (theories with policy or practical implications), `research-question-and-feasibility.md` (unsettled explanandum or a proposal), `research-agenda-and-prioritisation.md` (ordering the tasks at the end) |
| Rarely: only when the work crosses into another category | `experimental-design.md` and `statistical-inference.md` (designing the test of the theory), `reactivity-and-observer-effects.md`, `adversarial-and-failure-mode-analysis.md` |

## What counts as theoretical research

Theoretical research builds, extends, integrates or criticises explanations. Its output says why something happens, by what mechanism, under what conditions, and what else should therefore be observed. It is found in every discipline: verbal theories with propositions in the social sciences, analytical models in economics and theoretical biology, mechanistic models in the life and cognitive sciences, simulation models of complex systems, and formal theories in the physical sciences.

Its characteristic evidence is explanatory: the range of phenomena accounted for, the coherence of the account, the specification of the mechanism, the derivation of conclusions from assumptions, the robustness of those conclusions, and the predictions that could fail.

### Sub-varieties

| Kind | What it produces | Where it usually fails |
|---|---|---|
| Verbal or propositional theory | Constructs linked by propositions, with a mechanism and boundary conditions | Propositions that cannot fail; mechanisms named but not specified; missing boundary conditions |
| Analytical or mathematical model | Assumptions, equations and derived results (equilibria, comparative statics, dynamics) | Results driven by an idealisation; unclear mapping from model to world |
| Computational or simulation model | A model run to show what its rules produce | Results that are artefacts of parameter choices or implementation; unclear validation target |
| Mechanistic model | Parts, their activities and organisation, producing a phenomenon | A how-possibly mechanism presented as how-actually |
| Theory integration or synthesis | A combined account from several theories | Constructs that do not mean the same thing across the theories; mismatched levels of analysis |
| Theory extension or transfer | An existing theory applied to a new domain | Scope conditions of the original theory ignored |
| Theoretical critique or comparison | An argument that a theory fails or that one beats another | The rival stated weakly; criteria chosen to favour one side |
| Theory built from cases | An explanation induced from observations or case studies | The theory fitted to the very cases cited in its support |

### Boundaries with the other categories

- **Conceptual.** A framework that organises concepts without positing explanatory relations belongs to the conceptual skill. Once the framework claims that its components explain or produce outcomes, it is a theory and belongs here.
- **Philosophical.** Arguments about what explanation, causation or laws are belong to the philosophical skill. Building an explanation of a phenomenon stays here.
- **Technical.** A model built as a tool to design or control something (an engineering model, an algorithm) belongs to the technical skill. A model built to explain a phenomenon stays here, including the mathematics of that model.
- **Empirical.** Testing the theory against data, estimating its parameters, or calibrating a model belongs to the empirical skill. Building and defending the theory stays here.

### Fit test

The material fits this skill when most of its load-bearing claims are explanatory, causal or predictive, or are formal results within a model meant to explain (see `claim-sorting.md`), and the work will be judged by what it explains and predicts.

Signs it belongs elsewhere: the main output is a definition or classification; the conclusion rests on data the researcher collected and analysed; the main output is an artefact or a proof about an artefact; the work defends a normative or foundational thesis.

### Making material fit this category

When the intake finds that the material fits another category better but the researcher wants to continue here, offer the reframings that apply:

- **A philosophical thesis.** Frame the session around the explanatory model the thesis implies or presupposes. Ask the researcher to state what the model would predict and what would count against it.
- **A conceptual framework.** Frame the session around the relations between the framework's components. Ask the researcher to state them as propositions, each with a mechanism and boundary conditions.
- **A method, system or algorithm.** Frame the session around the theory of why it works: a model of its behaviour that predicts when it will succeed and when it will fail.
- **A study.** Frame the session around the theory the study tests, or the explanation offered for its findings. Ask for the theory stated independently of the data.

In each case say what extra material the reframing needs.

## Standards of support

A theory or model is well supported to the extent that:

1. its **explanandum** is precise: it is clear which phenomena it explains, and which it does not;
2. its **mechanism** is specified, not just named;
3. its **conclusions follow** from its assumptions, by valid derivation or simulation;
4. its conclusions are **robust** to changes in assumptions that are not essential to the theory;
5. its **scope conditions** are stated;
6. it makes **predictions that could fail**, including some beyond the phenomena it was built to explain;
7. it **fits the established evidence**, or explains why apparent conflicts are not genuine;
8. it **does better than its rivals** on common criteria, or does something they cannot;
9. it is **parsimonious**, **coherent** with neighbouring well-supported theories, and **fruitful**.

Do not hold a theory to the standard of a completed empirical test; the empirical skill does that. Do hold it to having consequences that a test could check.

## Running the session

### Intake

Run `process/intake.md`, with these category specifics.

**Field 1, the material.** Ask for the theory or model itself: its propositions, equations, rules, diagram or verbal statement, and the phenomena it is meant to explain.

**Field 2, prior work.** Ask specifically for:

- earlier versions of the theory and why they changed;
- the phenomena, stylised facts or findings the theory is built to explain, and where they come from;
- derivations, proofs, simulation code, parameter settings and results;
- the rival theories the researcher knows about and how they characterise them;
- anomalies or findings that do not fit, if any are known;
- feedback received;
- what has been read on the topic.

**Field 4, audience.** Ask which theoretical tradition and which methodological norms the audience holds. What counts as an acceptable idealisation differs sharply between fields.

**Claim sorting.** Expect explanatory, causal, predictive and formal claims. Mark every empirical claim about the phenomena (the explanandum) as needing a source, and every construct whose definition is unclear as a possible conceptual issue.

**Depth signals specific to theory.** Raise depth for a theory with many propositions or a model with many assumptions, a claim to unify or overturn an established theory, a thesis chapter or a journal submission. Lower it for an early model sketch or a single proposition.

### Question labels for this category

Add these to the shared labels in `turn-mechanics.md`:

| Label | Use for questions that... |
|---|---|
| EXPLANANDUM | probe what exactly the theory explains |
| MECHANISM | probe how the cause produces the effect |
| MODEL | probe the structure, equations, rules or derivations of a model |
| SCOPE | probe the boundary conditions under which the theory holds |
| PREDICTION | probe what the theory implies that could be observed, and whether it could fail |
| ROBUSTNESS | probe whether conclusions survive changes to assumptions |
| LEVEL | probe the level of analysis and the link between levels |

### The arc in theoretical research

Follow `process/arc.md`. Here is what each stage means in theoretical work, which moves to draw on, and what to watch for.

#### Stage 1: clarify

Establish the explanandum, the kind of explanation sought, the constructs, the level of analysis and the scope.

- Typical themes: the phenomenon stated precisely, with the facts that make it puzzling; whether the explanation is causal, mechanistic, functional, equilibrium-based, evolutionary or statistical; which constructs carry the theory; the level (individual, group, organisation, system) at which the explanation operates and the level of the phenomenon.
- Moves: `claim-sorting.md`; `concepts.md` sections 1 to 4 for constructs; `hypothesis-and-causal-models.md` section 4.
- Watch for: an explanandum that shifts during the session; constructs that overlap; an explanation pitched at a different level from the phenomenon without an argument linking them.

#### Stage 2: reconstruct

Lay out the theory's structure explicitly and confirm it.

- For a verbal theory: constructs, propositions, the mechanism behind each proposition, boundary conditions, and the implications derived.
- For a formal or simulation model: assumptions, equations or rules, parameters, the derivation or simulation procedure, and the results.
- In both: the chain from assumptions to conclusions. Then steelman it.
- Moves: `hypothesis-and-causal-models.md` sections 1 to 4; `argument-reconstruction.md` for the derivation; `formalisation-and-implementation.md` sections 1 and 2 for formal models; `steelman-and-rivals.md` section 1.
- Watch for: theories whose structure exists only in a diagram; models whose results are reported without the route to them.

#### Stage 3: surface assumptions

Find what the theory takes for granted.

- Typical themes: which assumptions are core to the theory, which are auxiliary, and which are idealisations adopted for tractability; behavioural assumptions about agents; assumptions of independence, stationarity, equilibrium or rationality; ceteris paribus clauses; assumptions about the level of analysis.
- Moves: `assumptions-and-gaps.md`; `hypothesis-and-causal-models.md` section 4; `formalisation-and-implementation.md` section 1.
- Watch for: an idealisation that turns out to drive the main result; an assumption adopted from a parent theory without checking it holds in the new domain.

#### Stage 4: test reasons, evidence and inferential links

Test the derivation, the robustness and the fit.

- Typical themes: whether each conclusion follows from the stated assumptions; whether results survive relaxing an idealisation; whether the mechanism is specified or only named; whether the theory fits the established facts it claims to explain; whether its predictions could fail.
- Moves: `argument-reconstruction.md` sections 3 and 4; `formalisation-and-implementation.md` section 2; `hypothesis-and-causal-models.md` sections 2 to 5; `literature-and-sources.md` section 5.
- Watch for: a theory confirmed only by the cases used to build it; free parameters that let the model fit anything; a mechanism inferred from the outcome it is meant to explain.

#### Stage 5: trace implications, boundary cases and costs

Follow the theory outwards.

- Typical themes: novel predictions beyond the original explanandum; what the world would look like if the theory were true; boundary conditions and what happens at them; consistency with neighbouring theories; implications for policy or practice and what they assume.
- Moves: `hypothesis-and-causal-models.md` sections 3 and 5; `results-to-claims.md` section 2; `reproducibility-and-generalisation.md` part 2; `normative-claims.md` section 7 for practical implications.
- Watch for: predictions that are only restatements of the explanandum.

#### Stage 6: counterexamples, rival interpretations and opposing perspectives

Apply the strongest pressure.

- Typical themes: anomalies the theory gets wrong; the strongest rival explanation of the same phenomena; rivals that predict the same observations through a different mechanism, and the test that would separate them; the perspective of a researcher from a neighbouring field who would explain the phenomenon differently.
- Moves: `counterexamples-and-modal.md` sections 2 and 3; `steelman-and-rivals.md` sections 4 and 5; `behaviour-and-mechanism.md` sections 2 and 3; `hypothesis-and-causal-models.md` section 2.
- Watch for: rivals described in a form their proponents would reject; anomalies absorbed by an auxiliary assumption added after the fact.

#### Stage 7: revise and retest

Invite the researcher's revision and test it.

- Typical themes: whether the revision is principled or ad hoc; whether it narrows scope, adds a mechanism, or changes an assumption; what new predictions the revised theory makes; a pre-commitment to how future results would change it.
- Moves: `hypothesis-and-causal-models.md` section 5; `self-scrutiny.md` part 1.
- Watch for: revisions that protect the theory from the anomaly but make no new prediction.

#### Round allocation

| Stage | Light | Standard | Deep |
|---|---|---|---|
| 1. Clarify | 1 (with 2) | 1 | 1-2 |
| 2. Reconstruct | (with 1) | 1-2 | 2 |
| 3. Assumptions | 1 | 1 | 2 |
| 4. Derivation, robustness and fit | 1 | 2 | 2-3 |
| 5. Implications and predictions | (folded into 6) | 1 | 1-2 |
| 6. Anomalies and rivals | 1 | 1-2 | 2-3 |
| 7. Revise and retest | 0-1 | 1 | 1-2 |
| Total | 4-5 | 8-10 | 11-15 |

Theoretical work typically fails at stage 2 (the structure was never made explicit), stage 4 (conclusions that do not follow or are not robust), and stage 6 (a rival that explains the same facts), so those get the extra rounds.

## Characteristic weaknesses

| Weakness | Usual class | Probe with |
|---|---|---|
| The explanandum is vague or shifts | Needs clarification | `hypothesis-and-causal-models.md` section 4 |
| The mechanism is named but not specified, or redescribes the outcome | Needs argument | `hypothesis-and-causal-models.md` section 3 |
| The theory accommodates any possible result | Fatal, or repairable by adding scope conditions | `hypothesis-and-causal-models.md` section 5 |
| A conclusion does not follow from the stated assumptions | Repairable or fatal | `argument-reconstruction.md` section 3 |
| A main result is driven by an idealisation | Scope-limiting or repairable | `hypothesis-and-causal-models.md` section 4 |
| Scope conditions are missing | Scope-limiting | `reproducibility-and-generalisation.md` part 2 |
| An individual-level mechanism explains an aggregate pattern without an aggregation argument | Needs argument | `assumptions-and-gaps.md` section 4 |
| A rival explanation predicts the same observations | Needs evidence (a discriminating test) | `steelman-and-rivals.md` section 4 |
| The theory is supported only by the cases it was built from | Needs evidence | `hypothesis-and-causal-models.md` section 5 |
| Constructs are ill-defined or overlap | Needs clarification | `concepts.md` sections 4 and 5 |
| Conflict with established findings is not addressed | Needs argument | `literature-and-sources.md` section 1 |
| Free parameters let the model fit anything | Repairable | `formalisation-and-implementation.md` section 1 |
| A how-possibly mechanism is presented as how-actually | Scope-limiting | `behaviour-and-mechanism.md` section 3 |
| Simulation results depend on unexamined implementation choices | Needs evidence | `formalisation-and-implementation.md` section 5 |
| Unification claimed where theories are only placed side by side | Needs argument or presentational | `steelman-and-rivals.md` section 4 |

## Example rounds

Illustrative only. Adapt the content to the researcher's material.

The researcher's theory: "Firms adopt new technologies in waves because each adoption by a competitor lowers the perceived risk of adopting for the rest."

**Round 2, reconstruct.** Round 1 fixed the explanandum as the S-shaped, clustered timing of adoption within an industry.

```text
What I heard: the phenomenon is clustered adoption timing within an industry, not
adoption rates across industries. You said "perceived risk" means managers'
uncertainty about whether the technology will work in their own operations, and that
the theory operates at the level of the individual firm's decision, with waves as
the aggregate result.

Round 2 of about 9 · Reconstruct · Theme: the chain from one firm's adoption to the
next firm's decision

The theory's claim lives in the steps between "a competitor adopts" and "my perceived
risk falls". Until those steps are explicit, it is hard to tell what the theory
predicts that a rival would not.

1. [MECHANISM] How does a competitor's adoption reach a manager's risk estimate: by
   observing the competitor's results, by the fact of adoption alone, through shared
   suppliers or consultants, or through staff moving between firms?
2. [MODEL] Can you state the theory as two or three propositions, each linking one
   construct to another, with the direction of the effect?
3. [LEVEL] What turns many individual decisions into a wave? Is it enough that each
   adoption lowers risk for others, or does the theory need something about how
   firms are connected?
4. [SCOPE] Does the mechanism need competitors to be visible to each other? What
   happens in an industry where adoption is secret?
5. [PREDICTION] If the theory is right, what pattern should appear in which firms
   adopt next, beyond the overall S-shape?

Answer any or all of these, in any order.
```

**Round 7, rivals.** The researcher has specified the mechanism as learning from observed results among firms that can see each other, with waves spreading along visibility networks.

```text
What I heard: you now hold three propositions. P1: a firm's perceived risk falls
when a visible competitor's adoption produces observable results. P2: lower
perceived risk raises the probability of adoption. P3: waves spread along networks
of mutual visibility. You accepted that P3 is what separates your account from a
simple contagion story, and that the theory needs results to be observable, so it
does not apply to technologies whose benefits take years to show.

Round 7 of about 9 · Rivals · Theme: whether a common shock explains the same waves

A rival explanation says firms adopt together because they face the same change at
the same time (a price fall, a regulation, a supplier switching), with no learning
at all. If it predicts the same clusters, the waves alone do not support your theory.

1. [RIVAL] If the technology's price fell sharply in one year, what adoption pattern
   would the common-shock account predict? How would it differ from yours?
2. [PREDICTION] Your P3 says adoption follows visibility networks. Would a common
   shock also produce adoption that tracks those networks, for example if visible
   competitors share suppliers?
3. [COUNTEREXAMPLE] Suppose two equally visible competitors adopt, one with good
   results and one with poor results. What does your theory predict for their
   neighbours, and what does the rival predict?
4. [PERSPECTIVE] An economist would probably reach first for prices and costs. Which
   observation would most quickly persuade them that learning matters?
5. [CONDITION] What finding would make you treat the common shock as the main
   explanation and learning as a secondary one?

Answer any or all of these, in any order.
```

## Checkpoints

Use `process/checkpoints.md`. Add two entries to the ledger:

- **Current theory**: the propositions, equations or mechanism as they now stand, with revisions since the last checkpoint marked.
- **Predictions and rivals**: the predictions the theory now makes, and the strongest rival with the observation that would separate them.

## The audit

Use `process/audit-skeleton.md`, filling its shared sections as follows and adding the category sections below.

### Filling the shared sections

- **Section 2, claim inventory**: mark empirical claims about the explanandum as needing sources.
- **Section 3, clarified terms**: the constructs of the theory, each with its definition and what distinguishes it from its neighbours.
- **Section 4, reconstructed structure**: the propositions or equations, the mechanism, and the derivation chain from assumptions to conclusions; then the steelman.
- **Section 5, assumptions**: classify each as core, auxiliary or idealisation, and record whether the main conclusions are robust to relaxing it.
- **Section 6, strongest support**: the phenomena explained and how well, and any prediction already borne out, with sources.
- **Section 7, strongest challenge**: the anomaly or rival theory that most threatens the account.
- **Section 12, what the work does not license**: include, where they apply, that a model result is not a fact about the world without a mapping argument, that a how-possibly mechanism does not show how-actually, and that fitting the cases a theory was built from is not confirmation.
- **Section 15, research tasks**: typical tasks are a robustness analysis on a named assumption, deriving a novel prediction, identifying a case that discriminates between the theory and its rival, specifying the mechanism at a named step, and stating scope conditions.

### Category sections

Insert after shared section 1:

- **1a. Explanandum.** The phenomena the theory explains, stated precisely with their sources, and phenomena it does not attempt to explain.

Insert after shared section 5:

- **5a. Model assumption ledger.** Each assumption, whether core, auxiliary or idealisation, and whether each main conclusion survives relaxing it.
- **5b. Scope conditions.** The conditions under which the theory is claimed to hold, and the cases at the boundary.

Insert after shared section 7:

- **7a. Hypothesis tree and rivals.** The theory's main predictions, the rival accounts, what each predicts, and the observation or test that would discriminate between them.

Insert after shared section 13:

- **13a. Pre-commitment.** For each discriminating test, how each possible result would change the theory.

## Report variants

Use the shells in `process/report-variants.md`.

- **Supervision note.** Tie each weakness to a proposition, assumption or derivation step. Research tasks are typically a robustness check, a mechanism specification, a novel prediction, or a comparison with a named rival.
- **Examiner's report.** The examiner covers the explanandum, constructs, mechanism, derivation, assumptions, scope, rival theories, testability and contribution to theory. Quote the wording where the theory claims more than it explains.
- **Reviewer's report.** Judge the theoretical contribution (a new explanation, an integration, a boundary condition, a resolved anomaly), the specification of the mechanism, testability, relation to rival theories and robustness. Requests for empirical tests usually belong under "Beyond scope" unless the paper claims empirical support.

## Written memo

Use the memo structure in `process/report-variants.md`. Open with the three most consequential questions, which in theoretical work are usually about the mechanism, the assumption driving the main result, and the strongest rival. Then follow the theory proposition by proposition or the model step by step, and close with the audit.

## When the material crosses into another category

Sessions stay in one category. When a part of the material belongs elsewhere:

- testing the theory against data, or estimating its parameters: note it for `empirical-research-socratic`;
- defining or distinguishing its constructs at length: note it for `conceptual-research-socratic`;
- proving mathematical properties of the model in their own right: examine them here with `formalisation-and-implementation.md`, or note them for `technical-research-socratic` if the proofs are the main contribution;
- normative claims drawn from the theory: note them for `philosophical-research-socratic`.

Record each as an open item in the audit.

## Never

These add to the never-rules in the shared process modules.

- Never treat a theory's fit with the cases it was built from as confirmation.
- Never treat a model's result as a fact about the world without an argument that the model's assumptions hold for the case.
- Never accept a mechanism because it is plausible; ask what evidence there is for it independently of the outcome it explains.
- Never invent findings that would support or refute the theory. Mark them `[EVIDENCE NEEDED]` or `[SOURCE NEEDED]`.
- Never call a theory unfalsifiable without first checking whether stating its scope conditions and auxiliary assumptions would give it testable consequences.
- Never let the session end without the audit or the chosen report, unless the researcher declines it.
