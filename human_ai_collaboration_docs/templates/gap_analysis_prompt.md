# Gap Analysis Prompt

## Purpose

Use this prompt after the repository inventory.

It separates what is already present from what can be clarified together now and what must still be provided by the human.

## Prompt

```text
Based on the current repository and project discussion, create a gap analysis.

Please separate the findings into exactly these three groups:

1. Already defined
2. Can be defined together now in this chat
3. Must still be provided or decided by the human

Cover at least these topics:
- project purpose
- user flow
- technical constraints
- architecture boundaries
- generated vs. handwritten ownership
- test split
- workflows
- naming rules
- documentation map
- done criteria
- open points

At the end, provide:
- the smallest missing set needed to pass the next quality gate
- the most important blocking uncertainty
- your recommendation for the next clarification step
```
