# Test-Driven Development (TDD) Instructions

**Purpose**
Define the required TDD discipline for non-trivial changes. Use this when implementing new behavior or fixing bugs.

---

## When to Use TDD

Use TDD by default for:
- Bug fixes and regressions
- New or changed behavior
- Edge cases, parsing, validation, transformations

TDD may be skipped for:
- Formatting-only or mechanical refactors
- Documentation-only changes

If uncertain, **use TDD**.

---

## The TDD Loop (Mandatory)

Follow this sequence strictly:

1. **Red** — Write a test that executes and fails due to an assertion
2. **Green** — Implement the minimal fix
3. **Refactor** — Improve structure without changing behavior

Do not skip or reorder steps.

---

## Red Phase Rule (Critical)

**Red means assertion failure, not execution errors.**

- Create minimal stubs so tests run and **fail on assertions**, not on syntax errors or missing symbols.
- Error-first tests are acceptable **only** when existence itself is the requirement (e.g., public API). Move to assertion-based tests immediately after.

---

## Test Writing Rules

- Test names must describe **observable behavior**
- Each test should have **one reason to fail**
- Tests must fail for the *right reason*
- Target **public behavior**, not internal implementation
- Use the **narrowest test** that proves the behavior (unit > integration > contract/e2e)
- Tests must be deterministic, fast, and have clear assertions
- Avoid conditionals, loops, or complex logic in tests

If a test is hard to write, treat that as **design feedback**, not a test problem.

---

## Implementation Rules (Green)

- Implement only what is needed to pass the failing test
- Do not refactor or add unrelated behavior
- Prefer clarity over cleverness
- A passing test must fail if the implementation is wrong

---

## Refactor Rules

- Refactor only after tests pass
- No behavior changes
- All tests must remain passing
- Refactor tests with the same care as production code
- Validate with `make check`

---

## Test Execution Discipline

- During development: run the **smallest relevant test set** frequently
- After a small unit of work: run the relevant module or package tests
- Before completion: run the **full suite** (`make check`)

Optimize for fast feedback, not batch debugging.

---

## Anti-Patterns (Never Do)

- Write tests after the fix
- Let tests error accidentally
- Mix refactors with behavior changes
- Over-mock instead of using real collaborators
- Write tests that pass even if the implementation is removed
- Skip tests because the change is “small”
- Treat import, naming, or wiring errors as a valid Red state

---

## Final Rule

If behavior changes and no failing **assertion-based** test justified the change, **TDD was not followed**.
