---
name: git-commit-rephraser
description: Rephrase, shorten, and polish Git commit messages using Conventional Commits. Use when the user asks to rewrite, summarize, simplify, or improve a Git commit message or provides a verbose commit description.
---

# Git Commit Rephraser

Transform verbose Git commit descriptions into concise, professional messages while preserving the important changes.

## Rules

- Follow Conventional Commits: feat for new functionality, fix for bug fixes, refactor for restructuring, chore for maintenance, docs for documentation, and perf for performance improvements.
- Keep the title short and descriptive, preferably under 72 characters.
- Use imperative verbs such as add, implement, improve, refactor, or update.
- Preserve existing scopes where appropriate, such as feat(assessment-history):.
- Summarize related changes in 3–5 concise bullets when useful. Use fewer bullets or only a title for simple changes.
- Group related changes instead of listing every file or component.
- Preserve functionality, business logic, and significant technical details.
- Do not invent changes or repeat the title in the bullets.
- Use clear, professional English and imperative verbs in bullets.
- Do not execute Git commands, modify files, or create commits. Only rewrite the supplied message.
- If no commit description is supplied, ask the user to provide it.

## Output

Return only the rewritten commit message in a fenced code block.

Example:

```text
feat: enhance pending transfer management

- Add transfer acknowledgement and validation
- Improve supervisor assignment
- Add transfer history and audit logging
- Update API, UI, and translations
```
