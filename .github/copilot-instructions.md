# `<Project Name Here>` – Copilot Instructions

## Scope
These instructions apply to all Copilot interactions in this repository.
They must be followed unless explicitly overridden by the user.

---

## Core Principles (Operational)

- Be **correct and concrete**. Prefer executable steps over explanation.
- Keep changes **small, focused, and reviewable**.
- Surface **assumptions, risks, and unknowns** before proceeding.

Do not provide meta commentary about quality or principles unless asked.

---

## Project Reality

- Primary language: <Language>
- Formatting and linting are enforced via Makefile targets.
- Canonical commands (when present):
  - `make format`
  - `make lint`
  - `make check`
  - `make test`
  - `<make commands here>`

Before proposing or running commands:
- Inspect `<insert files here>` if unsure.
- Do not invent commands or assume global installs.

---

## Commands and Execution

- Prefer Makefile targets when available.
- If no suitable target exists, say so explicitly before suggesting alternatives.
- Activate the project’s virtual environment using the repository-standard mechanism (`<command here>`).
- Do not run background processes unless explicitly requested.
- Do not truncate command output unless asked.

---

## Code Changes

- Prefer test-driven development (TDD) for non-trivial changes.
- Do not mix refactors with behavior changes.
- Use `make format` for mechanical-only changes.
- Use `make lint` to check for style issues.
- Run relevant tests before and after substantive changes.
- Allow the user to manage commits unless asked to do so.

---

# Further Instructions

- When asked to use the bugfixing workflow, follow the steps in `.github/instructions/bugfixing.instructions.md`.
- When asked to perform a Seven Cs evaluation, follow the steps in `.github/instructions/sevencs.instructions.md`.
- When asked to perform test-driven development (TDD), follow the steps in `.github/instructions/tdd.instructions.md`.
