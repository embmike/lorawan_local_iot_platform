# Human-AI Project Handbook

## Goal

This handbook describes how a human works with ChatGPT and ChatGPT Codex from one quality gate to the next.

The idea is simple:

- the human reads the handbook
- the human and ChatGPT clarify the frame together
- they move from one quality gate to the next
- once a gate is clear, the human and ChatGPT Codex execute the work
- when questions or problems appear, the work returns to human + ChatGPT clarification
- after clarification, the process continues with the next gate

This is the practical operating model of the AI-assisted engineering process.

## Default tool split

Use the tools with a simple default rule:

- ChatGPT for framing, clarification, review, and gate decisions
- ChatGPT Codex for bounded execution inside an approved frame

If execution reveals a gap, conflict, or missing input, return to ChatGPT before continuing.

## Core principle

The process should not begin with implementation.

It should begin with framing.

The process should also not continue blindly when uncertainty becomes visible.

It should stop, clarify the issue, and only then continue.

So the basic cycle is:

1. understand the current state
2. clarify what is missing
3. pass the next quality gate
4. execute the bounded work package
5. review the result
6. return to clarification if needed
7. continue to the next gate

## Roles

### Human

The human is responsible for:

- project intent
- priorities
- approval decisions
- final interpretation of open points
- gate release

### ChatGPT

Use ChatGPT for:

- clarification
- structuring the frame
- reviewing consistency
- finding missing information
- defining and checking quality gates
- preparing work packages
- documenting decisions
- resolving questions and problems

### ChatGPT Codex

Use ChatGPT Codex for:

- repository-local implementation work
- code changes
- refactoring
- test implementation
- multi-file editing
- keeping changed files aligned

### Important rule

ChatGPT should usually help define the work.

ChatGPT Codex should usually help execute the approved work.

If execution reveals a gap, ambiguity, or conflict, return to ChatGPT first.

## Recommended operating loop

### Phase 1: Kickoff

Use ChatGPT to inspect the repository and existing documentation.

Goal:

- understand what already exists
- identify what is missing
- separate what can be clarified together from what the human must still provide

Output:

- repository inventory
- first gap analysis
- initial project frame
- first quality gates

### Phase 2: Gate-by-gate clarification

The human and ChatGPT move from one gate to the next.

For each gate, answer:

- what is already known?
- what is still unclear?
- what assumptions are being made?
- what blocks progress?
- what is safe to postpone?
- what must be documented now?

If the frame is strong enough, the gate can be passed.

If not, stay in clarification mode.

### Phase 3: Execution

Once the next gate is clear, the human and ChatGPT Codex execute the bounded work package.

Execution should happen only when:

- the task is bounded
- the expected output is clear
- assumptions are visible
- review responsibility is clear

### Phase 4: Review

After execution, the result is reviewed.

Check:

- does the result stay inside the frame?
- are code, tests, and documentation aligned?
- were new assumptions introduced?
- did new open points appear?

If yes, and they are important, return to clarification with ChatGPT.

### Phase 5: Continue

After review, move to the next quality gate.

## Recommended gate sequence

A practical default sequence is:

1. Gate 1: Project purpose and scope are clear
2. Gate 2: Technical frame is clear
3. Gate 3: Quality frame is clear
4. Gate 4: Work package is ready
5. Gate 5: Result is accepted
6. Gate 6: Next package is selected

The sequence can be adapted, but the principle remains the same:
do not execute unclear work.

## When to stop execution and return to clarification

Return from Codex work to ChatGPT when:

- the repository structure is different than expected
- a needed input is missing
- the code conflicts with the declared architecture
- the ownership boundaries are unclear
- the test approach is unclear
- the expected output changed
- the result would require new assumptions

This return is not a failure.

It is part of the process.

## Minimal daily usage model

In day-to-day work, the human can use the process like this:

1. open the handbook
2. identify the current gate
3. use the matching prompt with ChatGPT
4. clarify until the gate is passable
5. hand the bounded task to Codex
6. review the result
7. either continue or return to clarification

## Practical rule for momentum

Do not switch back to broad exploration once a gate is clear.

Do not continue implementation once a gate is unclear.

That balance is what keeps the process effective.

## Prompt set in this folder

This folder contains prompts for:

- kickoff
- repository inventory
- gap analysis
- quality-gate review
- work-package planning
- end-of-package review
- missing-input recovery
- next-step planning

Use them as a practical toolkit, not as rigid ceremony.

## Summary

The process is:

- human reads the handbook
- human and ChatGPT move from gate to gate
- once the frame is clear, human and ChatGPT Codex execute the work
- when questions or problems appear, return to human + ChatGPT clarification
- then continue with the next gate

That is the intended working model for the next project.
