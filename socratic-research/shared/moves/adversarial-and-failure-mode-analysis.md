# Adversarial and failure-mode analysis

Use this move to stress-test a design, system, protocol, policy, intervention or argument against the ways it could fail: by accident, under pressure, through interaction between parts, or because someone is actively trying to break or exploit it. The question is not whether the thing works in the expected case, but how it fails, how badly, and whether anyone would notice.

## Use when

- A system, method, protocol, safeguard or policy is proposed.
- A claim of reliability, safety, security or robustness is made.
- The work assumes a cooperative or non-strategic environment.
- The researcher needs a pre-mortem before committing.

## 1. The adversary or stressor

Name what the thing must withstand:

- **accidental failure**: faults, errors, noise, wear, unexpected inputs, misuse by well-meaning users;
- **environmental stress**: load, scale, distribution shift, resource exhaustion, failure of dependencies;
- **a motivated adversary**: someone or something trying to cause harm, extract value, evade detection, or game the system.

For an adversary, ask:

- What are their goals, knowledge, access, resources, persistence and tolerance for being detected?
- Are insiders in scope? Third-party components? The supply chain?
- What does the adversary know about the defence?

For an argument, the adversary is the most capable critic: what would they target first?

## 2. Walking a failure path

- Walk one complete path from initial cause or intent to the harmful outcome. What has to happen at each step?
- Where on that path could the failure be prevented, detected or contained?
- Now add complications: failures that combine, steps spread over time that are each harmless alone, several actors coordinating, the adversary adapting to the defence, the monitoring budget running out.

## 3. Independence and common causes

- Are the layers of defence genuinely independent, or do they share an assumption, a component, a data source, or a blind spot?
- If one layer fails, does that make the next more likely to fail?
- Is there a single point of failure?

## 4. How it fails

- Does the system fail loudly (detectably) or silently?
- Does it fail safe (into a harmless state) or fail open?
- Can it recover? How long does recovery take, and what is lost?
- Which failures are reversible and which are not?

## 5. Adaptation and incentives

- Does the defence block known attacks only, or does it raise the cost of attacks that adapt to it?
- What incentives does the design create for the people operating it? Would false alarms, delays or costs lead them to bypass it?
- Does the design depend on the adversary or environment being non-strategic, transparent or stable?

## 6. Pre-mortem

Imagine it is some time after deployment, publication or adoption, and the work has failed badly. What is the most likely story of how that happened? What is the most damaging story?

## 7. Red-teaming plans

When the researcher plans to test the thing adversarially:

- Is the aim to discover vulnerabilities, estimate how common they are, validate a defence, or provide assurance? Does the design fit that aim?
- Who are the testers, what expertise and access do they have, and are they constrained by the same assumptions as the designers?
- How are unsuccessful attempts recorded?
- What justifies treating "nothing found" as evidence? What search would have found something if it were there?
- How will findings be reproduced, triaged, fixed and retested? How will hazardous findings be disclosed?

## Watch for

- Testing against a conveniently weak adversary.
- "No failures observed" presented as evidence of safety without a model of the search.
- Average-case performance presented where worst-case behaviour matters.
- Defences evaluated only against attacks their designers thought of.
- Detailed elaboration of genuinely hazardous attack methods beyond what the analysis needs.

## Artefacts

- **Failure-mode table**: each failure mode with its cause, severity, likelihood, detectability, current mitigation, and residual risk.
- **Minimal assumption set**: the smallest set of assumptions on which the success or safety of the design depends.
- **Stop conditions**: the observations that should halt deployment or use.
- **Assurance statement**: the exact claim a red-team exercise or stress test can support, and no more.
