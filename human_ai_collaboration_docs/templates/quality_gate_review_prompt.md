# Quality Gate Review Prompt

Use this prompt with ChatGPT when you want to inspect the current gate before execution continues.

## Prompt

Review the current quality gate for this project and answer in a structured way:

1. What is already clear and stable?
2. What is still unclear or missing?
3. Which facts already exist but are still in the wrong form or wrong document?
4. Which open points are blocking and which are temporarily acceptable?
5. Which BDD features, scenarios, or state-based tests already define the expected behavior?
6. Which required test cases are still missing for this package?
7. Is this gate ready to pass? If not, what is the next clarification step?

Return the answer in sections:

- stable facts
- missing inputs
- formatting/documentation gaps
- test and scenario status
- gate decision
- recommended next step
