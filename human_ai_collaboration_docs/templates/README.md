# Human-AI Templates

## Goal

Provide a reusable starter kit for the next project so human preparation and AI execution follow a clear, repeatable path from day one.

This folder is the practical companion to:

- [Collaboration](../collaboration/README.md)

The collaboration chapter explains the lessons learned from this project.

This folder provides:

- the working handbook
- the kickoff material
- the practical prompt set
- the preflight checklist
- the work-package brief
- the process-flow document
- the recovery protocol
- the BDD and test-design support documents

## Working model

The intended working model is:

1. the human reads the handbook
2. the human and ChatGPT move from one quality gate to the next
3. before execution, the current work package is clarified, checked, and brought into the right form
4. the BDD features, scenarios, and required test cases are made visible before implementation begins
5. once the current package is clear, the human releases bounded execution
6. ChatGPT Codex executes the bounded work locally inside the approved frame
7. when questions or problems appear, the work returns to human + ChatGPT clarification
8. after clarification, the process continues with the next gate or the revised package

This is the practical operating model of the AI-assisted engineering process.

Default split:

- ChatGPT is used for framing, clarification, review, BDD/test clarification, and gate-by-gate progress.
- ChatGPT Codex is used for bounded execution once a gate has been passed and the package has been released.
- If execution reveals questions or conflicts, return to ChatGPT clarification first.

## What This Folder Contains

### Core handbook

- [human_ai_project_handbook.md](./human_ai_project_handbook.md)
- [human_ai_process_flow.md](./human_ai_process_flow.md)

### Kickoff and framing

- [human_ai_kickoff_prompt.md](./human_ai_kickoff_prompt.md)
- [repository_inventory_prompt.md](./repository_inventory_prompt.md)
- [gap_analysis_prompt.md](./gap_analysis_prompt.md)

### Gate and execution flow

- [quality_gate_review_prompt.md](./quality_gate_review_prompt.md)
- [work_package_planning_prompt.md](./work_package_planning_prompt.md)
- [end_of_package_review_prompt.md](./end_of_package_review_prompt.md)
- [missing_input_recovery_prompt.md](./missing_input_recovery_prompt.md)
- [next_step_planning_prompt.md](./next_step_planning_prompt.md)

### Templates and supporting files

- [project_frame.template.json](./project_frame.template.json)
- [architecture_frame.template.json](./architecture_frame.template.json)
- [state_model.template.json](./state_model.template.json)
- [test_frame.template.json](./test_frame.template.json)
- [agent_workflow.template.json](./agent_workflow.template.json)
- [global_constraints.template.json](./global_constraints.template.json)
- [recovery_log.template.json](./recovery_log.template.json)
- [ai_project_preflight_checklist.md](./ai_project_preflight_checklist.md)
- [ai_work_package_brief.template.md](./ai_work_package_brief.template.md)
- [ai_test_case_brief.template.md](./ai_test_case_brief.template.md)
- [failure_recovery_protocol.md](./failure_recovery_protocol.md)
- [bdd_test_design_guideline.md](./bdd_test_design_guideline.md)
- [artifact_ownership_matrix.md](./artifact_ownership_matrix.md)
- [context_loading_strategy.md](./context_loading_strategy.md)

## Recommended Use

At the start of a new project:

1. copy this folder into the new repository
2. rename the JSON files by removing `.template`
3. run the kickoff session
4. create the repository inventory
5. create the gap analysis
6. pass the first quality gate
7. define the first work package
8. clarify the required BDD features, scenarios, and test cases
9. execute bounded work with Codex
10. review the result
11. continue gate by gate

## Summary

This folder is meant to make the process usable in daily engineering work.

It is not just a document collection.

It is a practical operating kit for moving from one quality gate to the next while keeping preparation, execution, testing, and recovery visible.
