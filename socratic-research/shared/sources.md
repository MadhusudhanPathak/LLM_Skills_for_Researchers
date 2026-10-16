# Sources behind these skills

Read this file only if the researcher asks where a practice in the skills comes from, or wants to cite the reasoning behind it. It records what each source contributed and which sources could not be read. Verify any source-specific claim against the original before citing it in academic work.

## Sources read and used

**Ramin Saadat, *When Questioning Entrenches Ignorance: Rereading the Socratic Method through Ignorance Studies for Today's World*, working paper, British Institute for Ignorance Studies (date not confirmed).** https://biis.uk/wp-content/uploads/2026/08/When-Questioning-Entrenches-Ignorance.pdf
Argues that the *elenchus* works against simple ignorance (*agnoia*) but can entrench complex ignorance (*amathia*) when conducted before an audience, through public accountability, normative pressure, face-threat and motivated reasoning. Reads Euthyphro, Laches and Meno as defensive exits. Suggests success be judged by movement from *amathia* towards *agnoia*, and that private settings, possibly including unobserved conversations with AI, may be less prone to the effect; the author flags the AI point as untested. The paper states its own limits: three dialogues as case studies, and laboratory findings that may not transfer. Used for: the success criterion, `dialogue-safety.md`, and defensive-exit handling.

**Kien Pham Thi (2025), "Socratic philosophy: Dialectics, ethics, and enduring influence", *Futurity Philosophy* 4(2), 21-46.** https://doi.org/10.57125/FP.2025.06.30.02
A qualitative overview of the Socratic method, Socratic epistemology and ethics, the "Socratic problem", and Socrates' influence. Describes the method in four steps (unsettling what seems obvious and exposing contradiction; *maieutics*, the questioner as midwife; induction from particular cases; definition), with the Euthyphro as its example. Reports Popper's objection that the method can produce endless argument without a conclusion, and notes that its slow pace can frustrate people who want answers and that it suits abstract fields better than technical ones where direct instruction often works better. Used for: answering factual requests directly rather than withholding them; ending every session in a concrete audit and task list rather than open-ended argument. The paper's broader conclusions are asserted more strongly than its method supports, and some reference-list entries appear mismatched to the claims they support; treat it as orientation.

**Wikipedia, "Socratic method".** https://en.wikipedia.org/wiki/Socratic_method
Vlastos's five-step standard *elenchus*; Frede's objection that refuting a thesis does not establish its negation; *aporia* as the usual outcome; *maieutics*; warnings about shame and humiliation. Used for: `contradictions.md`. Treat as orientation; cite the primary scholarship in academic work.

**B. Barry Mahoney, Ron Oostdam, Hessel Nieuwelink and Jaap Schuitema (2023), "Learning to think critically through Socratic dialogue: Evaluating a series of lessons designed for secondary vocational education", *Thinking Skills and Creativity* 50, 101422.** Open repository copy: https://pure.hva.nl/ws/files/45266305/1-s2.0-S1871187123001906-main.pdf
Design study with five teachers and 85 students. Component skills of claiming, arguing and questioning; part-task practice helped. Teachers found guiding dialogue impartially demanding and slipped into explaining; students felt they had to attack or defend statements, or stayed overly friendly to avoid criticising. Small sample, self-report measures, learning effects not measured. Used for: the attack-and-defence risk, and the case for explicit structure in each round.

**Adam John, "Socratic Questioning: The 6 Types (With Examples) Explained".** https://criticalthinkingexercisez.com/socratic-questioning/
The six-type taxonomy (clarifying, assumptions, reasons and evidence, viewpoints, implications, questions about the question), a clarify-first sequence, and pitfalls: hostile tone, running a script, yes-or-no questions, rushing, applying the method only to others. Used for: question labels, the arc, adaptive theme choice, self-scrutiny.

**University of Connecticut CETL, "Socratic Questions".** https://cetl.uconn.edu/resources/teaching-your-course/leading-effective-discussions/socratic-questions/
The same six categories with examples; follow up on answers rather than moving on; summarise key points periodically. Used for: the summary at the start of each round, and checkpoints.

**Colorado State University TILT, "The Socratic Method: Fostering Critical Thinking".** https://tilt.colostate.edu/the-socratic-method/
Probing questions about underlying beliefs and values; best for exposing complexity and uncertainty; the questioner is neither opponent nor habitual devil's advocate; productive discomfort rather than intimidation. Used for: "not devil's advocacy by default" and the discomfort distinction.

**University of Chicago Law School, "The Socratic Method".** https://www.law.uchicago.edu/socratic-method
Cooperative questioning to reach the core of a problem; not constant interrogation or intimidation; accepting uncertainty and revising views as skills in themselves. Used for: treating revision as progress.

**EBSCO Research Starters, "Dialectics / Dialectical Method".** https://www.ebsco.com/research-starters/religion-and-philosophy/dialectics-dialectical-method/
Dialectic as two participants aiming to understand each other rather than win; admitting contradiction is not shameful. Used for: the dialogue framing.

**"Smarter Thinking: The Socratic Method" (blog).** https://blog.hptbydts.com/smarter-thinking-the-socratic-method
Hypothesis, examination, response cycle; moves such as instances, counterexample, parallel case and analogy; limitations including dependence on the questioner's skill and misuse to seed doubt. Used for: the theme-choice table and the caution against devil's advocacy.

**The Right Questions, "How to Progress from Debate to Dialogue Using the Socratic Method".** https://therightquestions.co/how-to-progress-from-debate-to-dialogue-using-the-socratic-method/
Receive, reflect, refine, re-state, repeat; "what makes you think that?" in place of "why?". Used for: summarising before questioning, and the revise-and-retest stage.

**SK Ellis, "Socratic Questions".** https://www.skellis.net/blog/socratic-questions
A list of the six categories credited to the UConn resource. Confirms the taxonomy.

**LudensFlow, "Socratic Questions".** https://www.ludensflow.com/en/blog/socratic-questions
Ask about the word, not the person; "what led you to that" rather than "why did you"; make the case concrete before going abstract; watch power dynamics. Used for: `dialogue-safety.md`.

## Sources that could not be read

- **Philosophy Stack Exchange, "Is there an issue with the Socratic method arguing against points?"** (https://philosophy.stackexchange.com/questions/72805): access refused to automated fetching. Not used.
- **SecEd, "A questioning classroom: 38 Socratic questions for your teaching"**: only the introduction is public. Not used beyond confirming its general recommendation of open questions.
- **Eva Keiffenheim, "A step-by-step guide to master the Socratic method for better thinking"** (Medium): only the introduction was retrievable. Not used.

## Prompt libraries supplied by the project author

Four prompt banks (reusable Socratic prompts for philosophical research, for technical AI safety research, a set of fifty example prompts, and a sixty-prompt research library) supplied most of the research moves, question stems and audit structures in `shared/moves/` and `shared/process/`. Two earlier skills by the same author, `idea-refine` and `socratic-method`, supplied the three-tier assumption audit, prior-work labels, feasibility checks, the contradictions procedure, dialogue-safety practices and writing-style rules. The prompt banks' own reference lists cite further sources (for example the Foundation for Critical Thinking, Google's model evaluation guidance, CSET's evaluations explainer, and arXiv work on evaluation awareness and benchmark trust) that were not independently checked for these skills.

The design decisions that turned this material into the present skills (themed rounds of four or five questions, summaries after every round, inferred and confirmed depth, the seven-stage arc, five research categories built on shared modules) were made by the project author and are recorded in the repository's `Skill_Design.md`.
