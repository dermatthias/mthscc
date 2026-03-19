# CLAUDE.md

This file provides guidance for AI assistants (e.g., Claude Code) working in this repository.

## Repository Status

This repository is in its **initial state** — no source code has been committed yet. This document captures known conventions and workflows based on the repository configuration.

## Git Workflow

### Branch Naming

Feature branches follow the pattern:
```
claude/<description>-<SESSION_ID>
```

Example: `claude/add-claude-documentation-9HARV`

### Remote

- **Remote name**: `origin`
- **URL**: `http://local_proxy@127.0.0.1:43565/git/dermatthias/mthscc`

### Pushing Changes

Always use the `-u` flag when pushing a new branch:
```bash
git push -u origin <branch-name>
```

Retry on network failures with exponential backoff (2s, 4s, 8s, 16s — up to 4 retries).

### Commit Messages

Write clear, descriptive commit messages:
- Use the imperative mood: "Add feature" not "Added feature"
- Keep the subject line under 72 characters
- Explain *why* in the body if the change is non-obvious

## Development Guidelines for AI Assistants

### General Principles

- Read files before modifying them
- Prefer editing existing files over creating new ones
- Keep changes focused — only implement what was asked
- Do not add unnecessary comments, docstrings, or type annotations to unchanged code
- Avoid over-engineering; solve the problem at hand

### Security

- Never commit secrets, credentials, or `.env` files
- Validate input at system boundaries (user input, external APIs)
- Avoid common vulnerabilities: SQL injection, XSS, command injection

### Before Pushing

1. Ensure all tests pass (once a test suite exists)
2. Verify the branch name matches the required `claude/` pattern
3. Confirm changes are scoped to the current task

## Project Structure

> To be filled in as the project is developed.

```
mthscc/
├── CLAUDE.md          # This file
└── ...                # Source files to be added
```

## Testing

> Document test commands here once a test suite is established.

```bash
# Example (update with actual commands):
# npm test
# pytest
# cargo test
# go test ./...
```

## Build & Dev

> Document build and dev server commands here once established.

```bash
# Example (update with actual commands):
# npm run dev
# npm run build
```

## Conventions

> Update this section as code conventions are established:

- Language/runtime: TBD
- Formatting/linting: TBD
- Code style: TBD
