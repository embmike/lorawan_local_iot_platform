# Context Loading Strategy

## Goal

Keep the AI context focused enough to stay precise while still loading the facts that matter.

## Default rule

Do not load everything blindly if the package is narrow.

Instead use three layers:

### 1. Always-load layer

Load these facts every time:

- global constraints
- relevant package brief
- relevant test and scenario expectations

### 2. Package-specific layer

Load only the details needed for the current task:

- relevant architecture section
- relevant state model section
- relevant test frame section
- relevant folder or artifact rules

### 3. Supporting prose layer

Load the prose needed for:

- clarification
- trade-off explanation
- review
- rationale

## Summary

The goal is not to reduce discipline.

The goal is to reduce noise and keep the current work package in focus.
