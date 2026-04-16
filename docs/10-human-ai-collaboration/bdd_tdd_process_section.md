## BDD And TDD In The Process

The process should not treat BDD and TDD as competing alternatives.

They serve different purposes and should be combined deliberately.

### Process level: BDD-guided

At the workflow and system level, the project should be guided by behavior descriptions.

This means the project should describe:

- what the user or operator should observe
- what a quality gate should produce
- what a work package should deliver
- what a successful review should confirm

In practice, this means there should always be something that the current result can be checked against.

Depending on the level, this reference can be:

- a behavior description
- an acceptance description
- a scenario
- a gate definition
- a checklist
- a test case

That is why the overall process is best understood as **BDD-guided**.

BDD is a good fit at this level because it keeps attention on expected behavior and observable outcomes.

Examples:

- Given the repository already contains starter documents
- When the human starts the kickoff with ChatGPT
- Then the process should produce an inventory, a gap analysis, and the first quality gates

- Given a work package has been executed
- When the result is reviewed
- Then code, tests, and documentation should be aligned and new open points should be visible

### Implementation level: TDD-oriented

At the implementation level, the process should be more TDD-oriented.

This applies especially to:

- small technical units
- deterministic logic
- state transitions
- formatters
- rules
- helper functions
- presenter or model behavior that can be isolated well

At this level, the most effective reference is usually a concrete test.

That means:

- define the expected behavior of the unit
- write or define the check first when practical
- implement the unit
- verify that the unit satisfies the check
- refine the implementation without losing the expected behavior

### Practical rule

A useful default rule is:

- use **BDD** to define expected workflow and system behavior
- use **TDD** to implement and verify small technical units

### Why this matters for the AI-assisted engineering process

The AI also needs a reference point.

It should not generate work into a vacuum.

There should always be an explicit basis for evaluation, such as:

- a scenario
- an acceptance description
- a quality-gate definition
- a checklist
- a unit test
- a system test

Without such a reference, review becomes subjective and correction becomes more trial-and-error driven.

With such a reference, both the human and the AI can check whether the current result is acceptable.

### Summary

The process should therefore be:

- **BDD-guided at the workflow level**
- **TDD-oriented at the implementation level**

This gives the project two useful anchors:

- observable expected behavior at the process and system level
- concrete verification at the technical unit level
