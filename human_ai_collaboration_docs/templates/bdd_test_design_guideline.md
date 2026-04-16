# BDD and Test Design Guideline

## Goal

Clarify how BDD features, scenarios, and practical test cases fit into the Human-AI engineering process.

## Core rule

The expected behavior should be clarified before ChatGPT Codex starts implementation.

That means:

- the human and ChatGPT define the relevant behavior first
- the relevant BDD features and scenarios are made visible before execution
- the required test cases are identified before implementation starts
- ChatGPT Codex implements and refines inside that approved behavior frame

## Responsibility split

### Human + ChatGPT

Responsible for:

- deciding what behavior is required
- deciding what is in scope for the package
- defining or reviewing BDD features and scenarios
- defining which test cases are required for done
- deciding which tests are unit tests and which are system tests
- deciding what remains open

### ChatGPT Codex

Responsible for:

- implementing the approved behavior
- generating or refining test code for the approved scenarios
- keeping code and tests aligned
- stopping when the scenarios are too vague or contradictory

## Practical rule for work packages

Before a package is released for execution, it should be clear:

- what behavior changes or is added
- which scenarios describe that behavior
- which test cases are mandatory
- what belongs to unit tests
- what belongs to system tests
- what is intentionally postponed

## Preferred scenario structure

A useful default is:

- defined initial state
- one event or trigger
- defined resulting state
- explicit timeout if time-dependent

That fits well with both BDD wording and state-based testing.

## Summary

BDD and test design are not late-stage by-products.

They belong to the clarification of the work package before execution begins.
