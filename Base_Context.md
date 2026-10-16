# Base context

This document records what the project started from. Everything described here now lives in `Older_Context/`. It is written so that someone who never saw those files can understand what they contained, what was good in them, what was wrong with them, and which parts carried forward into the new skills described in `Skill_Design.md`.

## 1. What the starting material was

The original folder held three kinds of material:

1. **Four prompt libraries** written as copy-and-paste templates for a general-purpose LLM chat. Between them they hold roughly 190 prompts for Socratic examination of research.
2. **One academic paper** on Socratic philosophy, used as a background source.
3. **Two finished Claude skills**, each packaged as a Claude Code plugin: `idea-refine` and `socratic-method`. Both were labelled "v2", which suggests at least one earlier round of iteration that is not preserved here.

The prompt libraries came first. The `socratic-method` skill was built by distilling them, and its `sources.md` file says so directly: the four libraries "supplied most of the research moves and question stems" in the skill's reference files. The libraries were never removed after that distillation, so the folder held the same ideas at two levels of refinement with no link between them.

All of it was written for one researcher's programme: work that moves between philosophy and technical AI safety, with a particular focus on corrigibility, control, agency, deceptive alignment, interpretability and evaluation. That focus shaped almost every example and many of the structural choices.

## 2. The four prompt libraries

### 2.1 Reusable Socratic Prompts for Philosophical Research

Thirty-two templates, grouped into full inquiry prompts (an extended examination, a supervisor-style dialogue, research-question interrogation), conceptual analysis (concept clarification, necessary and sufficient conditions, ambiguity audits, a counterexample laboratory, conceptual engineering), argument diagnosis (reconstruction, validity and soundness, hidden assumptions, inferential gaps, minimal inconsistent sets, objection-and-reply ladders, steelmanning, rival theories), epistemic scrutiny (evidence audits, intuition audits, thought experiments, falsification conditions, an "ignorance and identity safeguard"), literature and contribution (positioning, source fidelity, novelty, gap claims), the bridge from philosophy to empirical work (operationalisation, concept-to-hypothesis, experimental stress tests, behaviour versus mechanism, toy-model generalisation), and impact planning (theory of change, a viva stress test).

It opens with a short methodological preamble that turned out to be the most durable part of the whole folder. It names six families of Socratic question (clarification, assumptions, reasons and evidence, perspectives, implications, questions about the question), describes the elenctic cycle, and makes two points that every later document repeats:

- A contradiction among commitments shows that they cannot all hold. It does not show which one is false, and refuting a thesis does not establish its negation.
- Questioning can entrench belief rather than revise it when the person feels attacked, so the questioner should be private, non-humiliating and non-leading, and should treat well-located uncertainty (*aporia*) as a legitimate result.

