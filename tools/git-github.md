# Git & GitHub Reference

![GitHub](../assets/images/github-banner.png)

This page is a command reference. Initial Git installation and authentication are documented in the [Windows 11 + WSL setup](../windows-11/README.md).

## Everyday workflow

```bash
git status
git add .
git commit -m "Describe the change"
git push
```

Update the current branch:

```bash
git pull
```

Clone a repository:

```bash
git clone https://github.com/OWNER/REPOSITORY.git
```

## Repository setup

Initialize a repository:

```bash
git init
```

Add a remote:

```bash
git remote add origin https://github.com/OWNER/REPOSITORY.git
```

View remotes:

```bash
git remote -v
```

Push the first `main` branch:

```bash
git push -u origin main
```

## Branches

List branches:

```bash
git branch
```

Create and switch to a branch:

```bash
git switch -c branch-name
```

Switch branches:

```bash
git switch branch-name
```

Rename the current branch:

```bash
git branch -m new-name
```

Delete a local branch:

```bash
git branch -d branch-name
```

Delete a remote branch:

```bash
git push origin --delete branch-name
```

## Inspect changes and history

```bash
git diff
```

```bash
git log --oneline --graph --decorate --all
```

```bash
git show
```

## Undo common local changes

Restore an unstaged file:

```bash
git restore path/to/file
```

Unstage a file while keeping the working copy:

```bash
git restore --staged path/to/file
```

Temporarily save work:

```bash
git stash
```

Restore the most recent stash:

```bash
git stash pop
```

## Cleanup — use carefully

Preview untracked files that would be removed:

```bash
git clean -n
```

Remove untracked files only after reviewing the preview:

```bash
git clean -f
```

Do not use aggressive cleanup options unless you understand exactly what will be deleted.

## Tags

```bash
git tag
```

```bash
git tag -a v1.0.0 -m "Release v1.0.0"
```

```bash
git push origin v1.0.0
```

## Useful configuration

```bash
git config --global --list
```

```bash
git config --global init.defaultBranch main
```

```bash
git config --global core.editor "code --wait"
```

## Authentication

The preferred setup in this repository is **Git Credential Manager from Git for Windows**, shared with Git inside WSL.

Check the configured helper:

```bash
git config --global --get credential.helper
```

GitHub Personal Access Tokens remain available for workflows that explicitly require one:

https://github.com/settings/tokens

Never commit passwords, tokens, private keys, or `.env` secrets.
