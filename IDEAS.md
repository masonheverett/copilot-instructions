# Ideas

This file is a place to jot down ideas for future instruction templates, guidelines, or enhancements to the existing copilot-instructions repository.

## Unprocessed Thoughts
- Spec Kit doesn't always write tasks in a way that follows TDD, so it might be good inject TDD principles into the template, agent, or prompt.
- Include a background step and a discovery step in the spec kit process
  - Background step: Summarize current state of the project based on available documentation (docs/, README.md, specs/, etc.)
  - Discovery step: Fact finding mission to support the specification process; primarily looking into sample input and output data, asking questions about edge cases, and clarifying requirements
- Think about making an agent for TDD specifically, like spec kit has the analyze agent

## Changelog

### 2025-12-20
v1.0 — Seven Cs Framework Hardening
- Reframed the Seven Cs as an explicit output contract rather than an implicit quality checklist.
- Introduced a mandatory per-C output structure, including scoring, findings, justification, tactical recommendations, and required user decisions.
- Added a shared 1–5 star scoring rubric, redefining ⭐⭐⭐⭐⭐ as exceptional (decision-optimal) rather than merely sufficient.
- Elevated scoring discipline with:
  - Explicit guidance on score rarity and usage
  - A formal “decline to score” rule when evaluation would be speculative
  - Added a mandatory Audience & Decision Context gate to prevent misaligned evaluations.
  - Required framed decision requests (options + recommendation) instead of open-ended questions.
Clarified evaluation order based on failure cost.
  - Strengthened per-C definitions with explicit criteria for what “5 stars” means.
  - Added an anti-patterns section to prevent common misuse and score inflation.
