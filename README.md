# Git Commit Rephraser

An instruction-only Agent Skill that turns verbose Git commit descriptions into concise, professional messages using Conventional Commits.

## Features

- Use Conventional Commit types such as `feat:`, `fix:`, `refactor:`, `chore:`, `docs:`, and `perf:`.
- Keep titles short, preferably under 72 characters.
- Group related changes into concise bullet points.
- Preserve the original meaning, important changes, and existing scopes.
- Return a ready-to-copy commit message in a code block.

The skill only rewrites messages. It does not execute Git commands, modify project files, or create commits.

## Install with an agent

Paste this into Codex in VS Code or another agent that supports Agent Skills:

```text
Install the Git Commit Rephraser Agent Skill by following https://raw.githubusercontent.com/cindyljp/git-commit-rephraser/main/INSTALL-WITH-AN-AGENT.md.
```

The installation instructions download the skill into a supported skill directory. For Codex, they use the personal directory when permitted and writable, or the current project's skill directory otherwise.

No Python, CLI package, or additional dependencies are required for this skill. The installing agent needs network access and permission to save the file.

## Manual installation for Codex

Copy [SKILL.md](skills/git-commit-rephraser/SKILL.md) to one of these locations:

| Scope | Destination |
| --- | --- |
| Personal: available across projects in the same environment | `~/.agents/skills/git-commit-rephraser/SKILL.md` |
| Project: available within the current project | `.agents/skills/git-commit-rephraser/SKILL.md` |

If you use WSL, SSH, or a Dev Container, install the file in the environment where Codex runs.

If the skill does not appear after installation, restart Codex or VS Code.

## Usage

In Codex, type `$git-commit-rephraser` and provide the commit description you want rewritten:

```text
$git-commit-rephraser

Help me rephrase:
Added pending transfer acknowledgement and validation.
Improved supervisor assignment.
Added transfer history and audit logging.
Updated API, frontend, and translations.
```

Example output:

```text
feat: enhance pending transfer management

- Add transfer acknowledgement and validation
- Improve supervisor assignment
- Add transfer history and audit logging
- Update API, UI, and translations
```

For a simple change, the skill may return only a title or fewer bullet points. Use the skill invocation supported by your agent when using a tool other than Codex.

## Repository layout

- [skills/git-commit-rephraser/SKILL.md](skills/git-commit-rephraser/SKILL.md): skill metadata and rewriting instructions.
- [INSTALL-WITH-AN-AGENT.md](INSTALL-WITH-AN-AGENT.md): installation instructions for an agent.
- [README.md](README.md): installation and usage guide.

## Updating an installed copy

Changes on GitHub do not automatically update a manually installed copy. Ask your agent to follow the installation instructions again, or replace your local `SKILL.md` with the latest version. Review any local customizations before replacing the file.

## Uninstall

Paste this into the agent where you installed the skill:

```text
Uninstall the git-commit-rephraser skill. Check the current project's
.agents/skills/git-commit-rephraser directory and the personal
~/.agents/skills/git-commit-rephraser directory in this environment.
Also check ~/.codex/skills/git-commit-rephraser if a previous installer
used that location.

Remove only the installed git-commit-rephraser skill directory.
If multiple copies exist, ask which copy to remove.
Do not delete the source repository or other skills.
Report the path removed.
```

To uninstall manually, delete the `git-commit-rephraser` folder from the skill directory where you installed it. For WSL, SSH, or a Dev Container, remove it in that same environment.

Restart Codex or VS Code if the skill still appears in the selector. Uninstalling a local copy does not delete this GitHub repository.

## Contributing

Open an issue to suggest an improvement, or submit a pull request with focused changes to the skill instructions.
