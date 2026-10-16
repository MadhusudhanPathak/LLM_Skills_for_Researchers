# The arc

The arc is the default order of stages in a session. It carries much of the method's expertise: criticism of a claim that has not been clarified attacks a version the researcher may not hold, and pressure applied before the position has been reconstructed and steelmanned invites a defensive reply. Each category skill describes what every stage means for its kind of research and which moves it draws on; this file defines the stages themselves.

## The seven stages

### 1. Clarify

Establish the central claim, the terms it depends on, its intended scope, and what kind of claim it is.

- Run `claim-sorting.md` on the material if the intake has not already done so in full.
- Pin down load-bearing terms: what they mean here, what they exclude, and which neighbouring terms they must be distinguished from.
- Fix quantifiers, modality and scope. A counterexample to a vague claim is a counterexample to nothing.
- Establish what the researcher would count as success: what a satisfactory answer, result or defence would look like.

**Exit when** the central claim can be stated in one sentence that the researcher accepts, with its key terms defined well enough to test.

### 2. Reconstruct

Lay out the structure of the work explicitly and get the researcher's confirmation.

- For an argument: numbered premises and conclusions, with stated and supplied premises marked.
- For a model or theory: its components, mechanism, assumptions and the phenomena it explains.
- For a design, specification or system: its requirements, components, interfaces and the properties claimed for it.
- For a study: the question, hypotheses, design, measures, analysis and the inference from results to conclusion.

Before moving on, **steelman** it: state the strongest version an informed proponent would recognise, and ask whether it is accurate. Every later stage examines the steelmanned version, not a weaker one.

Mark everything Claude supplies as a reconstruction, never as something the researcher said. Where several reconstructions fit the material equally well, present them and let the researcher choose.

**Exit when** the researcher has confirmed a reconstruction and a steelman.

### 3. Surface assumptions

Find what the work takes for granted: conceptual, metaphysical, epistemic, normative, methodological, empirical, technical and scope assumptions, and the bridge premises that connect one step to the next.

- Separate unavoidable starting points from contestable assumptions that carry weight.
- Rank assumptions by how much the conclusion depends on them and how contestable they are.

**Exit when** the load-bearing assumptions are listed and ranked, and the researcher agrees the list is complete enough to proceed.

### 4. Test reasons, evidence and inferential links

Examine whether the support offered is sufficient and whether each step follows.

- For each load-bearing premise or claim: what supports it, how strongly, and under what assumptions.
- For each inferential step: what licenses it, what kind of inference it is, and whether the conclusion is stronger, broader or more certain than the support allows.
- For empirical and technical work: whether the design, measures, analysis, proof or tests support the stated conclusion.

**Exit when** each load-bearing link has been examined and classified (see the problem classes in `contradictions.md`).

### 5. Trace implications, boundary cases and costs

Follow the position outwards.

- What follows if the claim is true? What else must then be true?
- Where are its boundaries: the cases, settings or conditions at which it stops holding?
- What does it cost: what must be given up, what becomes harder to explain, which commitments it creates elsewhere?
- What follows in practice, if anything?

**Exit when** the scope of the claim is mapped and its main costs are visible.

### 6. Counterexamples, rival interpretations and opposing perspectives

Apply the strongest pressure last, immediately before revision.

- Test the claim against counterexamples drawn from the families in `counterexamples-and-modal.md`.
- Bring the strongest rival account, explanation or reading, and compare on common criteria (`steelman-and-rivals.md`).
- Take the perspective of the opponent, the sceptical examiner, the reviewer in another subfield, the practitioner or the affected party.

Pursue one or two serious challenges through reply and counter-reply rather than listing many shallow ones.

**Exit when** the strongest available challenge has been put and answered, conceded, or recorded as open.

### 7. Revise and retest

Invite the researcher to revise the position in light of the session, then test the revision.

- Ask what they would now narrow, qualify, add, drop or replace.
- Test the revision: does it answer the problem that prompted it without creating a new one, and is it principled rather than tailored to one case?
- Record every revision in the revision log.

**Exit when** the researcher has a revised position they are willing to defend, or has located precisely what remains underdetermined.

## Moving through the arc

- **Return to earlier stages when an answer requires it.** A revision in stage 7 often needs a new round of clarification. A counterexample in stage 6 may reveal an assumption missed in stage 3.
- **Compress when the work is already precise.** A researcher who arrives with a confirmed reconstruction and defined terms may need only one confirming round for stages 1 and 2.
- **With long material, start where the weight is.** For a chapter or a full paper, do not work through it in sequence. Identify the claim the rest depends on, and run the arc on that claim first.
- **Stages are not rounds.** A stage may take one round or four. The category skill and the depth setting decide the allocation.

## Allocating rounds by depth

Typical allocations. Each category skill adjusts these to where its kind of research usually fails.

| Stage | Light (3-5) | Standard (6-9) | Deep (10-15) |
|---|---|---|---|
| 1. Clarify | 1 (combined with 2) | 1 | 1-2 |
| 2. Reconstruct | (combined with 1) | 1 | 1-2 |
| 3. Assumptions | 1 | 1 | 2 |
| 4. Reasons and evidence | 1 | 1-2 | 2-3 |
| 5. Implications | (folded into 6) | 1 | 1-2 |
| 6. Counterexamples and rivals | 1 | 1-2 | 2 |
| 7. Revise and retest | 0-1 | 1 | 1-2 |

## The research question is not a default stage

Examining whether the research question itself is well formed is not part of the arc. The arc examines the work as it stands. Use `research-question-and-feasibility.md` only when:

- the intake shows the question is unsettled, shifting or contested;
- the researcher asks whether they are asking the right question;
- a stage keeps failing in a way that traces back to the question rather than the answer.

When it is needed, run it as one or two rounds before stage 1 or after stage 7, and say why.
