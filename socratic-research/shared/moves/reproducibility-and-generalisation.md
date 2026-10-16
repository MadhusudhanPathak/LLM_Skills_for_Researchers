# Reproducibility and generalisation

Use this move to ask whether a result could be obtained again, by someone else, and whether it holds beyond the setting in which it was obtained. These are separate questions: a result can be perfectly reproducible and still not generalise.

## Use when

- A result, proof, artefact or finding is reported and others will rely on it.
- The conclusion extends from the tested setting to a wider one.
- The work uses a simplified setting (a toy model, a laboratory task, a pilot, a simulation, one case) to support a claim about realistic ones.
- The deployment, application or target setting differs from the one studied.

## Part 1: reproducibility

### Levels

| Level | Question |
|---|---|
| Computational reproducibility | With the same data and code, does one get the same numbers? |
| Direct replication | With the same procedure and new data, does one get the same result? |
| Conceptual replication | With a different procedure testing the same claim, does one get the same result? |
| External validation | Does the result hold in a different population, setting or system? |

Ask which level the researcher is aiming for, and which the evidence reaches.

### What another researcher would need

- data, materials, texts, instruments or stimuli;
- code, environments, dependencies and their versions;
- configurations, parameters, random seeds, prompts, settings;
- the exact procedure, including filtering, exclusion and cleaning rules;
- analysis decisions, including those tried and abandoned;
- hardware or equipment details where they matter.

Stems:

- Which undocumented choice could change the result most?
- Could someone reconstruct the analysis from the write-up alone?
- What cannot be shared (privacy, licensing, security, access), and what substitute evidence keeps the work checkable?
- What would count as a failure to replicate, and would such a failure be informative?

## Part 2: generalisation

### Map the differences

List every dimension along which the tested setting and the target setting differ. Depending on the field, these may include: population, sample, materials, task, language, culture, period, scale, complexity, capability, incentives, environment, tools, observability, institution, time horizon.

- Which mechanism must stay the same across those differences for the result to transfer? What supports that?
- Which differences are most likely to matter?

### What kind of evidence is this

- Is the result an existence proof (it can happen), a mechanism demonstration (here is how), a performance result (it scored this on this test), or evidence about the target setting itself?
- Which kinds of claim can each support?

### Shift

- What kinds of shift are likely between the studied and target settings: in the inputs, in the relationship between inputs and outcomes, in the meaning of the categories, in the population, over time, or in response to the result itself (people or systems adapting to it)?
- Does average performance stay stable while rare severe failures increase?
- Can the method detect when it is outside the range in which it was validated?

### Reversal

- Describe a scenario in which the result reverses, disappears, or becomes unmeasurable in the target setting.
- How plausible is that scenario? What would show whether it is happening?

## The generalisation ladder

Build a ladder from the narrowest claim to the broadest:

1. true of these observations;
2. true of this sample or these runs;
3. true of this population, system or setting;
4. true of a wider class;
5. true in the target setting;
6. implications for practice or policy.

For each rung, state the evidence or bridge study needed to reach it, and mark the highest rung the current evidence reaches.

## Watch for

- A toy or laboratory result described in the language of the target setting.
- Generalisation assumed because nothing suggested it fails.
- A single replication treated as settling the matter, in either direction.
- Reproducibility claims based on code that has only ever run on one machine.

## Artefacts

- **Reproducibility checklist**: what is shared, what is not, the substitute evidence for what cannot be shared, and the most consequential undocumented choice.
- **Replication design**: the replication that would test the least-tested assumption, and what its failure would mean.
- **Generalisation ladder**: rungs, bridge evidence for each, and the highest rung reached.
- **Shift map**: the expected differences between tested and target settings, and the monitoring that would detect each.
