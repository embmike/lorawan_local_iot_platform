# Human-AI Kickoff Prompt

## Goal

Use this prompt at the very beginning of a new project.

The human has already created a GitHub repository and starts a first conversation with ChatGPT.

The purpose of this kickoff is:

- to clarify what already exists in the repository
- to identify what is still missing
- to separate what can be worked out together in the chat from what the human must still provide
- to create the first structured project frame before implementation begins

This prompt is intentionally written for practical use.

---

## Kickoff Prompt Template

```text
Hello, I want to start a new project with you.

Context:
- I have already created the GitHub repository for this project.
- At the beginning, I want to define the project frame together with you before implementation starts.
- Our goal is to reduce trial and error by making the scope, constraints, workflows, and quality expectations explicit.

Your role in this first session:
1. Help me identify what is already present in the repository.
2. Help me identify what is missing or still unclear.
3. Separate the following three categories:
   a) what already exists
   b) what we can define together now in this chat
   c) what I, as the human, still need to provide or decide
4. Help me build the initial project frame for an AI-assisted engineering process.

Please proceed in this order:

Step 1:
Review the repository structure and existing documents.

Step 2:
Summarize what is already available regarding:
- project purpose
- user flow or state flow
- technical stack
- architecture constraints
- generated vs. handwritten ownership
- test strategy
- documentation structure
- workflows
- naming rules
- done criteria
- known open points

Step 3:
Create a gap analysis with three sections:
- already defined
- can be defined together now
- must still be provided by the human

Step 4:
Ask only the most necessary clarification questions.
Do not ask broad or redundant questions.
Prefer grouped questions that help complete the project frame efficiently.

Step 5:
Based on the answers, propose:
- the initial project frame
- the first quality gates
- the first work package that is small, safe, and well-bounded

Important working rules:
- Do not jump directly into implementation.
- First establish the frame.
- Make uncertainty visible.
- Mark assumptions explicitly.
- Keep code, tests, and documentation aligned.
- Prefer a structured engineering approach over ad-hoc exploration.

At the end of this kickoff, I want:
- a clear summary of what already exists
- a list of missing inputs
- a proposal for the first quality gates
- a recommendation for what we should do next
```

---

## Expected Output Of The Kickoff

A good kickoff should produce:

1. a repository and documentation inventory
2. a gap analysis
3. a first project frame
4. a first set of quality gates
5. a proposal for the first work package
6. a clear list of human follow-up inputs

---

## Recommended Follow-Up

After the kickoff:

1. fill or refine the starter JSON files
2. update the documentation map
3. run the preflight checklist
4. write the first work package brief
5. only then begin larger implementation work
