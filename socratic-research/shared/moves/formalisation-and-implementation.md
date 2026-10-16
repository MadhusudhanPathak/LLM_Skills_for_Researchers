# Formalisation, proof and implementation

Use this move when an informal idea becomes a formal object (a definition in logic or mathematics, a model, a specification, an objective, an algorithm) or when a formal object becomes a working artefact (code, a system, a protocol, a device). Each translation can drop, distort or add content, and a result can become true by construction without anyone noticing.

## Use when

- An informal claim is being formalised, or a formalisation is under examination.
- A proof, derivation or formal guarantee is offered.
- A specification, design or architecture is proposed.
- A definition, specification or objective has been implemented in code, hardware or a procedure.
- A formal result is applied to a real system.

## 1. From informal to formal

- State the claim in plain language. What are its entities, relations, quantifiers and conditions?
- Which formalism is being used (logic, probability, decision theory, a causal model, a state-transition system, a type system, a set of equations)? Why that one?
- Map each symbol to the informal notion it stands for. Is anything in the informal claim left without a symbol?
- What does the formalisation capture, and what does it omit?
- Which assumptions did the formalisation add that were not in the informal claim? (Determinism, stationarity, independence, full observability, rationality, finiteness, continuity, a fixed environment, a particular model of agents.)
- Does the formalisation make the claim trivial, or give it unintended consequences?
- Test it on a representative case and on a case the informal claim would get right. Does the formal version agree?

Formal notation is not evidence that the underlying assumptions are true.

## 2. Proofs and derivations

- What exactly does the theorem state? Under which assumptions?
- Is each step justified? Which steps rely on lemmas, and are those lemmas proved or cited?
- Which assumptions does each step use? Are any used but not stated?
- What happens at the boundary conditions: zero, infinity, empty sets, degenerate cases, ties?
- Is this a full proof or a sketch? Which gaps would a careful reader find?
- Is there a counterexample when one assumption is relaxed? Does that show the assumption is needed?
- Has the proof been checked independently, by a person or a proof assistant?

## 3. Specification

- What problem does the artefact solve, for whom, under what conditions?
- What are the requirements: functional (what it must do), and non-functional (performance, reliability, security, usability, cost, maintainability)?
- Are the requirements consistent with each other? Where do they trade off?
- Is the specification complete: does it say what happens in every case, including errors, invalid input, overload and failure of dependencies?
- Can each requirement be checked? How?
- What assumptions about the environment does the specification make?

## 4. Design and architecture

- What are the components, their responsibilities, and the interfaces between them?
- What invariants must hold at all times? What maintains them?
- Where is state kept, and who can change it?
- What happens when a component fails, is slow, or behaves incorrectly?
- How does the design scale: with more load, more data, more users, more components?
- What alternatives were considered, and why were they rejected?
- What is the complexity (time, space, communication) and is it justified?

## 5. From formal object to implementation

Trace each component of the definition or specification into the implementation:

concept → formal term → specification → code path or procedure → test

- Which parts of the concept were dropped, approximated or replaced for tractability?
- Which assumptions did the implementation add (data representation, numerical precision, library behaviour, hardware, ordering, timing)?
- Is the result true by construction: does the implementation make the claimed property hold trivially, so that the test cannot fail?
- Construct a case where the implementation passes and the intended property fails. Construct the reverse.

## 6. Verification and validation

- **Verification**: does the artefact meet its specification? By proof, model checking, testing, review?
- **Validation**: does the specification capture what is actually needed? An artefact can be verified and useless.
- What test coverage exists? Which behaviours are untested?
- Are tests independent of the implementation, or written by reading it?
- Is there a test that would fail if the key claim were false?

## 7. Applying a formal result to a real system

- Which assumptions of the formal result does the real system satisfy, and how do you know?
- Which does it violate? Does the result degrade gracefully, or fail entirely, when they are violated?
- Is the formal guarantee being presented as a real-world guarantee?

## Watch for

- A formal model that has lost exactly the feature that made the informal problem interesting.
- Assumptions introduced by the formalism and never examined.
- A proof whose hardest step is "it is easy to see that".
- An implementation whose tests share its assumptions, so they cannot catch errors in them.
- Verification mistaken for validation.

## Artefacts

- **Traceability table**: concept, formal term, specification item, code path or procedure, test, and status of each link.
- **Formalisation ledger**: what was captured, what was omitted, and what was added by the formalisation.
- **Proof audit**: each step, its justification, the assumptions it uses, and its status.
- **Specification check**: requirements, their consistency, completeness, checkability and environmental assumptions.
