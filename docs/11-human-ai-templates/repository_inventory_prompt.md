# Repository Inventory Prompt

## Purpose

Use this prompt after the kickoff or whenever the repository has changed significantly.

It helps create a structured inventory of what is already present.

## Prompt

```text
Please inspect the repository and create a structured inventory.

Goal:
- identify what already exists
- identify what is missing
- identify what is unclear or inconsistent

Please summarize the repository with these sections:

1. Project purpose
2. User flow or state flow
3. Technical stack
4. Architecture constraints
5. Generated vs. handwritten ownership
6. Build, debug, and flash workflows
7. Test strategy
8. Documentation structure
9. Naming rules
10. Done criteria
11. Known open points
12. Risks or inconsistencies

For each section, label the result as:
- clearly defined
- partially defined
- missing
- inconsistent

At the end, provide:
- a concise repository health summary
- the three most important gaps
- the three most important strengths
```
