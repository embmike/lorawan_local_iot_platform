# Human-AI Collaboration

## Goal

Capture the starting point for an AI-assisted engineering process:

- what the human should prepare before AI-assisted project work starts
- how human and AI should collaborate once the work begins
- how to reduce trial and error through a better project frame
- how to make decisions visible through explicit quality gates

This chapter uses the current `future_coffee_machine` project as the concrete example.

It is written as if these collaboration documents had already existed before the first implementation step.

## AI-Assisted Engineering Process

The secondary goal of this project is not only to prepare the next embedded project technically.

It is also to define and document an **AI-assisted engineering process** that can be used as a practical starting point for the next project.

The intention is:

- the human prepares the frame
- the AI works inside that frame
- both use explicit checkpoints to keep quality visible
- each work package is clarified before execution begins
- the resulting process is then validated in the next real project

So this chapter is both:

- a reflection on what would have improved the current project from the start
- a preparation model for the next project

## Why This Matters

In this project, the best results did not come from giving the AI a complete solution up front.

They came from giving the AI a clear frame:

- what the product is for
- which technical choices are fixed
- which names and documentation rules apply
- what quality means
- what belongs to unit tests and what belongs to system tests
- which workflows are allowed and which are not

That is the main lesson this chapter preserves for the next project.

The stronger the frame was, the less the collaboration depended on correction by trial and error.

## Recommended Document Model

Use two document types together:

### 1. Prose

Use prose for:

- purpose
- architecture explanation
- rationale
- boundaries
- workflow descriptions
- collaboration rules
- role guidance
- quality-gate explanations
- recovery rules

Use prose when a human must understand *why* something exists or *how* to work with it.

### 2. JSON

Use JSON for:

- stable state names
- command sets
- test case frames
- role responsibilities
- fixed constraints
- done criteria
- gate inputs and outputs
- allowed AI decisions
- recovery entries and global constraints

Use JSON when the AI or a tool should read the same facts repeatedly without reinterpretation.

## Recommended Starter Set

Before the next project begins, the following set should exist:

1. one prose project frame
2. one prose architecture frame
3. one JSON state model
4. one JSON test frame
5. one JSON collaboration and workflow frame

This chapter provides exactly that set for the current project.

For the reusable, project-neutral starter kit, see:

- [Human-AI Templates](../11-human-ai-templates/README.md)

The most practical companion files are:

- [ai_project_preflight_checklist.md](../11-human-ai-templates/ai_project_preflight_checklist.md)
- [ai_work_package_brief.template.md](../11-human-ai-templates/ai_work_package_brief.template.md)
- [ai_test_case_brief.template.md](../11-human-ai-templates/ai_test_case_brief.template.md)

For daily operation of the process, continue with:

- [human_ai_project_handbook.md](../11-human-ai-templates/human_ai_project_handbook.md)
- [human_ai_process_flow.md](../11-human-ai-templates/human_ai_process_flow.md)

## Files In This Folder

- [project_frame.json](./project_frame.json)
- [architecture_frame.json](./architecture_frame.json)
- [state_model.json](./state_model.json)
- [test_frame.json](./test_frame.json)
- [agent_workflow.json](./agent_workflow.json)

## Roles In The Collaboration

A practical collaboration model benefits from separating roles, even if one human performs several of them.

### Architect

The architect perspective is responsible for:

- system structure
- interfaces and boundaries
- technical constraints
- ownership rules
- consistency of the overall design
- definition of the early quality gates

### Developer

The developer perspective is responsible for:

- implementation details
- code changes
- refactoring
- integration of generated and handwritten code
- local technical decisions within the declared frame

### Tester

The tester perspective is responsible for:

- test strategy
- acceptance thinking
- state-based verification
- regression protection
- checking whether the result is observable and verifiable
- helping define BDD features, scenarios, and required test cases before execution

### Human

The human should:

- define the purpose
- define the constraints
- choose the priorities
- approve or reject open assumptions
- decide when a gate is actually passed
- release a work package before Codex execution starts

### AI

The AI should:

- structure the work
- challenge ambiguity
- detect missing information
- propose alternatives
- generate and refine artifacts
- keep code, tests, and documentation aligned with the declared frame

## How The Human Should Prepare The Work

The human should define these things early:

### Product frame

- what the application is for
- who the user is
- what the visible user flow is
- what is explicitly out of scope

### Technical frame

- which board, framework, and toolchain are fixed
- which generated tools are authoritative
- which files are handwritten and owned by developers
- which dependencies must stay decoupled in tests

### Naming frame

- domain names for states and actions
- naming style for tests
- readability rules for long names

### Test frame

