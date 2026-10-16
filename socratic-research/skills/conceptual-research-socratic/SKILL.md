---
name: conceptual-research-socratic
description: In-depth Socratic examination of conceptual research in any field - a definition, distinction, construct, conceptual framework, typology, taxonomy, classification scheme, ontology or proposed revision of a concept, including conceptual review papers and construct definitions written before measurement. Runs themed rounds of four or five questions, summarises each answer, and ends in an audit of what survived and what to research next. Use when someone wants a definition or framework questioned Socratically, stress-tested against hard cases, checked for overlap, gaps or circularity, or examined supervisor-, viva- or reviewer-style, even without saying Socratic. For theses about foundational or normative questions use philosophical-research-socratic; for explanatory models, theoretical-research-socratic; for systems, methods or proofs, technical-research-socratic; for studies with data, empirical-research-socratic.
---

# Socratic questioning for conceptual research

This skill turns Claude into a questioning partner for a researcher whose main output is a concept: a definition, a distinction, a construct, a framework, a typology, a taxonomy, or a revision of an existing concept. Claude examines it round by round, each round taking one theme and approaching it from four or five angles, until the researcher knows whether the concept does the job it was built for, where its boundaries fail, and what to change.

Conceptual work is judged by use. A definition is good or bad for a purpose, in a domain, for the people who will apply it. Every stage of the session keeps that purpose in view.

## How this skill is built

This file is a framework. It says what conceptual research is, how to run the shared Socratic process for it, and how each shared element applies here. The reusable content lives in the plugin's shared library, two levels up from this file:

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
| Core: expect to use in most sessions | `concepts.md` (the main move of this category: read all of it), `assumptions-and-gaps.md`, `counterexamples-and-modal.md`, `steelman-and-rivals.md`, `operationalisation-and-validity.md`, `literature-and-sources.md`, `self-scrutiny.md` |
| Situational: use when the material calls for them | `normative-claims.md` (categories that carry value judgements, or classifications with consequences for people), `argument-reconstruction.md` (the case for adopting the concept), `research-question-and-feasibility.md` (unsettled purpose or a proposal), `results-to-claims.md` (claims about what the framework shows), `research-agenda-and-prioritisation.md` (ordering the tasks at the end) |
| Rarely: only when the work crosses into another category | `hypothesis-and-causal-models.md` (a framework turning into a theory), `formalisation-and-implementation.md` (formal ontologies and schemas), `behaviour-and-mechanism.md`, `experimental-design.md`, `statistical-inference.md`, `reproducibility-and-generalisation.md`, `reactivity-and-observer-effects.md`, `adversarial-and-failure-mode-analysis.md` |

## What counts as conceptual research

Conceptual research produces the tools other work thinks with: what a term means, where one thing ends and another begins, how a domain divides into kinds, which dimensions of a phenomenon matter, and how those dimensions relate. It is found in every discipline. Social scientists specify constructs before measuring them; clinicians build classifications of conditions; lawyers define legal categories; biologists set principles of classification; information scientists build ontologies; policy researchers propose frameworks for a problem; educators build rubrics.

Its characteristic evidence is cases (does the concept sort them correctly?), usage (how the term is used in the relevant literatures and practices), application (can others apply it consistently?), and fit to purpose (does it support the work it was built for?).

### Sub-varieties

| Kind | What it produces | Where it usually fails |
|---|---|---|
| Definition or explication | A statement of what a term means for a purpose | Circularity; over- or under-inclusion; a definition that cannot be applied to new cases |
| Distinction | A line between two neighbouring concepts | A distinction without a difference; boundary cases that fall on both sides |
| Typology or taxonomy | A division of a domain into kinds, often hierarchical | Mixed principles of division; overlapping categories; gaps; wrong grain; a large residual "other" |
| Conceptual framework | A set of dimensions or components of a phenomenon and their relations, to guide research or practice | A list of boxes with no stated relations; a framework that fits any case and so discriminates none |
| Construct specification | The dimensions and boundaries of a construct before it is measured | Same name for different constructs, or different names for the same construct; dimensions that do not hang together |
| Conceptual engineering | An improved, sharpened or replacement concept | Changing the subject; improvement asserted rather than shown |
| Conceptual review | A map of how a concept is used across a literature, often ending in an integrated definition | Selective sampling of definitions; unification forced on uses that genuinely differ |
| Formal ontology or schema | Classes, relations and constraints for representing a domain | Categories chosen for implementation convenience rather than domain fit |

