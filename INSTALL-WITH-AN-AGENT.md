# Install Git Commit Rephraser

Install the instruction-only `git-commit-rephraser` Agent Skill. No Python, CLI package, or additional dependencies are required.

## Instructions for the agent

1. Download the exact UTF-8 content from:
   https://raw.githubusercontent.com/cindyljp/git-commit-rephraser/main/skills/git-commit-rephraser/SKILL.md
2. For Codex, use the personal destination `~/.agents/skills/git-commit-rephraser/SKILL.md` when it is writable and permitted. Otherwise, install in `.agents/skills/git-commit-rephraser/SKILL.md` under the current project workspace. Report whether the installation is personal or project-scoped.
3. For another agent, use its documented skill directory. Do not guess an unsupported location.
4. Create the destination directory and download using an available tool such as curl, wget, PowerShell Invoke-WebRequest, or the agent's file/network tools. Do not require Python or run downloaded code: this is a Markdown-only skill.
5. If a destination file already exists, compare it with the downloaded content. Leave an identical file unchanged. Ask before replacing different local content.
6. Respect filesystem permissions. If the personal destination is blocked, use the permitted project destination; do not change permissions or use sudo.
7. Verify that the saved file contains the YAML name `git-commit-rephraser` and the complete downloaded instructions. Report its absolute path and scope.
8. For Codex, tell the user to invoke `$git-commit-rephraser` with their commit description. If the skill does not appear, restart Codex or VS Code.

If network access is unavailable, ask the user to paste the SKILL.md contents and save them using the same destination rules.

This installation only requires the skill file. Do not claim that it was installed until the file has been saved and checked.