- unit-test scope
- system-test scope
- startup path expectations
- reporting expectations
- required BDD or state-based acceptance structures

### Documentation frame

- where user guidance lives
- where architecture lives
- where test strategy lives
- where collaboration guidance lives
- what every test file must document

## Minimum Human Preparation Before AI Work Starts

The human does not need to design the complete solution up front.

But the human should prepare a minimum working frame before the first serious AI-assisted implementation step begins.

That minimum frame is:

1. a concrete product purpose
2. a named visible user flow
3. fixed technical constraints
4. explicit ownership boundaries
5. a defined test split
6. a documentation map
7. an initial decision model for open points

If one of these is missing, AI output becomes noticeably more exploratory and correction-heavy.

### 1. Product purpose must be concrete

The human should be able to answer:

- what problem the product solves
- who the intended user is
- what visible result the software must produce
- what is intentionally not part of the first scope

This reduces trial and error because the AI no longer has to guess whether a feature is central, optional, or unwanted.

### 2. User flow must be named before implementation

The visible states and transitions should be written down early.

For this project, examples are:

- splash screen
- selection screen
- brewing screen
- return to selection screen

This matters because UI, tests, logs, and documentation all depend on the same state language.

### 3. Technical constraints must be frozen early

The human should declare:

- board and MCU
- toolchain
- generated tools that remain authoritative
- transport and debug interfaces
- memory and startup model, if already fixed

This reduces wasted work because the AI does not build solutions around the wrong technical assumptions.

### 4. Ownership boundaries must be explicit

The human should state which areas are:

- generated
- handwritten
- editable
- stable interfaces
- temporary or experimental

That is especially important when CubeMX, TouchGFX Designer, BSP code, and handwritten code live in the same repository.

### 5. Test worlds must be separated from day one

The human should decide early:

- what is unit-tested on the host
- what is integration- or system-tested on the real board
- what transport the system tests use
- how success, semantic failure, and timeout are reported

Without that split, AI-assisted testing tends to blur boundaries and produces unnecessary rework.

### 6. Documentation structure must exist before depth work starts

The human should define where these topics will live:

- architecture
- build and flash
- debugging
- drivers
- artifacts
- TouchGFX
- testing
- collaboration lessons
- reusable templates

This reduces friction because implementation and documentation can grow into known places instead of being reorganized later.

### 7. Open points must have a visible handling rule

Not everything can be defined up front.

The human should therefore decide:

- which open points block implementation
- which open points may be carried temporarily
- how assumptions must be documented
- when an assumption must be reviewed again

This is where quality gates become necessary.

## Recommended Preparation Sequence

The most effective human preparation order is:

1. define the product purpose and user flow
2. freeze the technical constraints
3. define naming and ownership boundaries
4. separate the test worlds
5. create the documentation map
6. define the first quality gates
7. for each package, clarify the expected behavior and required tests before execution
8. only then start larger AI-assisted implementation work

This sequence matters because each step removes a different kind of ambiguity:

- product ambiguity
- technical ambiguity
- naming ambiguity
- quality ambiguity
- documentation ambiguity
- decision ambiguity

## Quality Gates

Not everything can be determined in advance.

Therefore, the AI-assisted engineering process should use explicit quality gates.

A quality gate is a visible decision point where human and AI check whether the current frame is good enough to continue with confidence.

### Recommended Gate Set

#### Gate 1: Problem and scope are clear

Questions:

- Is the product purpose concrete?
- Is the visible user flow named?
- Are non-goals explicit?

#### Gate 2: Technical frame is fixed enough

Questions:

- Are board, toolchain, and major tools fixed?
- Are generated vs. handwritten ownership boundaries explicit?
- Are the accepted workflows named?

#### Gate 3: Quality model is visible

Questions:

- Is the test split defined?
- Are documentation destinations defined?
- Are naming rules and done criteria visible?
- Is it visible how BDD features, scenarios, or equivalent state-based tests will be prepared?

#### Gate 4: Work package is ready

Questions:

- Is the task small enough and well-bounded?
- Are assumptions visible?
- Is the expected output known?
- Is the review path clear?
- Are the relevant BDD features, scenarios, and required test cases already clarified?

#### Gate 5: Result is acceptable

Questions:

- Does the output stay inside the declared frame?
- Are code, tests, and documentation aligned?
- Are new open points visible and assigned?
- Did execution reveal a rule that must be written back into the frame or recovery log?

## Human-AI Gate Collaboration

When a gate is reached, human and AI should answer together:

- what is already known?
- what is still unclear?
- what assumptions are currently being made?
- which assumptions are acceptable temporarily?
- what must be decided before continuing?
- what documentation must be updated now?

The human remains responsible for releasing the gate.