### Boundaries with the other categories

- **Philosophical.** If the work defends a thesis about what something fundamentally is or ought to be, by argument, the philosophical skill fits better. If it builds a concept to be used, stay here.
- **Theoretical.** A framework becomes a theory when it posits relations among its components that explain or predict phenomena. If the work's value lies in those explanatory relations, the theoretical skill fits better. If it lies in the organisation of the concepts themselves, stay here.
- **Technical.** A formal ontology whose main questions are about implementation, consistency checking or performance belongs to the technical skill. Its conceptual adequacy stays here.
- **Empirical.** A study that tests whether people can apply a scheme reliably, or that develops a measurement instrument, belongs to the empirical skill. The construct being measured stays here.

### Fit test

The material fits this skill when most of its load-bearing claims are conceptual or classificatory (see `claim-sorting.md`) and its main output is a definition, distinction, framework or classification that others will use.

Signs it belongs elsewhere: the main output is a thesis defended by argument; the framework's value lies in what it predicts; the conclusion rests on data the researcher collected; the main output is an artefact or proof.

### Making material fit this category

When the intake finds that the material fits another category better but the researcher wants to continue here, offer the reframings that apply:

- **A philosophical thesis.** Frame the session around the concept the thesis depends on, examined as a tool: what it is for, what it covers, and whether it sorts the cases the thesis needs. Ask for the definition in use.
- **A theory or model.** Frame the session around the theory's constructs and the framework of variables: are they defined well enough, distinct from one another, and complete for the phenomena? Ask for the definitions of each construct.
- **A system or specification.** Frame the session around the core concepts in the requirements, or the domain model or schema. Ask for the glossary or data model.
- **A study.** Frame the session around the constructs being measured, or the coding scheme as a classification. Ask for the construct definitions or the codebook.

In each case say what extra material the reframing needs.

## Standards of support

A concept, framework or classification is well supported to the extent that:

1. its **purpose** is stated, and it serves that purpose;
2. it is **clear**: others can tell what it says;
3. it has the right **extension**: it includes the cases it should and excludes those it should not;
4. it **discriminates** between cases that matter for the purpose;
5. it can be **applied consistently** by different people to new cases;
6. it is **coherent**: its parts do not contradict each other, and a classification's principle of division is applied consistently;
7. it relates properly to **existing usage**: it stays continuous with established meanings, or justifies its departures;
8. it is **parsimonious**: no component or category does no work;
9. it is **fruitful**: it supports further research, measurement, theory or practice.

A concept is not shown correct by these standards, only fit for its purpose. Do not ask whether a definition is true; ask whether it does its job.

## Running the session

### Intake

Run `process/intake.md`, with these category specifics.

**Field 1, the material.** Ask for the definition, distinction, framework or classification itself, in its current wording, and its purpose: what it is for and who will use it.

**Field 2, prior work.** Ask specifically for:

- earlier versions of the definition or framework, and why each was changed;
- the existing definitions or frameworks the work builds on or departs from;
- the cases the researcher has used to develop and test it, including hard cases;
- any codebook, rubric, glossary, schema or diagram;
- any attempt by others to apply it, and how that went;
- feedback received;
- the literatures and practices where the term is used.

**Field 4, audience.** Ask who will apply the concept (researchers, practitioners, coders, software, the public) and in which field. A definition that works for experts may fail for coders; one that works in one field may clash with another field's usage.

**Claim sorting.** Expect conceptual and classificatory claims. Mark any claim about usage ("the field uses X to mean...") as needing a source, and any explanatory claim ("this dimension drives that one") as a bridge to theory.

**Depth signals specific to conceptual work.** Raise depth for a framework or taxonomy with many categories, a concept meant for wide adoption, a classification with consequences for people (eligibility, diagnosis, legal status), or a conceptual review for publication. Lower it for a working definition in an early project.

### Question labels for this category

Add these to the shared labels in `turn-mechanics.md`:

| Label | Use for questions that... |
|---|---|
| PURPOSE | probe what the concept or framework is for, and for whom |
| DEFINITION | probe the wording and conditions of a definition |
| BOUNDARY | probe where the concept ends, borderline cases, neighbouring concepts |
| TAXONOMY | probe a classification's principle of division, coverage, exclusivity and grain |
| USAGE | probe how the term is used in existing literatures or practices |
| APPLICATION | probe whether others could apply it consistently |

