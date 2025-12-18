# Bug Fixing Methodology (Mandatory for Bugs)

Apply this process whenever fixing a **bug or regression**.

---

## Phase 1: Diagnose

Before writing code or tests:

1. Confirm it is a bug (not bad data or a missing feature)
2. Reproduce with exact inputs
3. Document expected vs actual behavior
4. Trace data flow: Input → Various Internal Layers → Output
5. Identify the precise root cause (files and lines)

---

## Phase 2: Test Creation (Before Implementation)

- Tests must fail with the current bug
- Choose the narrowest effective test

Test types:
- Unit tests
- Integration tests
- Contract/E2E tests

Guidelines:
- Deterministic tests
- Clear assertions
- Reference issue IDs when applicable

---

## Phase 3: Implementation

1. Run baseline validation:
   - `make check`

2. Apply minimal, targeted changes:
   - Make the smallest change that fixes the root cause
   - Run tests frequently
   - Follow TDD principles

3. Validate:
   - `make check` passes
   - No regressions
   - Manual verification if appropriate

---

## Phase 4: Documentation

- Summarize the fix clearly
- Recommend documentation updates:
  - Specs/design notes during development
  - Bug fix records for regressions

---

## Anti-Patterns (Never Do)

- Fix without diagnosis
- Mask data issues with code
- Treat missing features as bugs
- Fix without tests
- Write tests after fixing
- Skip documentation
- Skip `make check` before and after changes
