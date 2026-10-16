# Statistical inference and null results

Use this move when numbers support the conclusion: estimates, comparisons, correlations, tests, models, intervals, rates or aggregated scores. It also covers interpreting null, negative and unexpected results.

## Use when

- The conclusion rests on a quantitative result.
- A difference, effect, association or trend is reported.
- An expected effect did not appear.
- Many analyses, comparisons or outcomes are involved.

## 1. What is being estimated

- What quantity is the conclusion about (the estimand)? A mean difference, a proportion, a risk ratio, a correlation, a rank, a rate?
- Does the analysis estimate that quantity, or something nearby?
- What population or process does the estimate describe?

## 2. Units and independence

- What is the sampling unit? How many independent units are there?
- Are repeated measurements of the same unit being counted as independent? (Several responses from one person, several items from one source, several outputs from one prompt, several runs from one seed.) The effective sample size is usually the number of independent units, not the number of observations.
- Is there clustering (by site, group, rater, time) that the analysis must account for?

## 3. Size and uncertainty

- What are the effect sizes, and what are their intervals? A p-value alone says little.
- Is the effect large enough to matter in practice? Who decides what matters?
- What is the smallest effect this design could have detected (power, sensitivity)?
- Is the uncertainty interval wide enough that the data are compatible with both a meaningful effect and none?

## 4. Many analyses

- How many comparisons, outcomes, subgroups or model specifications were examined? How many are reported?
- Were the analyses chosen before or after seeing the data?
- Has the analysis been corrected for multiple comparisons, or are the extra analyses labelled as exploratory?
- Would a different reasonable analysis (different covariates, exclusions, transformations, aggregation) give a different answer?

## 5. Robustness

- Does the conclusion survive a different aggregation, a model that accounts for grouping, or removing the most influential unit or task?
- How are outliers and missing data handled? Would a different reasonable choice change the result?
- Are the model's distributional assumptions plausible? What happens if they are relaxed?
- Is the average hiding variation that matters: subgroups that go the other way, or rare severe cases?
- Is the tail, rather than the mean, what the conclusion is really about?

## 6. Alternative frameworks

- If priors are used, how were they chosen, and how sensitive is the conclusion to them?
- Would an estimation approach (intervals, posterior distributions) answer the question better than a test?

## 7. Null, negative and unexpected results

- Is this evidence of absence, or absence of evidence?
- Could the study have detected the effect if it were there? Did the positive controls work?
- Was the manipulation successful? Was the measure sensitive in the relevant range?
- Could an implementation error explain the result?
- Is the null local: to one sample, setting, version, task, or condition?
- Which explanations fit: the hypothesis is false; the effect exists but the test lacked sensitivity; the measure missed the concept; the implementation failed; a confounder masked the effect; the mechanism differs from the one proposed?
- Which follow-up would best separate those explanations?

Decide among: replicate, redesign, restrict the claim's scope, or abandon. Record what the null result does establish.

## Watch for

- Statistical significance treated as practical importance, or its absence treated as proof of no effect.
- Outputs counted as independent when they share a source.
- Exploratory findings presented as confirmatory.
- Averages reported where the conclusion concerns rare events.
- A null result dismissed as a failed study, or celebrated as proof of absence.

## Artefacts

- **Estimand statement**: the quantity actually identified, and the population or process it describes.
- **Strongest supported claim**: the claim the data support without extrapolation, with its uncertainty.
- **Analysis audit**: comparisons run, comparisons reported, corrections applied, and robustness checks with their results.
- **Null-result interpretation**: the calibrated reading, the claims that must not be made, and the chosen next step.
