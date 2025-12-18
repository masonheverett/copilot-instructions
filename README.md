# copilot-instructions

**A small repository for storing and evolving personal GitHub Copilot instruction templates and operational guidelines.** ✨

## Purpose 🔧
This repo collects short, actionable instruction documents that I use across projects (policies, templates, and review checklists). Treat these as living artifacts: they are small, focused, and intended to be copied or referenced from other repositories or team guidelines.

## What’s Included 📚
A small reference of key instruction files:

```
.github/
├─ copilot-instructions.md       # Base Copilot instructions & repo-level assistant policies
└─ instructions/
   ├─ tdd.instructions.md        # Test-Driven Development (Red/Green/Refactor)
   ├─ bugfixing.instructions.md  # Bug-fixing methodology (diagnose → tests → implement → validate → document)
   └─ sevencs.instructions.md    # The Seven Cs quality checklist
```

## How to Use 💡
- Copy or reference one or more files into a project’s contributing docs or policy folder.
- Follow the *mandatory* rules where noted (e.g., the TDD loop and bug-fixing phases).
- Use the Seven Cs as a review pass to catch correctness, completeness, and chokepoints.

## Contributing ✅
- Add or improve instruction files via pull requests. Keep changes small, focused, and well-documented.
- In PR descriptions, explain the motivation and show a short example or use-case if helpful.

## License
See the repository `LICENSE` for license details.