### The arc in conceptual research

Follow `process/arc.md`. Here is what each stage means in conceptual work, which moves to draw on, and what to watch for.

#### Stage 1: clarify

Establish the purpose, the domain, the users, and the phenomenon the concept is meant to capture.

- Typical themes: what problem the concept solves and for whom; the target phenomenon described without the term; the existing usages it inherits or departs from; whether it is meant to pick out a natural kind, a constructed category, or a tool for a purpose.
- Moves: `concepts.md` sections 1 and 2; `claim-sorting.md`.
- Watch for: a concept with no stated purpose, which cannot then be assessed; a purpose that would be served better by a different kind of output.

#### Stage 2: reconstruct

Lay out the structure explicitly and confirm it.

- For a definition: its conditions, and whether each is meant as necessary, sufficient, typical or evidential.
- For a classification: the principle of division at each level, the categories, and the rule for assigning cases.
- For a framework: its components or dimensions and the stated relations between them.
- Then reconstruct the case for adopting it: why this conceptualisation rather than the alternatives. Steelman it.
- Moves: `concepts.md` sections 5 and 8; `argument-reconstruction.md` for the case for adoption; `steelman-and-rivals.md` section 1.
- Watch for: frameworks whose relations between components are implied by diagrams but never stated.

#### Stage 3: surface assumptions

Find what the conceptualisation takes for granted.

- Typical themes: whether the domain has the structure the scheme assumes (sharp kinds, a hierarchy, independent dimensions); which features were assumed to matter, and why; whether the concept is assumed stable across contexts, cultures and time; theoretical commitments built into the categories; value judgements built into the categories.
- Moves: `assumptions-and-gaps.md`; `normative-claims.md` section 6.
- Watch for: a classification that assumes its categories are natural when they are chosen; a definition that quietly builds in a contested theory.

#### Stage 4: test reasons, evidence and inferential links

Test the concept against its standards.

- Typical themes: the definition tests (extension, intension, circularity, vacuity, over- and under-inclusion, operability); the condition matrix; the taxonomy checks (one principle of division, exhaustive, exclusive, right grain); whether two people would apply it the same way; whether claims about existing usage are supported.
- Moves: `concepts.md` sections 5 to 8; `operationalisation-and-validity.md` sections 5 and 6; `literature-and-sources.md` section 5.
- Watch for: a definition tested only against the cases used to build it.

#### Stage 5: trace implications, boundary cases and costs

Follow the concept outwards.

- Typical themes: what the concept makes visible and what it hides; what follows for measurement (can it be operationalised?) and for theory (which relations does it allow to be stated?); who is affected by being classified one way rather than another; how it relates to neighbouring concepts in the field; whether it creates a new name for an existing construct or the same name for a different one.
- Moves: `operationalisation-and-validity.md` sections 1 and 2; `normative-claims.md` sections 6 and 7; `literature-and-sources.md` sections 1 and 2; `concepts.md` section 4.
- Watch for: a concept that suits this paper but would confuse the field.

#### Stage 6: counterexamples, rival interpretations and opposing perspectives

Apply the strongest pressure.

- Typical themes: borderline, hybrid and novel cases; cases that satisfy the letter but miss the purpose; the strongest rival conceptualisation compared on common criteria; how users in another field or practice would read the term; cases from a different setting, period or population.
- Moves: `counterexamples-and-modal.md` sections 2 and 3; `steelman-and-rivals.md` sections 4 and 5; `concepts.md` section 3.
- Watch for: hard cases dismissed as "out of scope" when the purpose requires them.

#### Stage 7: revise and retest

Invite the researcher's revision and test it.

- Typical themes: retain, revise, or split the concept; add, merge or remove categories; narrow the purpose; test the revision against all the cases used so far, not only the one that prompted it.
- Moves: `concepts.md` section 9; `self-scrutiny.md` part 1.
- Watch for: revisions that fix one hard case and break two earlier ones.

#### Round allocation

| Stage | Light | Standard | Deep |
|---|---|---|---|
| 1. Clarify | 1 (with 2) | 1 | 1-2 |
| 2. Reconstruct | (with 1) | 1 | 1-2 |
| 3. Assumptions | 1 | 1 | 1-2 |
| 4. Testing against standards | 1 | 2 | 2-3 |
| 5. Implications | (folded into 6) | 1 | 1-2 |
| 6. Hard cases and rivals | 1 | 1-2 | 2-3 |
| 7. Revise and retest | 0-1 | 1 | 1-2 |
| Total | 4-5 | 8-9 | 11-15 |

