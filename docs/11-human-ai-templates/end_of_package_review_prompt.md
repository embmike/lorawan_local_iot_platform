# End Of Package Review Prompt

Use this prompt with ChatGPT after ChatGPT Codex has completed one bounded work package.

## Prompt

Review the result of the completed work package.

Please answer:

1. Does the result stay inside the approved frame?
2. Are code, tests, and documentation aligned?
3. Were the approved BDD scenarios or required test cases covered?
4. Did execution reveal a new rule, conflict, or missing input?
5. Which results are acceptable now?
6. Which follow-up actions are still required?
7. Should anything be written back into the frame, package, or recovery log?

Return the result in sections:

- accepted results
- deviations
- test/scenario coverage
- documentation alignment
- required write-back updates
- final review decision
