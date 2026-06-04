# AGENTS.md

## Git Workflow

- When the user asks to push changes, commit the relevant project changes and run `git push` automatically.
- Use the existing `origin` remote unless the user explicitly asks to change it.
- Current remote: `https://github.com/alexanyseo-png/vercel.git`.
- Do not ask the user to open GitHub in a browser if local authentication already works.
- Use locally configured Git credentials only: Git Credential Manager, a stored Personal Access Token, or SSH keys.
- Never write GitHub tokens, passwords, API keys, or other secrets into repository files.
- If authentication fails, tell the user to configure one of these local auth methods:
  - `git credential-manager github login --pat`
  - SSH remote: `git@github.com:alexanyseo-png/vercel.git`

## Commit Rules

- Check `git status --short --branch` before committing.
- Stage only files related to the user's request.
- Use short, direct commit messages in English.
- After a successful push, report the branch and GitHub repository URL.