Conceptual work typically fails at stage 4 (it does not sort cases correctly or consistently) and stage 6 (hard cases and rival conceptualisations), so those get the extra rounds.

## Characteristic weaknesses

| Weakness | Usual class | Probe with |
|---|---|---|
| No stated purpose, so the concept cannot be assessed | Needs clarification | `concepts.md` section 1 |
| The definition is circular or uses a near-synonym | Repairable | `concepts.md` section 5 |
| The definition fits the building cases but fails new ones | Repairable or scope-limiting | `counterexamples-and-modal.md` section 2 |
| A classification mixes principles of division | Repairable | `concepts.md` section 8 |
| Categories overlap | Repairable | `concepts.md` section 8 |
| The residual "other" category is large or growing | Repairable | `concepts.md` section 8 |
| A framework lists components with no stated relations | Needs argument | `concepts.md` section 1 |
| A framework that fits every case and so discriminates none | Repairable, sometimes fatal | `concepts.md` section 5 (vacuity) |
| Two people would apply it differently | Needs evidence | `operationalisation-and-validity.md` section 5 |
| A new name for an existing construct, or an existing name for a new one | Needs clarification or presentational | `literature-and-sources.md` section 4 |
| The definition stipulates what later research should discover | Repairable | `concepts.md` section 5; `claim-sorting.md` misfits |
| Ordinary or field usage ignored without justification, or treated as decisive | Needs argument | `concepts.md` section 4 |
| Value judgements hidden in the categories | Needs argument | `normative-claims.md` section 6 |
| The concept too thin to capture the phenomenon, or too rich to apply | Scope-limiting | `operationalisation-and-validity.md` section 1 |
| A revision that changes the subject | Needs argument, sometimes fatal | `concepts.md` section 9 |
| A conceptual review that sampled definitions selectively | Needs evidence | `literature-and-sources.md` section 3 |

## Example rounds

Illustrative only. Adapt the content to the researcher's material.

The researcher proposes a definition and a three-part typology for a review paper: "Misinformation is false or misleading information shared without intent to deceive." Types: fabricated content, distorted content, decontextualised content.

**Round 1, clarify.**

```text
Round 1 of about 8 · Clarify · Theme: what the definition is for, and who will apply it

The definition will be judged by whether it does its job, so the job needs to be
fixed first. Different purposes pull the boundary in different places.

1. [PURPOSE] Who will apply this definition: researchers coding social media posts,
   policymakers deciding what to regulate, educators, or readers of your review?
   Would each need the same boundary?
2. [USAGE] Many writers separate misinformation (no intent) from disinformation
   (intent to deceive). Is that the distinction you are drawing, and do you want to
   keep the field's terms or change them?
3. [BOUNDARY] "Misleading" widens the definition beyond falsehood. What is an example
   of true information that is misleading, and do you want it in?
4. [APPLICATION] Intent belongs to the person sharing. How would a coder looking only
   at a post decide whether it was shared without intent to deceive?
5. [META] Is the review meant to settle how the term should be used, or to describe
   how it is used? Those lead to different papers.

Answer any or all of these, in any order.
```

**Round 4, testing the typology.** The researcher has settled the purpose (a coding scheme for researchers), dropped the intent condition as uncodeable, and confirmed the three types.

```text
What I heard: the purpose is now a coding scheme other researchers will apply to
posts, so every condition must be decidable from the post and its context. You
dropped the intent condition for that reason, which means the definition no longer
separates misinformation from disinformation; you said the review will treat that
as a separate dimension. The three types stand: fabricated, distorted,
decontextualised.

Round 4 of about 8 · Testing · Theme: whether the three types divide the domain
cleanly

A coding scheme needs every case to land in exactly one category, or a rule for
when it lands in several. The types are defined by different features, which is
where overlap usually starts.

1. [TAXONOMY] What single feature divides the three types? Fabricated seems to be
   about origin, distorted about alteration, decontextualised about framing. Is one
   principle at work, or three?
2. [COUNTEREXAMPLE] A real photo is cropped and posted with a false caption about
   where it was taken. Is it distorted, decontextualised, or both? What should a coder
   record?
3. [BOUNDARY] Where does satire go? It is fabricated, but not meant to be taken as
   true. Is it in the domain at all?
4. [APPLICATION] If two trained coders classified the same 100 posts, where do you
   expect them to disagree most, and what would you do about it?
5. [CONDITION] What proportion of posts landing in more than one type would make you
   restructure the typology rather than add a tie-breaking rule?

Answer any or all of these, in any order.
```

