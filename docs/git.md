# Git Commands

Part of [Cmdbook](../README.md).

## Table of Contents

- [What is Git Commands?](#what-is-git-commands?)
- [Setup & Config](#setup--config)
- [Starting a Project](#starting-a-project)
- [Staging & Committing](#staging--committing)
- [Branching](#branching)
- [Syncing with Remotes](#syncing-with-remotes)
- [Undoing Things](#undoing-things)
- [Stashing](#stashing)
- [Inspecting History](#inspecting-history)
- [Tags](#tags)

---

## What is Git Commands?
....

## Setup & Config

| Command | Description |
|---|---|
| `git config --global user.name "Name"` | Set your global username |
| `git config --global user.email "email"` | Set your global email |
| `git config --list` | View all config settings |
| `git init` | Initialize a new repo in the current folder |
| `git clone <url>` | Clone a remote repo locally |

## Starting a Project

| Command | Description |
|---|---|
| `git status` | Show changed/staged/untracked files |
| `git add <file>` | Stage a specific file |
| `git add .` | Stage all changes in current directory |
| `git add -p` | Interactively stage chunks of changes |

## Staging & Committing

| Command | Description |
|---|---|
| `git commit -m "message"` | Commit staged changes with a message |
| `git commit -am "message"` | Stage tracked files + commit in one step |
| `git commit --amend` | Edit the previous commit (message or content) |
| `git commit --amend --no-edit` | Add staged changes to the last commit without changing the message |

## Branching

| Command | Description |
|---|---|
| `git branch` | List local branches |
| `git branch <name>` | Create a new branch |
| `git checkout <branch>` | Switch to a branch |
| `git checkout -b <branch>` | Create and switch to a new branch |
| `git switch <branch>` | Switch branches (modern alternative to checkout) |
| `git switch -c <branch>` | Create and switch to a new branch |
| `git branch -d <branch>` | Delete a branch locally (safe) |
| `git push origin --delete <branch>` | Delete a branch Remotely (safe) |
| `git branch -D <branch>` | Force delete a branch |
| `git merge <branch>` | Merge a branch into the current one |
| `git rebase <branch>` | Reapply commits on top of another branch |
| `git push origin <branch>` | Push and set upstream tracking of a branch |

## Syncing with Remotes

| Command | Description |
|---|---|
| `git remote -v` | List remotes |
| `git remote add origin <url>` | Add a remote |
| `git fetch` | Download changes without merging |
| `git pull` | Fetch + merge from remote |
| `git pull --rebase` | Fetch + rebase instead of merge |
| `git push` | Push commits to remote |
| `git push -u origin <branch>` | Push and set upstream tracking |
| `git push --force-with-lease` | Safer force push (checks for remote changes first) |

## Undoing Things

| Command | Description |
|---|---|
| `git restore <file>` | Discard unstaged changes to a file |
| `git restore --staged <file>` | Unstage a file (keep changes) |
| `git reset --soft HEAD~1` | Undo last commit, keep changes staged |
| `git reset --mixed HEAD~1` | Undo last commit, keep changes unstaged |
| `git reset --hard HEAD~1` | Undo last commit, discard changes entirely |
| `git revert <commit id>` | Create a new commit that undoes a previous one |
| `git clean -fd` | Remove untracked files and directories |
| `git cherry-pick <commit-hash>` | choose a commit from one branch and apply it into another |

## Stashing

| Command | Description |
|---|---|
| `git stash` | Save uncommitted changes for later |
| `git stash list` | List all stashes |
| `git stash pop` | Apply and remove the latest stash |
| `git stash apply` | Apply the latest stash without removing it |
| `git stash drop` | Delete the latest stash |

## Inspecting History

| Command | Description |
|---|---|
| `git log` | View commit history |
| `git log --oneline --graph --all` | Compact visual history of all branches |
| `git diff` | Show unstaged changes |
| `git diff --staged` | Show staged changes |
| `git blame <file>` | Show who last changed each line |
| `git show <commit>` | Show details of a specific commit |

## Tags

| Command | Description |
|---|---|
| `git tag` | List tags |
| `git tag v1.0.0` | Create a lightweight tag |
| `git tag -a v1.0.0 -m "message"` | Create an annotated tag |
| `git push origin v1.0.0` | Push a specific tag |
| `git push origin --tags` | Push all tags |
| `git tag -d v1.0.0` | delete tag locally |
| `git push origin -d v1.0.0` | delete tag remotely |
