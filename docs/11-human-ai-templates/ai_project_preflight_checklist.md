# AI Project Preflight Checklist

## Goal

Use this checklist before the first larger AI-assisted implementation step.

The goal is not perfection.

The goal is to make sure the project frame is explicit enough that AI work starts as execution, not as uncontrolled exploration.

## Project identity

- [ ] The repository name is fixed.
- [ ] The project purpose is written in one or two clear sentences.
- [ ] The intended user or operator is named.
- [ ] The visible user flow or state flow is named.
- [ ] Explicit non-goals are listed.

## Technical frame

- [ ] Board, MCU, or target platform are named.
- [ ] Toolchain and major tools are named.
- [ ] Generated tools are identified.
- [ ] Generated vs. handwritten ownership is explicit.
- [ ] Accepted debug and flash workflows are named.
- [ ] Important interfaces and transports are named.

## Quality frame

- [ ] Unit-test scope is defined.
- [ ] System-test or integration-test scope is defined.
- [ ] Reporting expectations are defined.
- [ ] Done criteria are visible.
- [ ] Naming rules are visible.
- [ ] Documentation destinations are visible.

## Collaboration frame

- [ ] The human decision boundary is explicit.
- [ ] Allowed AI decisions are explicit.
- [ ] Temporary assumptions are allowed or forbidden by rule.
- [ ] Open points are visible.
- [ ] The first quality gates are defined.

## First-session readiness

- [ ] A kickoff session has been done.
- [ ] The existing repository contents have been reviewed.
- [ ] A gap analysis has been created.
- [ ] Missing human inputs are listed.
- [ ] The first work package is small and bounded.

## Minimum rule

If several boxes are still unchecked, the next AI task should usually be:

- improve the project frame
- not start deeper implementation yet
