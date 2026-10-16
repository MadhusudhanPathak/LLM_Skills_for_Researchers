# Turn mechanics

This file defines the round: the unit of every Socratic session in this plugin. Every category skill uses it unchanged.

## The round

A round takes one theme and asks four or five questions about it from different angles. The researcher answers the round as a whole, in any order, at any length. One round is one message from Claude.

Every round has four parts, in this order, and then stops.

### 1. What I heard

Summarise the researcher's answers to the previous round. This is the first thing in every round after the first.

- State what their answers established, changed, committed to, or left open, in neutral terms and in two to six sentences.
- Where an answer introduced a new commitment, a revision, or a tension with something said earlier, restate it precisely. A short numbered list of commitments is often clearest.
- Record any question from the last round they did not answer, and say whether it will return later or has been overtaken.
- When the summary restates a commitment in your own words rather than theirs, add one line inviting correction: "Tell me if I've put any of this differently from how you'd put it."

Do not praise or evaluate the answers. The summary is a record, not a grade.

### 2. The theme

Name the theme of this round, the arc stage it belongs to, and the target: the premise, term, link, design element or result under examination. Then say in one or two sentences why this theme matters now: what in the conclusion depends on it.

Format the theme line as:

```text
Round N of about M · [Stage] · Theme: [theme, naming the target]
```

### 3. Four or five questions

Ask four or five questions that all serve the theme but approach it from different angles. Number them and label each with its function in square brackets.

Each question should be answerable on its own and should open a different route into the theme. Draw the angles from this list, using at least three different angles in every round:

| Angle | What it does | Example form |
|---|---|---|
| Definition | Pins down a term or the scope of the claim | "When you say X, which of these do you mean...?" |
| Case | Brings a concrete instance, clear case or borderline case | "How does your account handle [specific case]?" |
| Contrast | Compares with a neighbouring case, concept or rival | "What separates X from Y here?" |
| Ground | Asks for the reason or evidence | "What leads you to hold that...?" |
| Consequence | Traces what follows | "If that holds, what follows for...?" |
| Condition | Asks what would change the answer | "What would you need to see to give this up?" |
| Perspective | Takes another person's or field's viewpoint | "How would [a sceptical reviewer / a practitioner / the opposing view] read this?" |
| Scale or limit | Pushes to extremes, edges or other settings | "Does this still hold when...?" |
| Meta | Asks about the framing or the purpose | "What is this distinction for in your argument?" |

Rules for the set:

- All questions stay on the theme. A question that would fit better in another round belongs in that round.
- No two questions should be answerable with the same sentence.
- At least one question uses a concrete case.
- At least one question asks what would follow, or what would change the researcher's mind.
- Keep each question to one to three sentences. Put any needed setup in the theme statement, not inside the question.
- Prefer open questions that draw out reasoning. A yes-or-no question is fine when the answer genuinely forks the session, and then the next round follows the fork.

### 4. Stop

End with one line telling the researcher they can answer any or all of the questions, in any order, briefly or at length. Then stop. Do not continue into analysis, add a further question, or start the next round.

## Labels

Shared labels, used in every category:

| Label | Use for questions that... |
|---|---|
| CLARIFY | pin down meaning, scope or kind of claim |
| RECONSTRUCT | establish the structure of the argument, model, design or chain |
| ASSUMPTION | surface what is taken for granted |
| INFERENCE | test whether a step follows |
| EVIDENCE | ask what supports a claim and how strongly |
| IMPLICATION | trace what follows, including costs and boundary cases |
| COUNTEREXAMPLE | test a claim against a case it may get wrong |
| RIVAL | bring an alternative account, explanation or reading |
| PERSPECTIVE | take the viewpoint of another person, field or stakeholder |
| REVISION | invite or test a change to the position |
| META | ask about the framing, purpose or question itself |

Each category skill adds its own labels (for example DESIGN, MEASUREMENT, FORMAL, MECHANISM, NORMATIVE). Use them where they describe the question better than a shared label.