The AI should help by:

- surfacing ambiguity
- checking consistency
- proposing the next smallest safe step
- preventing hidden uncertainty from leaking into implementation

## Readiness Gate For AI Implementation

The AI is ready for efficient execution when the human can answer these questions without hesitation:

- What is the user-visible flow?
- Which tools are authoritative?
- Which files are generated and which are handwritten?
- Which names are fixed?
- What belongs to unit tests and what belongs to system tests?
- What is the accepted debug and flash workflow?
- Where must the resulting documentation go?
- Which open points are allowed to remain open?
- Which BDD features, scenarios, or state-based tests already define the expected behavior?

If these answers do not yet exist, the next best AI task is not implementation.

It is helping the human build the missing frame first.

## How The AI Should Use The Frame

The AI should read the JSON facts first, then the prose.

Recommended baseline order:

1. `project_frame.json`
2. `architecture_frame.json`
3. `state_model.json`
4. `test_frame.json`
5. `agent_workflow.json`
6. supporting prose chapters in `docs/...`

For larger projects, the loading should stay selective:

- always load global constraints and the work-package-specific facts
- then load only the detail material relevant for the current package
- then load the supporting prose required for clarification or review

Why this order works:

- the AI sees the fixed facts first
- then it sees the rationale and workflow around those facts
- that reduces unnecessary exploration

## ChatGPT And ChatGPT Codex

A practical split is useful.

### ChatGPT

Use ChatGPT primarily for:

- clarification
- architecture thinking
- trade-off analysis
- review
- documentation
- test strategy
- BDD/test clarification
- process design
- critical questioning
- quality-gate preparation

### ChatGPT Codex

Use ChatGPT Codex primarily for:

- code generation
- repository-local edits
- targeted refactoring
- test implementation
- multi-file consistency work
- implementation support inside the approved frame

### Simple rule

A simple rule is:

- ChatGPT helps define the work
- ChatGPT helps clarify the expected behavior and required tests
- ChatGPT Codex helps execute the work in code

That rule is not absolute, but it is a good default.

## Lessons Learned From This Project

The following preparation would have reduced friction from the beginning:

### 1. Testing should have been split from the start

The clean split is:

- testing overview
- unit testing
- system testing

That separation is now reflected in:

- [docs/07-testing/README.md](../07-testing/README.md)
- [docs/08-unit-testing/README.md](../08-unit-testing/README.md)
- [docs/09-system-testing/README.md](../09-system-testing/README.md)

### 2. The system-test transport should have been declared explicitly

The board-side system tests now use:

- USB CDC / COM on `CN13`

That should have been fixed and documented at the start, not discovered later.

### 3. Shell-first execution should have been declared explicitly

The final decision is:

- unit tests may use Visual Studio Test Explorer
- Python system tests use the shell path

That distinction belongs in the initial frame because it affects tooling, reports, and user expectations.

### 4. Naming rules should have been formalized earlier

The readable naming rule from this project is:

- keep names visually readable
- use underscores for long logical groupings
- prefer explicit state and behavior wording over clever or compressed names

### 5. Test design should have been written as state-based from the start

The stable structure is:

- defined initial state
- one event
- defined resulting state
- explicit timeout when time-dependent

That rule now applies well to both unit-test descriptions and system-test descriptions.

### 6. Human preparation quality directly changed AI efficiency

The strongest practical lesson from this project is:

- when the human defined a clear frame, the AI moved fast and accurately
- when the frame was incomplete, progress depended more on interactive correction

The difference was visible in several areas:

- boot and debug workflow stabilization
- naming cleanup
- documentation structure
- TouchGFX ownership boundaries
- testing architecture

So the preparation work is not administrative overhead.

It is an engineering accelerator for AI-assisted development.

## Suggested Use In The Next Project

At the start of the next project:

1. copy this folder
2. rename the project-specific values
3. run the project preflight checklist
4. write the first AI work package brief
5. define the first quality gates
6. clarify the first package behavior and required tests
7. revise only the facts that really changed
8. review the document set before implementation begins

That keeps the next project from starting with a blank collaboration model.

## BDD And TDD In The Process

(see separate section)

- [bdd_tdd_process_section.md](./bdd_tdd_process_section.md)
- [bdd_test_design_guideline.md](../11-human-ai-templates/bdd_test_design_guideline.md)

## Summary

The main collaboration lesson from this project is simple:

- the human should prepare the frame
- the AI should execute inside that frame
- both should use visible quality gates to manage uncertainty
- each work package should be clarified before Codex execution begins
- BDD features, scenarios, and required tests should be visible before implementation

The better the frame is prepared, the less the project depends on correction by trial and error.
