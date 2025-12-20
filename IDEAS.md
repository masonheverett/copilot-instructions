# Ideas

This file is a place to jot down ideas for future instruction templates, guidelines, or enhancements to the existing copilot-instructions repository.

## Unprocessed Thoughts
- Spec Kit doesn't always write tasks in a way that follows TDD, so it might be good inject TDD principles into the template, agent, or prompt.
- Include a background step and a discovery step in the spec kit process
  - Background step: Summarize current state of the project based on available documentation (docs/, README.md, specs/, etc.)
  - Discovery step: Fact finding mission to support the specification process; primarily looking into sample input and output data, asking questions about edge cases, and clarifying requirements
- Update Seven Cs to be clear about output, potentially including a template
  - For each C, provide summary of findings, justification for score (5 stars scale), tactical recommendations for bringing the score to 5 stars if the score is not already 5 stars, and clear outline of what information or decisions are needed from the user to implement those recommendations, deferring broadly to the user rather than making assumptions
  - When asking for information from the user, provide options and a recommendation with justification rather than open-ended questions
  - Think about making an agent for TDD specifically
