# Study design, controls and rival explanations

Use this move when a study is being designed or has been run: experiments, quasi-experiments, observational studies, surveys, computational experiments, benchmarks, field studies, case studies and qualitative inquiry. The question throughout is whether the design can support the conclusion drawn from it, against the rival explanations that could produce the same result.

## Use when

- A study design is proposed or has been carried out.
- An effect has been observed or is expected.
- Baselines, comparisons or controls are in question.
- The researcher needs a minimum defensible design.

## 1. The comparison

- What exactly is the treatment, intervention, condition or exposure? What is the comparison?
- What question does each comparison answer? Is that the question the conclusion needs?
- Is the comparison fair: equal effort, time, resources, tuning, access and information on each side? Does the favoured condition receive any advantage the others lack?

## 2. Sampling

- What are the units (people, organisations, documents, sites, items, tasks, models, runs, seeds)? How were they chosen?
- Who or what was excluded, and why? Could exclusion create the result?
- Is the sample representative of the population the conclusion is about? If not, what population does it represent?
- How many independent units are there, as opposed to repeated observations of the same units?

## 3. Allocation and bias control

- How were units assigned to conditions? Was it randomised? Could the assignment correlate with the outcome?
- Was anything blinded: participants, experimenters, raters, analysts?
- Was order counterbalanced where order could matter?
- Were hypotheses, measures, analysis plan, stopping rules and exclusion criteria fixed before seeing the results?

## 4. Baselines and controls

- What baselines are included: no intervention, a simple heuristic, the current standard, the best existing alternative, an upper bound?
- Does each baseline get comparable effort and resources? A weak baseline makes any method look good.
- **Negative control**: what should stay unchanged if the proposed mechanism is real? Was it checked?
- **Positive control**: can the procedure detect an effect known to exist? Was it checked?
- **Manipulation check**: did the intervention actually change what it was meant to change?
- **Ablation**: which component of the intervention produces the effect? Has each been removed in turn?

## 5. Rival explanations

Reconstruct the causal structure the conclusion assumes (see `hypothesis-and-causal-models.md`), then list what else could produce the result:

- confounders that influence both condition and outcome;
- selection effects in who or what entered the study;
- measurement artefacts and rater effects;
- order, fatigue, practice and learning effects;
- regression to the mean;
- differential dropout or missing data;
- reactivity to being studied (see `reactivity-and-observer-effects.md`);
- implementation error;
- chance (see `statistical-inference.md`).

Rank the rivals by plausibility and by how much each would change the conclusion. Do not leave an unranked list. For the strongest rival, find the cheapest test that would discriminate it.

## 6. Observational and quasi-experimental designs

When assignment was not controlled:

- What design feature substitutes for randomisation: matching, stratification, adjustment, a natural experiment, an instrument, a discontinuity, comparison of changes over time?
- What assumption does that design rely on, and how plausible is it here?
- What unmeasured variable could still explain the result?

## 7. Qualitative and case-based designs

- Why these cases, sites or participants? Were they chosen to be typical, extreme, diverse, critical, or convenient?
- How was data collection decided: what was asked, observed or collected, and when was it enough (saturation)?
- How were interpretations checked: by triangulation across sources, by participants, by a second analyst, by searching for disconfirming cases?
- How does the researcher's position shape what was seen and how it was read?
- What claims does the design support: about these cases, about a mechanism, about a population?

## 8. The result most likely to be overread

- Which result in this study would be most tempting to overinterpret?
- What would the result look like if the effect were absent but the design flawed in the way most likely here?

## Watch for

- A design that cannot produce the result that would count against the hypothesis.
- Baselines chosen after seeing which ones the method beats.
- Positive controls missing, so a null result cannot be interpreted.
- Many outcome measures with only the favourable ones reported.
- A qualitative study judged by quantitative standards it never claimed to meet, or the reverse.

## Artefacts

- **Three defects most likely to change the conclusion**, each with the design change that would address it.
- **Minimum defensible design**, and a stronger design if resources allow.
- **Baseline and control matrix**: each comparison, its purpose, whether it was run, and what each possible result would mean.
- **Pre-specification list**: hypotheses, primary and secondary measures, analysis plan, exclusion rules, stopping rules and decision rules, in the form of a preregistration.
- **Ranked rivals**: the strongest rival explanations with the cheapest discriminating test for each.
