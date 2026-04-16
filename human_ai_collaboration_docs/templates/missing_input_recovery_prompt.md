# Missing Input Recovery Prompt

Use this prompt with ChatGPT when ChatGPT Codex or the human detects missing or conflicting input during execution or package review.

## Prompt

Analyze the detected missing input or conflict and structure the recovery step.

Please answer:

1. What exactly is missing, contradictory, or wrongly placed?
2. Is the problem local to the work package or does it affect the project frame?
3. Which document should be updated?
4. Does this affect BDD scenarios or required test cases?
5. What is the smallest safe correction?
6. What must be true before execution can resume?
7. Create a recovery-log entry draft.

Return the result in sections:

- problem summary
- scope of impact
- required document updates
- scenario/test impact
- recovery decision
- resume condition
- recovery-log draft