It also set out a list of default dialogue rules (one main question at a time, build on the last answer, clarify before criticising, label each question, do not answer on the researcher's behalf, no disguised advice or rhetorical questions, no invented sources, separate supplied material from inference, minimal inconsistent sets, steelman before pressure, permit uncertainty, end with an audit). This list became the target of the user's first round of detailed feedback, described in `Skill_Design.md`.

Its first prompt, "Extended Socratic examination", is the closest thing in the folder to a complete method. It gives an eight-stage order (clarify, reconstruct, surface assumptions, test reasons and evidence, introduce counterexamples and rival views, trace implications, question whether the research question is well formed, revise and retest), a set of question labels, an instruction to steelman first, the inconsistency procedure, and an end-of-session output. The other thirty-one prompts are narrower versions of single stages of this one.

### 2.2 Reusable Socratic Prompts for Technical AI Safety Research

Thirty templates with the same overall shape, tuned to empirical and engineering work: research formulation (a full examination, research-question stress tests, problem-importance audits, hypothesis generation), concepts and measurement (operationalising a safety property, proxy validity, behaviour-mechanism separation, definition-to-implementation audits), experimental design (design interrogation, baselines and controls, confounders, statistics, null results, reproducibility), evaluations and benchmarks (benchmark design, evaluation validity, evaluation awareness and sandbagging, elicitation versus capability), alignment and control (corrigibility, control protocols, deceptive alignment, scalable oversight, agentic systems), interpretability, robustness and security (interpretability claims, distribution shift, threat models, red-team design), and results and direction (results-to-claims, paper review, research agenda).

Its general operating rules extend the philosophical list with technical labels (DESIGN, MEASUREMENT, ALTERNATIVE EXPLANATION, GENERALISATION, SECURITY) and add standing cautions: benchmark performance is not safety, failure to elicit a behaviour is not evidence of its absence, a toy result is evidence about the toy, and more capable systems may conceal or adapt to tests.

Most of this library is general research methodology wearing AI-safety clothing. Proxy validity, confounders, effective sample size, null-result interpretation, reproducibility levels, generalisation from a simplified setting, and the observer effect all apply in any empirical field. A smaller part (corrigibility, control protocols, scheming, scalable oversight) is genuinely specific to AI safety.

### 2.3 Socratic reasoning example prompts

Fifty short prompts, each in the form "Act as a [rigorous/skeptical/adversarial] Socratic interlocutor... Review my [X]... Ask questions that expose...". Half target technical AI safety (definitions, assumptions about control, evaluation methods, logical consistency of alignment proposals, interpretability and deceptive alignment); half target philosophy (epistemology, philosophy of mind and agency, normative ethics, metaphysics, dialectical method).

This file is the weakest of the four as a basis for a skill, and it is useful to say why. Its preamble instructs the model to adopt "a strictly adversarial yet constructive stance", to "refuse surface-level agreement" and to "force" the user to defend positions. That framing contradicts the cautions in the other three libraries, which warn that adversarial questioning produces defence rather than revision. Its prompts are also topic-indexed rather than move-indexed: each one names a subject (Twin Earth, the orthogonality thesis, wireheading) rather than a reusable reasoning move, so they do not transfer to other fields. Its value is as a list of topics and failure modes a researcher in this area might want examined, not as method.

### 2.4 Socratic Research Prompt Library (sixty prompts)

The longest and most even-handed of the four. Sixty prompts in nine parts: core Socratic analysis; concepts, definitions and conceptual engineering; counterexamples, thought experiments and modal reasoning; steelmanning, objections and dialectical fairness; evidence, epistemology and literature research; AI alignment, corrigibility, control and agency; research design, formalisation and empirical stress-testing; meta-level reflection and research integrity; and ten short prompts for single research moves ("find the single weakest link", "ask for the missing premise", "what would change the conclusion").

Several prompts here appear nowhere else and proved important later:

- distinguishing a genuine objection from a merely possible one, and testing whether an objection is relevant to the claim at all;
- asking whether a concept does explanatory work or only relabels a pattern;
- formalising an informal claim without hiding its assumptions, and remembering that formal notation is not evidence;
- examining epistemic standards and burdens of proof, and separating confidence from practical decision thresholds;
- prioritising candidate research questions by expected value, and converting open uncertainty into a staged research agenda;
- checking whether questioning itself has become adversarial or unproductive;
- avoiding the inference from a failed theory to the truth of a rival;
- asking the model to audit its own previous analysis.

Its closing workflow maps prompts to research stages and offers a "useful research cycle": clarify, reconstruct, expose assumptions, test reasons and evidence, consider alternatives, derive implications, identify revisions, specify what would resolve the remaining uncertainty. Its practical safeguards (supply source text, require evidence discipline, avoid one-sided prompting, do not reward endless scepticism, separate conceptual from empirical questions, preserve uncertainty, keep an audit trail) are general and carried forward almost unchanged.

### 2.5 What the four libraries share, and where they overlap

Read together, the libraries repeat themselves heavily. Concept clarification, assumption excavation, counterexamples, steelmanning, evidence audits, operationalisation, behaviour versus mechanism, and results-to-claims each appear in three or four of the files with different wording. They also share a single theory of good questioning: clarify before criticising, steelman before pressing, follow the answer rather than a checklist, keep inconsistency diagnosis honest, never invent sources, separate what was supplied from what was inferred, and end with an audit that converts open questions into tasks.

The duplication is the clearest sign of fragmentation. There was no single place where a reusable move was defined once.

## 3. The background paper

`FP_Pham+Thi,+K.+(2025).pdf` is Kien Pham Thi, "Socratic philosophy: Dialectics, ethics, and enduring influence", *Futurity Philosophy* 4(2), 21-46, 2025 (doi:10.57125/FP.2025.06.30.02). It is the article that the old skill's `sources.md` recorded as unreadable because the journal page returned an error; the local copy makes it available.

The paper is a qualitative, interpretive overview based on Plato's and Xenophon's accounts. It covers the Socratic method, Socratic epistemology (knowledge as self-knowledge, "I know that I know nothing"), virtue ethics ("virtue is knowledge"), the "Socratic problem" of separating the historical Socrates from his literary portraits, Socrates' relation to religion, his place in literature and art, comparisons with Confucius and Nagarjuna, and his influence on Western philosophy and education.

The parts relevant to skill design are few but useful:

- It describes the method in four steps: an opening move that unsettles what the interlocutor takes as obvious and exposes a contradiction; *maieutics*, the questioner as midwife who helps the other person produce the idea rather than supplying it; induction from particular cases to a general feature; and finally definition. The Euthyphro exchange ("is it pious because the gods love it, or do they love it because it is pious?") is its worked example.
- It reports criticisms that matter for an LLM implementation. Popper is cited for the objection that the method can produce endless argument without a conclusion. The paper's own discussion notes that the slow, reflective pace can frustrate people who want answers, and that the method suits abstract fields better than technical ones such as mathematics, where direct instruction often works better.
- It notes that Socrates' refusal to give firm definitions of justice or morality is read by some scholars as a deliberate spur to inquiry and by others as a weakness.

The paper should be cited with care. Its conclusions about cross-cultural reach and digital education are asserted more strongly than its method (a narrative literature survey without systematic search) can support, and some entries in its reference list look mismatched to the claims they are attached to. It is a reasonable orientation to the classical method, not an authority on Socratic questioning as a research tool.

## 4. The two existing skills

### 4.1 idea-refine (v2)

A Claude skill for turning one rough research idea into a defensible plan. It routes the request first (rough idea, several candidate directions, a settled plan to attack, or no idea yet) and enters a three-phase process at the matching point:

1. **Sharpen and widen.** Restate the idea as an answerable research question with every term operationalised; ask only the questions whose answers would change the recommendation (output and deadline, who judges it, resources, what counts as success and what a null result would mean, what has been tried); generate three to six variations that differ in mechanism, using "lenses" chosen by symptom (operationalise, swap the method, narrow the claim, invert the hypothesis, find the observable consequence, generalise, replicate and extend, change the unit of analysis, find the minimum version).
2. **Stress-test and converge.** Apply five tests to at most three directions: contribution, feasibility against the deadline, prior work, validity threats, and an assumption audit in three tiers (dealbreaker, important, secondary). Report only the tests that bite, then give an honest recommendation.
3. **The one-pager.** Research question, recommended direction, contribution claim, assumptions ranked by risk, minimum viable study, prior-work status, a Not Doing list, and questions for the supervisor.

Its NEVER list is sharp and specific: no invented citations, no novelty claims without a search, no invented figures without stated assumptions, no padded variations, no scoping to the most interesting version when a deadline binds, no skipping the null-result question.

This skill was already close to domain-general. It covers dissertations, papers, philosophy essays and grant proposals, and its lenses include a section for conceptual work. Its examples happen to come from AI safety and philosophy of AI, but the method does not depend on them.

Two of its ideas carried forward into the new design: the three-tier assumption audit, and the prior-work labels ("close prior work found", "related work found, gap is X", "no prior work found in N searches", "not checked"). Its feasibility test (count backwards from the deadline, find the critical path, separate known-hard from novel-hard steps) also became part of a new shared module.

### 4.2 socratic-method (v2)

A Claude skill that runs an in-depth Socratic examination of a research claim, argument, draft, definition, hypothesis, study design or result. It is the most developed artefact in the folder and the direct ancestor of the new skills.

Its structure:

- **Three fixed modes.** Philosophical, technical AI safety, or both. The session starts by asking which, because each mode applies a different standard of support: argument for philosophy, evidence for technical claims, both plus a bridge argument for combined work.
- **A four-part turn.** Take stock of the last answer; ask one labelled principal question with a sentence on why it matters; offer two to four open "think-with" prompts as routes into the question; stop. Turns are capped at about 120 words.
- **A default arc.** Clarify, reconstruct, steelman, surface assumptions, test inferences and evidence, counterexamples and rivals, implications and scope, question the question, revise and retest.
- **An adaptive response table.** What to do when an answer is vague, too broad, confident without support, strong, weak, quickly agreed, "I don't know", contradictory, defensive, repetitive, a request for Claude's view, or a request for facts. The last two depart from the tutoring tradition on purpose: a researcher who asks what the literature says should be told.
- **Contradictions done properly.** State the smallest inconsistent set with modality and scope preserved, ask which member to revise, never decide on the researcher's behalf, never treat the failure of one thesis as support for a rival. Problems are classified as fatal, repairable, scope-limiting, needs clarification, needs evidence, or presentational.
- **Keeping it a dialogue.** Drawing on Ramin Saadat's working paper on questioning that entrenches ignorance, and on classroom studies of Socratic dialogue, it sets rules for avoiding attack-and-defence dynamics: question the claim not the person, no devil's advocacy by default, treat revision as progress, hold rival views to the same standard, and stop pressing after a defensive exit. Its success criterion is movement from *amathia* (thinking one knows) towards *agnoia* (knowing that one does not), plus a plan.
- **A NEVER list** aimed at the ways an LLM fails at this: capitulating to repetition, answering its own question, praise, firing lists of objections, running reference stems as a checklist, declaring refutation from inconsistency, pressing after a defensive exit, filling literature gaps from memory.
- **Writing style rules** (plain formal UK English, no em dashes, no inflated vocabulary) justified by the fact that researchers lift phrasing from memos into their own drafts.
- **Checkpoints, audits and variants.** A ledger every five questions or so; mode-specific end-of-session audits with origin tags (`[supplied]`, `[researcher]`, `[Claude]`, `[open]`); a written-memo alternative; supervision, viva and reviewer variants.

Its reference files hold the content: `philosophy.md` (19 research moves), `technical-ai-safety.md` (24 moves, about a third of them specific to AI safety), `combined.md` (the bridge between concept and experiment, organised around a research cycle of problem, analysis, operational definition, hypothesis, implementation, stress test and revision), `audit-templates.md`, and `sources.md` (an honest record of each source read, what it contributed, and which sources could not be read).

The design quality here is high. The problem is scope. The two subject modes cover philosophy and technical AI safety and nothing else. A historian, an economist, a clinical researcher or a materials scientist has no mode that fits, and the technical mode in particular mixes general method with AI-specific threat models in a way that cannot be separated without rewriting it.

## 5. Problems the starting material had

Taken together, the starting material had five problems that the new design set out to fix.

1. **Fragmentation.** The same research moves were written out three or four times across the prompt libraries and again in the skill's reference files. There was no single canonical definition of any move, so improving one meant finding and editing all of its copies.
2. **Narrow scope.** Both the libraries and the `socratic-method` skill were organised around one research programme. Categories of research that are common elsewhere (theoretical model-building, conceptual and taxonomic work outside philosophy, engineering and formal work outside AI, qualitative and observational empirical work) had no home.
3. **Topic-indexing instead of move-indexing.** Much of the material, especially the fifty example prompts, is organised by subject ("my definition of a treacherous turn") rather than by reasoning move ("test a definition against borderline cases"). Subject-indexed prompts do not transfer.
4. **Inconsistent stance on adversarial questioning.** Three files warn against adversarial pressure; one instructs the model to adopt it. A merged skill had to pick one, and the evidence collected in the old `sources.md` favours the collaborative stance.
5. **Interaction mechanics that ask too much of the model.** Several rules depend on the model judging subtle features of its own phrasing: whether a question is "leading", whether advice is "disguised", whether it has implicitly answered on the researcher's behalf. The user's view, recorded in `Skill_Design.md`, is that models do not apply such rules reliably, and that one-question turns are both hard to write well and too narrow to approach a concern from several angles.

## 6. What carried forward

The new skills keep most of the substance and change the structure. In summary:

| From | Kept | Changed or dropped |
|---|---|---|
| Philosophical prompt bank | The extended examination as the backbone of every session; the six question families; the inconsistency procedure; steelman before pressure; the closing audit with origin tags | One question per turn replaced by a themed round of four or five questions; two judgement-heavy rules removed; fixed turn count replaced by inferred depth; stage order revised; "question the research question" removed from the default arc |
| Technical prompt bank | Proxy validity, behaviour versus mechanism, definition-to-implementation, design, confounders, statistics, null results, reproducibility, generalisation, results-to-claims, threat modelling, research agenda | Rewritten domain-neutral. Evaluation awareness generalised to reactivity and observer effects; security threat models generalised to adversarial and failure-mode analysis; corrigibility, control protocols, scheming and scalable oversight left out of the shared modules |
| Fifty example prompts | A list of failure modes worth probing | The adversarial framing; the topic-indexed structure |
| Sixty-prompt library | Objection relevance, explanatory work of concepts, formalisation, burdens of proof, research prioritisation, refutation versus positive theory, Claude's self-audit, the practical safeguards | Absorbed into shared move modules rather than kept as standalone prompts |
| Background paper | The four-step description of the method; the warnings about endless argument and slow pace | Used as context only |
| idea-refine | Three-tier assumption audit; prior-work labels; feasibility against deadline | The skill itself is not part of the new set |
| socratic-method | Response table, contradictions procedure, dialogue-safety practices, NEVER list, writing style, checkpoints, audits, variants, evidence-integrity rules, `sources.md` record | Three fixed modes replaced by five research categories built on shared modules; think-with prompts replaced by the themed question round |

`Skill_Design.md` records how and why each of these decisions was made.