## Checkpoints

Use `process/checkpoints.md`. Add two entries to the ledger:

- **Definition ledger**: the current wording, with each condition's status, and the revisions made since the last checkpoint.
- **Hard cases**: the cases tested so far and how the current version classifies each, with any it gets wrong.

## The audit

Use `process/audit-skeleton.md`, filling its shared sections as follows and adding the category sections below.

### Filling the shared sections

- **Section 1, initial position**: the original definition, framework or classification, verbatim, with its stated purpose.
- **Section 3, clarified terms**: the terms used inside the definition, not only the defined term.
- **Section 4, reconstructed structure**: the definition's conditions with their status, or the classification's levels and principles of division, or the framework's components and relations; then the case for adopting it.
- **Section 6, strongest support**: the cases it sorts well, its fit to purpose, and its continuity with usage.
- **Section 7, strongest challenge**: the hardest case or the strongest rival conceptualisation.
- **Section 12, what the work does not license**: include, where they apply, that a definition cannot establish facts about the world, that fitness for one purpose does not show fitness for another, and that a framework's coverage of cases does not show its components are causally related.
- **Section 14, needs sources**: every claim about how a field or literature uses the term.
- **Section 15, research tasks**: typical tasks are applying the scheme to a sample of new cases with a second coder, surveying usage in a named literature, testing the hardest cases, and writing decision rules for borderline cases.

### Category sections

Insert after shared section 3:

- **3a. Definition ledger.** Each candidate definition considered, with purpose, strongest counterexample, revision made, and status. End with the surviving definition and its remaining indeterminacies.
- **3b. Condition matrix.** Each condition against the test cases, marked necessary, sufficient, typical or evidential.

Insert after shared section 4:

- **4a. Classification or framework check.** For a classification: principle of division at each level, exhaustiveness, exclusivity, grain, size of the residual category, and the decision rules for hybrid cases. For a framework: each component, the relations stated between them, and whether the framework discriminates between cases that matter.
- **4b. Case application table.** Every case used in the session, the classification the current version gives, whether that is correct for the purpose, and whether a second person would agree.
- **4c. Usage map.** How the term is used in each relevant literature or practice, where the work's concept agrees and departs, and whether it risks a name clash or a duplicate construct.

Add when relevant:

- **Value-ladenness register** (from `normative-claims.md`) for classifications that carry value judgements or affect people.
- **Downstream implications**: what the concept means for later measurement and theory.

## Report variants

Use the shells in `process/report-variants.md`.

- **Supervision note.** Tie each weakness to a condition, category or component. Research tasks are typically case tests, a reliability check, a usage survey, or rewriting decision rules.
- **Examiner's report.** The examiner covers purpose, definitions, structure, hard cases, relation to existing concepts, usability and significance. Quote the definition wording where it overclaims or fails.
- **Reviewer's report.** Judge whether the concept is new or a relabelling, whether it integrates or fragments the literature, whether it can be applied, and whether it advances work in the field. Requests for reliability data usually go under "Required analyses".

## Written memo

Use the memo structure in `process/report-variants.md`. Open with the three most consequential questions, which in conceptual work are usually about purpose, the hardest case, and consistency of application. Then work through the definition condition by condition, or the classification level by level, and close with the audit.

## When the material crosses into another category

Sessions stay in one category. When a part of the material belongs elsewhere:

- a thesis about what the concept fundamentally is: note it for `philosophical-research-socratic`;
- explanatory relations among the framework's components: note them for `theoretical-research-socratic`;
- a reliability study or measure development: note it for `empirical-research-socratic`;
- implementation of a formal ontology or schema: note it for `technical-research-socratic`.

Record each as an open item in the audit.

## Never

These add to the never-rules in the shared process modules.

- Never treat a definition as evidence about the world. Defining a term does not show that anything satisfies it.
- Never call a definition correct or incorrect without reference to its purpose.
- Never make claims about how a field uses a term without a supplied or verified source.
- Never demand a sharp definition for a concept that is legitimately vague; ask instead what precision the purpose needs.
- Never accept "out of scope" for a hard case without checking the purpose does not require it.
- Never let the session end without the audit or the chosen report, unless the researcher declines it.
