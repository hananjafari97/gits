# Git

## Basic commands
<div style="background:#f6f8fa;padding:12px;border-radius:8px;">

- Set name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```
Set your global Git username.
Set your global Git email.

- Initialize a new repository or clone an existing one:

```bash
git init
git clone <repo-url>
```
Create a new local Git repository.
Copy a remote repository to your machine.

- Check status and prepare commits:

```bash
git status
git add <file>
git add .
git commit -m "commit message"
```
Show the current status of the working directory and staging area.
Stage a specific file for commit.
Stage all changes in the working directory.
Create a commit with the provided message.

</div>

## Branches and merging

- Create and switch branches:

```bash
git branch new-feature
git checkout new-feature
# or the modern command:
git switch new-feature
```
Create a new branch named `new-feature`.
Switch to the `new-feature` branch.
Switch to the `new-feature` branch using the newer command.

- Create and switch to a new branch in one line:

```bash
git checkout -b fix/typo
```
Create a new branch `fix/typo` and switch to it immediately.

- Merge and rebase:

```bash
git checkout main
git merge new-feature
# or for a cleaner history:
git rebase main
```
Switch to the `main` branch.
Merge the `new-feature` branch into `main`.
Reapply commits on top of `main` for a linear history.

## Working with remotes

- Add a remote:

```bash
git remote add origin <url>
```
Add a new remote named `origin` that points to the given URL.

- Fetch and integrate changes:

```bash
git fetch
git pull
```
Download changes from the remote without merging.
Fetch and merge remote changes into the current branch.

- Push changes:

```bash
git push -u origin <branch>
```
Upload local commits to the remote `origin` and set upstream tracking for the branch.

## Restore, stash, and cleanup

- Restore a file to the state at HEAD:

```bash
git restore <file>
```
Restore the specified file to the version in HEAD.

- Temporarily save changes:

```bash
git stash
# view stashes
git stash list
# apply and remove the latest stash
git stash pop
```
Save local changes temporarily and clean the working directory.
List all saved stashes.
Apply the most recent stash and remove it from the stash list.

- Remove untracked files (preview first):

```bash
git clean -n
git clean -f
```
Show which untracked files would be removed without deleting them.
Remove untracked files from the working directory.