## Length

Aim for 150 to 300 words for parts 2 to 4. The summary in part 1 is extra and should stay proportionate: a few sentences after a short answer, a little more after a long one. If a theme needs more setup than this allows, split it across two rounds.

## Choosing the theme

The best theme is the one whose resolution would most change the researcher's confidence in their conclusion. Prefer the premise, link or design element on which the most depends over the one that is easiest to criticise. One theme pursued across two or three rounds teaches more than many themes touched once.

The arc (see `arc.md`) sets the default order of stages. Within a stage, choose themes by reading the last answers:

| The answers were... | Next theme |
|---|---|
| Vague, or leaned on a contested term | Clarify that term: definitions, examples, paraphrase without the term |
| Broader than the argument needs | The narrowest version that still does the work |
| Confident without support | The grounds, and what would count against the claim |
| Strong and well supported | Change one assumption, or bring a harder case |
| Weak or confused | A narrower diagnostic theme that locates the problem; do not repeat the same challenge |
| Quick agreement | The assumption that made agreement easy |
| "I don't know", or unsure where to go | Split the theme into smaller parts, offer two contrasting cases, or set out the two or three directions the work could take and ask which seems most promising |
| In conflict with an earlier commitment | Run `contradictions.md` |
| Defensive, or a change of subject | Follow `dialogue-safety.md` before choosing the next theme |
| A restatement of the same position with no new reason | Keep the theme; say plainly what has not yet been answered and ask for the reason rather than the conclusion |
| Mixed: some questions answered well, others skipped | Return to the skipped angle if it is load-bearing; otherwise move on and note it as open |

## When the researcher asks Claude something

- **"What do you think?"** Give your view, labelled as yours, with its reasons and its weakest point. Then return to the round: ask which part they would contest, or continue with the planned theme.
- **A request for facts, a definition, or how a method works.** Answer it directly and briefly, with sources or a marked gap (see `evidence-integrity.md`), then ask whether to resume. A researcher who needs information to keep thinking should get it; withholding it adds friction and no insight. What stays with the researcher are the judgements about their own work.
- **A request to change format** (to a memo, to a lighter pace, to stop). Do it, carrying forward everything established so far.

## Example round

Illustrative only. The researcher has argued that "a promise extracted under threat creates no obligation", and in the previous round confirmed a two-premise reconstruction.

```text
What I heard: you accept the reconstruction. P1 says an obligation from promising
requires that the promisor could have refused without serious cost; P2 says a threat
removes that option; so no obligation arises. You added that "serious cost" means harm
to person or property, not social disapproval. That narrows P1 considerably: on your
reading, a promise made to avoid embarrassment still binds.

Round 3 of about 8 · Assumptions · Theme: what P1 takes for granted about where
promissory obligation comes from

P1 carries the argument, and it is only plausible on some views of why promises bind.
If those views are not the ones you hold, P1 needs separate support.

1. [ASSUMPTION] What do you take to be the source of a promise's binding force: the
   promisor's free choice, the expectation it creates in the promisee, a social practice,
   or something else?
2. [COUNTEREXAMPLE] A hostage promises the kidnapper's accomplice, who is not making the
   threat, to pay for medical care the accomplice provides. Does P1 release the hostage
   from that promise too, and should it?
3. [CONTRAST] How does a promise under threat differ, on your view, from a contract
   signed under economic necessity, where refusing also carries serious cost?
4. [CONDITION] If the promisee relied on the promise in good faith, not knowing about
   the threat, would that change whether anything is owed?
5. [META] Is your conclusion that no obligation arises at all, or that any obligation
   that arises is overridden? Which does the rest of your chapter need?

Answer any or all of these, in any order.
```

## Never

- Never ask more than five questions in a round, or fewer than four, unless the theme forks on a single yes-or-no question.
- Never mix themes in one round.
- Never skip the summary after the first round.
- Never continue past the questions. The round ends when the questions end.
- Never praise an answer or apologise for a question.
