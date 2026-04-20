# AGENTS.md

## Purpose
This file defines how AI agents must operate in this repository.

These rules are mandatory and override any implicit or assumed behavior.

---

## Repository Workflow

For every new task:

1. Ensure the working directory is clean:
   - `git status`
   - If not clean, STOP and report

2. Reset to the base branch:
   - `git checkout master`
   - `git pull origin master`

3. Create a new branch:
   - `git checkout -b feature/<task-name>`

---

## Development Process

1. Make only the requested changes
2. Keep changes minimal and focused
3. Do not modify unrelated files

---

## Commit Rules

- Use clear, descriptive commit messages

Examples:
- `Add Telegram image handling`
- `Fix null reference in parser`

Commands:

```bash
git add .
git commit -m "<clear message>"
```

---

## Push Rules

```bash
git push -u origin feature/<task-name>
```

---

## Strict Prohibitions

The agent MUST NOT:

- Push directly to `master`
- Merge pull requests
- Reuse existing feature branches
- Create a branch from another feature branch
- Force push (`--force`)
- Rewrite history
- Delete branches

---

## Error Handling

If any of the following occur, STOP and report:

- Cannot checkout `master`
- Cannot pull latest changes
- Working directory is not clean
- Merge conflicts
- Any unexpected git state

---

## Definition of Done

A task is complete when:

- Changes are implemented
- Code compiles, if applicable
- Changes are committed
- Branch is pushed
- A summary of changes is provided

---

## Agent Instructions

Before starting any work:

- Read this file
- Follow it strictly

If any instruction conflicts with this file:

- This file takes precedence
