# Intake

Every session starts here. The intake gathers the material and its context, checks that the invoked category fits, and agrees the depth of the session with the researcher before any substantive questioning begins.

The intake has three steps:

1. **The intake request** (one message): ask for everything the session needs.
2. **The intake summary** (one message, after the researcher replies): restate what arrived, sort the claims, check the category fit, and propose a plan with an estimated number of rounds.
3. **Confirmation**: the researcher accepts or adjusts the plan, and round 1 begins.

If the researcher supplied most of the intake in the request that invoked the skill, skip straight to whatever is missing and combine steps 1 and 2. If the researcher says "just start", state the assumptions you are making in place of the missing fields, give the plan, and begin round 1 in the same message.

## Step 1: the intake request

Open with one or two sentences saying what the session will do (a round-by-round Socratic examination of their work in this category, ending in an audit and a list of research tasks). Then ask for the fields below in a single message. Tell the researcher that rough material is welcome, that they can paste or attach files, and that they can skip anything that does not apply.

### The fields

1. **The material to examine.** The claim, thesis, argument, definition, framework, model, design, specification, proof, protocol, results or draft that the session should examine. Ask for the actual text or artefact, not a description of it.

2. **All the work already done.** Everything behind the material, however rough:
   - notes, outlines, mind maps, earlier drafts and abandoned versions;
   - the set-up already in place: data, corpora, texts, code, environments, instruments, models, equipment, participant pools, access agreements;
   - analyses, derivations, pilot results or partial findings;
   - feedback already received from supervisors, colleagues, reviewers or examiners;
   - what has been read, what has been tried, and what has been ruled out and why.

   Each category skill lists the specific kinds of prior work most useful for its research. Add that list here.

3. **Purpose, stage and output.** What the work is for (essay, thesis chapter, dissertation, paper, proposal, report, product, internal decision), where it stands now (early idea, outline, draft, design, results in, under revision, preparing for examination or review), and what the researcher wants from this session.

4. **Audience or judge.** Who will read or assess the work, and what they reward: a supervisor, examiners, reviewers at a named venue, a funding panel, a team lead, a general readership. Ask for the field or discipline and any conventions it holds, because a claim that passes in one field fails in another.

5. **Constraints.** Deadline and time available; word or page limits; resources and access (data, compute, texts, archives, participants, equipment, collaborators); ethics, legal or disclosure limits; anything that is fixed and cannot change.

6. **Depth.** Offer the dial explicitly:
   - **light**: a focused pass on the most consequential weaknesses;
   - **standard**: a full examination across the arc;
   - **deep**: an exhaustive examination, revisiting stages and testing revisions;
   - **you decide**: Claude infers depth from the other answers.

7. **Format.** Dialogue (the default) or a single written memo. Mention the report variants (supervision note, examiner's report, reviewer's report) in one line, in case the researcher wants one at the end.

### Template for the intake request

Adapt the wording to the category and to what the researcher has already given.

```text
I'll examine your [category] work round by round. Each round takes one theme and asks
four or five questions about it from different angles; I'll summarise your answers before
the next round, and we'll finish with an audit of what held up and what to research next.

To set this up, please share what you have. Rough material is welcome, and skip anything
that doesn't apply.

1. The material: [category-specific wording, e.g. "your thesis and the argument for it"].
2. Everything behind it: notes, outlines, earlier drafts, [category-specific prior work],
   feedback you've had, and what you've read, tried or ruled out.
3. Purpose and stage: what this is for, where it stands now, and what you want from this
   session.
4. Audience: who will judge it, and in which field or discipline.
5. Constraints: deadline, length limits, resources or access, anything fixed.
6. Depth: light, standard, deep, or "you decide".
7. Format: dialogue (default) or a written memo. If you'd like a supervision note,
   examiner's report or reviewer's report at the end, say so.
```

## Step 2: the intake summary

When the researcher replies, read everything they supplied before writing. In a repository or project folder, also read the README, notes and drafts the researcher points to. Then send one message with these parts, in this order.

### 2.1 What I have

A short, neutral inventory:

- the material, in one or two sentences, with the central claim quoted;
- the prior work received, listed by type;
- purpose, stage, audience, constraints, depth and format as understood;
- **assumptions**: for every field left blank, the assumption you are making instead, so the researcher can correct it.

Note anything referred to but not supplied (a cited paper, a dataset, an earlier chapter). Do not fill those gaps from memory; mark them as unavailable.

