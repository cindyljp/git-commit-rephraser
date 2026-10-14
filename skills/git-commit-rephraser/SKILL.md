---
name: git-commit-rephraser
description: Rephrase, shorten, and polish Git commit messages using Conventional Commits. Use when the user asks to rewrite, summarize, simplify, or improve a Git commit message or provides a verbose commit description.
---

# Git Commit Rephraser

## Purpose

Transform long or verbose Git commit messages into concise, clear, professional commit messages while preserving the important changes.

## Rules

1. Follow Conventional Commits format:
   - `feat:` New functionality
   - `fix:` Bug fixes
   - `refactor:` Code restructuring
   - `chore:` Maintenance tasks
   - `docs:` Documentation changes
   - `perf:` Performance improvements

2. Keep the title short and descriptive, preferably under 72 characters.

3. Use imperative verbs in the title, such as:
   - add
   - implement
   - enhance
   - improve
   - refactor
   - update

4. Summarize the changes into 3–5 concise bullet points when appropriate.

5. Group related changes together instead of listing every modified file or component.

6. Preserve important functionality, business logic, and technical changes.

7. Avoid unnecessary implementation details unless they are significant.

8. Do not invent features or changes not mentioned in the input.

9. Keep existing scopes where appropriate, such as `feat(assessment-history):`.

10. Use clear, professional English.

11. Do not execute Git commands, modify files, or create commits. Only rewrite the message.

## Output Format

Return only the rewritten commit message in a code block.

Example:

feat: enhance pending transfer management

- Add transfer acknowledgement and validation
- Improve supervisor assignment workflow
- Add transfer history and audit logging
- Update API, UI, and localization

## Additional Guidelines

- For simple changes, use fewer bullet points.
- Avoid repeating the commit title in the bullet points.
- Prefer "Add" instead of "Added".
- Prefer "Update" instead of "Updated".
- Avoid listing class names unless essential.
- Combine API, store, and frontend changes when they serve the same functionality.
- Preserve the original meaning.
