## Changelog

### 2025-12-20

Seven Cs Framework Hardening
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

### 2025-12-21

Test Driven Development Hardening
- Update Red state to be more assertive and clear about the requirement for assertion failures, not just any execution error.
- Add anti-pattern entry on the Red phase about creating tests that fail due to syntax errors or missing symbols.

Change Log Split
- Moved Change Log out of IDEAS.md into its own file
