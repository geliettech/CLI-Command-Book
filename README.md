# Cmdbook

> A curated, no-nonsense cheat sheet for everyday **Git**, **npm**, **pnpm**, and **Yarn** commands.

Stop googling the same command for the tenth time. Cmdbook collects the commands developers actually use day-to-day, organized by what you're trying to *do* rather than buried in an alphabetical list.

📌 Currently a README-based reference. A searchable website version is planned — see [Roadmap](#roadmap).

---

## Table of Contents

- [Git](#git)
  - [Setup & Config](#setup--config)
  - [Starting a Project](#starting-a-project)
  - [Staging & Committing](#staging--committing)
  - [Branching](#branching)
  - [Syncing with Remotes](#syncing-with-remotes)
  - [Undoing Things](#undoing-things)
  - [Stashing](#stashing)
  - [Inspecting History](#inspecting-history)
  - [Tags](#tags)
- [npm](#npm)
- [pnpm](#pnpm)
- [Yarn](#yarn)
- [Package Manager Command Comparison](#package-manager-command-comparison)
- [Contributing](#contributing)
- [Roadmap](#roadmap)
- [License](#license)

---

## Git

### Setup & Config

| Command | Description |
|---|---|
| `git config --global user.name "Name"` | Set your global username |
| `git config --global user.email "email"` | Set your global email |
| `git config --list` | View all config settings |
| `git init` | Initialize a new repo in the current folder |
| `git clone <url>` | Clone a remote repo locally |

### Starting a Project

| Command | Description |
|---|---|
| `git status` | Show changed/staged/untracked files |
| `git add <file>` | Stage a specific file |
| `git add .` | Stage all changes in current directory |
| `git add -p` | Interactively stage chunks of changes |

### Staging & Committing

| Command | Description |
|---|---|
| `git commit -m "message"` | Commit staged changes with a message |
| `git commit -am "message"` | Stage tracked files + commit in one step |
| `git commit --amend` | Edit the previous commit (message or content) |
| `git commit --amend --no-edit` | Add staged changes to the last commit without changing the message |

### Branching

| Command | Description |
|---|---|
| `git branch` | List local branches |
| `git branch <name>` | Create a new branch |
| `git checkout <branch>` | Switch to a branch |
| `git checkout -b <branch>` | Create and switch to a new branch |
| `git switch <branch>` | Switch branches (modern alternative to checkout) |
| `git switch -c <branch>` | Create and switch to a new branch |
| `git branch -d <branch>` | Delete a branch (safe) |
| `git branch -D <branch>` | Force delete a branch |
| `git merge <branch>` | Merge a branch into the current one |
| `git rebase <branch>` | Reapply commits on top of another branch |

### Syncing with Remotes

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

### Undoing Things

| Command | Description |
|---|---|
| `git restore <file>` | Discard unstaged changes to a file |
| `git restore --staged <file>` | Unstage a file (keep changes) |
| `git reset --soft HEAD~1` | Undo last commit, keep changes staged |
| `git reset --mixed HEAD~1` | Undo last commit, keep changes unstaged |
| `git reset --hard HEAD~1` | Undo last commit, discard changes entirely |
| `git revert <commit>` | Create a new commit that undoes a previous one |
| `git clean -fd` | Remove untracked files and directories |

### Stashing

| Command | Description |
|---|---|
| `git stash` | Save uncommitted changes for later |
| `git stash list` | List all stashes |
| `git stash pop` | Apply and remove the latest stash |
| `git stash apply` | Apply the latest stash without removing it |
| `git stash drop` | Delete the latest stash |

### Inspecting History

| Command | Description |
|---|---|
| `git log` | View commit history |
| `git log --oneline --graph --all` | Compact visual history of all branches |
| `git diff` | Show unstaged changes |
| `git diff --staged` | Show staged changes |
| `git blame <file>` | Show who last changed each line |
| `git show <commit>` | Show details of a specific commit |

### Tags

| Command | Description |
|---|---|
| `git tag` | List tags |
| `git tag v1.0.0` | Create a lightweight tag |
| `git tag -a v1.0.0 -m "message"` | Create an annotated tag |
| `git push origin v1.0.0` | Push a specific tag |
| `git push origin --tags` | Push all tags |

---

## npm

| Command | Description |
|---|---|
| `npm init` | Create a new `package.json` (interactive) |
| `npm init -y` | Create `package.json` with defaults |
| `npm install` | Install all dependencies from `package.json` |
| `npm install <pkg>` | Install and add a package to dependencies |
| `npm install <pkg> --save-dev` | Install as a dev dependency |
| `npm install -g <pkg>` | Install a package globally |
| `npm uninstall <pkg>` | Remove a package |
| `npm update` | Update packages to latest allowed versions |
| `npm run <script>` | Run a script defined in `package.json` |
| `npm ls` | List installed packages |
| `npm outdated` | Check for outdated packages |
| `npm audit` | Check for known vulnerabilities |
| `npm audit fix` | Automatically fix vulnerabilities where possible |
| `npm cache clean --force` | Clear the npm cache |
| `npm ci` | Clean install from `package-lock.json` (faster, for CI) |

---

## pnpm

| Command | Description |
|---|---|
| `pnpm init` | Create a new `package.json` |
| `pnpm install` | Install all dependencies |
| `pnpm add <pkg>` | Add a package to dependencies |
| `pnpm add -D <pkg>` | Add a dev dependency |
| `pnpm add -g <pkg>` | Install a package globally |
| `pnpm remove <pkg>` | Remove a package |
| `pnpm update` | Update dependencies |
| `pnpm run <script>` | Run a script |
| `pnpm list` | List installed packages |
| `pnpm outdated` | Check for outdated packages |
| `pnpm audit` | Check for vulnerabilities |
| `pnpm store prune` | Clean unused packages from the store |
| `pnpm -r <command>` | Run a command across all packages in a monorepo |

---

## Yarn

| Command | Description |
|---|---|
| `yarn init` | Create a new `package.json` |
| `yarn` / `yarn install` | Install all dependencies |
| `yarn add <pkg>` | Add a package to dependencies |
| `yarn add <pkg> --dev` | Add a dev dependency |
| `yarn global add <pkg>` | Install a package globally |
| `yarn remove <pkg>` | Remove a package |
| `yarn upgrade` | Update dependencies |
| `yarn run <script>` | Run a script |
| `yarn list` | List installed packages |
| `yarn outdated` | Check for outdated packages |
| `yarn audit` | Check for vulnerabilities |
| `yarn cache clean` | Clear the yarn cache |

---

## Package Manager Command Comparison

A quick side-by-side for switching between tools:

| Action | npm | pnpm | Yarn |
|---|---|---|---|
| Install all deps | `npm install` | `pnpm install` | `yarn` |
| Add a package | `npm install <pkg>` | `pnpm add <pkg>` | `yarn add <pkg>` |
| Add dev dependency | `npm install <pkg> -D` | `pnpm add <pkg> -D` | `yarn add <pkg> --dev` |
| Remove a package | `npm uninstall <pkg>` | `pnpm remove <pkg>` | `yarn remove <pkg>` |
| Install globally | `npm install -g <pkg>` | `pnpm add -g <pkg>` | `yarn global add <pkg>` |
| Run a script | `npm run <script>` | `pnpm run <script>` | `yarn run <script>` |
| Update deps | `npm update` | `pnpm update` | `yarn upgrade` |

---

## Contributing

Contributions are welcome! If you know a useful command that's missing, or a better explanation for an existing one:

1. Fork the repo
2. Add your command(s) to the relevant table, keeping the format consistent
3. Open a pull request with a short description of what you added

Please keep entries concise — one line per command, focused on the most common use case.

---

## Roadmap

- [ ] Expand coverage (e.g. `git worktree`, `npm workspaces`, `pnpm` monorepo commands)
- [ ] Add short usage examples for trickier commands
- [ ] Build a searchable website version (static site, likely with client-side search)
- [ ] Add categorized tags/filters (beginner, advanced, dangerous, etc.)

## License

[MIT](LICENSE)