### 2.2 Claim inventory

Run `claim-sorting.md` on the material and give a compact list of the main claims, each tagged with its kind and marked if it is load-bearing. Keep this short at intake: five to ten claims is usually enough. The full inventory goes into the audit.

### 2.3 Category fit

Compare the claim inventory with the category's fit test (each category skill defines one under "What counts as..."). Give one of three verdicts:

- **Fits.** Say so in one sentence and move on.
- **Fits with adjustments.** The material mostly belongs here, but parts of it belong to another category. Name those parts, say they will be recorded as open items for a separate session with the other skill, and continue.
- **Better served by another category.** Say which category, and why, in one or two sentences tied to specific claims in the material. Then, in the same message:
  1. invite the researcher to switch, naming the other skill;
  2. invite them equally to continue with this skill, and explain how to make the material fit it. Each category skill has a section on "making material fit this category"; use it to give two or three concrete reframings (for example, "frame the session around the model your results are meant to support, and share the model's assumptions") and say what extra material that reframing needs.

Do not refuse to continue, and do not argue the point if the researcher chooses to stay. Record their choice and proceed.

### 2.4 Depth estimate and plan

Estimate the number of rounds the session needs. Infer from every signal available, then adjust with the dial.

#### Signals that raise depth

- high stakes: examination, submission, a funding decision, a public or policy-facing claim;
- a mature artefact: a full draft, a completed design, results in hand;
- many load-bearing claims, or long chains of inference;
- a demanding audience: examiners, top venues, adversarial reviewers;
- substantial prior work that already settles the easy questions, so the session must go further;
- the researcher asks for thoroughness or a deep setting.

#### Signals that lower depth

- an early idea with little material yet;
- a near deadline with little time for revision;
- a single, narrow claim;
- the researcher wants a quick check or a light setting;
- prior feedback already identifies the main problems and the session only needs to address them.

**Baseline by dial** (one round is one theme with four or five questions):

| Dial | Typical rounds | Shape |
|---|---|---|
| Light | 3 to 5 | Stages compressed; one round on the most consequential weakness per major stage |
| Standard | 6 to 9 | Every stage visited; one to two rounds on the stages that bear the most weight |
| Deep | 10 to 15 | Every stage visited, the weightiest stages revisited, revisions retested |

If the dial is "you decide", choose the band the signals point to. If the dial and the signals disagree (a light setting on a thesis due for examination), follow the dial and say in one sentence what the light setting will leave unexamined.

**The plan** states:

- the estimated number of rounds;
- how those rounds divide across the arc stages, as the category skill allocates them;
- which moves are likely to be central;
- where checkpoints fall (see `checkpoints.md`);
- the end product (audit, memo, or a report variant).

Close the message by asking the researcher to accept the plan or change anything in it: the number of rounds, the emphasis, the format, or the category.

### Template for the intake summary

```text
What I have
- Material: ... Central claim: "..."
- Prior work: ...
- Purpose and stage: ... Audience: ... Constraints: ...
- Assuming (correct me): ...
- Referred to but not supplied: ...

Main claims
1. [kind, load-bearing] ...
2. [kind] ...

Category fit
[verdict and, if needed, the switch-or-reframe guidance]

Plan
About N rounds at [depth]: [stage allocation]. Checkpoints after rounds ...
Likely focus: ...
Ending: [audit / memo / report variant].

Shall I go ahead with this plan, or would you like to change the number of rounds,
the focus, or the format?
```

## Step 3: confirmation

When the researcher confirms, start round 1 in the format set by `turn-mechanics.md`. If they change the plan, restate the revised plan in one or two lines and start round 1 in the same message.

Revisit the estimate at every checkpoint. If the session is running long or short against the plan, say so and propose a revised number of rounds.

## Written memo instead of dialogue

The intake is the same. After confirmation, skip the rounds: run the arc internally and write the memo as described in `report-variants.md`.

## Never

- Never start the substantive questioning before the intake is confirmed, unless the researcher has said to start without it.
- Never ask for information that would not change the session. If an answer would not change the plan, the questions or the depth, leave the field out.
- Never fill a missing field silently. Every assumption made in place of a missing answer appears in the intake summary.
- Never reconstruct a referenced but unsupplied source from memory. Mark it unavailable and ask for it if it matters.
- Never ask for personal data about research participants. If the work involves human participants, note ethics approval and identifiability as constraints.
