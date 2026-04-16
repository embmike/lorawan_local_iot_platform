# Failure Recovery Protocol

## Goal

Define what happens when bounded execution fails, reveals a contradiction, or uncovers missing input.

The purpose of this protocol is not to add bureaucracy.

It is to prevent the same conflict from being solved again and again in isolated chats.

## Principle

When ChatGPT Codex encounters a blocking conflict, the correct next step is not silent improvisation.

The correct next step is:

1. stop bounded execution
2. make the conflict visible
3. return to human + ChatGPT clarification
4. update the relevant frame, package, test definition, or recovery log
5. release execution again only after clarification

## Typical triggers

Use this protocol when execution reveals any of the following:

- missing file or folder ownership information
- contradiction between generated and handwritten boundaries
- unclear destination for code, tests, or documentation
- scenario wording that is not implementable or not testable enough
- missing technical constraint
- conflict between repository reality and declared frame
- unexpected hardware, toolchain, or test-environment restriction

## Required recovery questions

Human + ChatGPT should answer:

- What exactly failed?
- Is the problem local or structural?
- Which artifact is affected?
- Which earlier assumption was incomplete or wrong?
- Does the project frame need to change?
- Does the work package need to change?
- Do the BDD scenarios or required tests need to change?
- What should be written into the recovery log?

## Recovery outcomes

A recovery step should end with one of these outcomes:

### 1. Local package fix

Use when:

- the issue stays inside the approved package
- no global rule changes
- no architecture boundary changes

Update:

- work package brief
- optional local test or documentation detail

### 2. Test clarification fix

Use when:

- the behavior is still desired
- but the scenario, acceptance wording, or test split was too vague

Update:

- BDD/test artifacts
- test frame if necessary
- work package brief

### 3. Frame update

Use when:

- a new rule must apply beyond the current package
- ownership, tool authority, architecture, or constraints change

Update:

- project frame
- architecture frame
- global constraints
- recovery log

## Minimal recovery record

Every blocking recovery should capture:

- issue id or date
- trigger
- short problem statement
- impacted artifacts
- decision
- updated document(s)
- release condition for resumed execution

## Summary

The process should learn from execution problems.

A conflict is not only something to fix.

It is also a signal that the frame, test definition, or package description may need to become clearer.
