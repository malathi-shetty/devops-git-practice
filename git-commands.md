# Git Commands Reference

Note: Updated from GitHub CLI for Day 22 task

## Setup & Config

### git config
- Sets user configuration like name and email
- Example:
  - git config --global user.name "Your Name"
  - git config --global user.email "your@email.com"

### git config --list
- Displays all Git configuration values
- Example:
  git config --global --list

---

## Basic Workflow

### git init
- Initializes a new Git repository
- Example:
  git init

### git add
- Adds files to the staging area
- Example:
  git add git-commands.md
  git add .

### git commit
- Saves staged changes as a snapshot with a message
- Example:
  git commit -m "Initial commit"

---

## Viewing Changes

### git status
- Shows the current state of the working directory
- Lists which files are modified, staged, or untracked
- Example:
  git status

### git log
- Shows full commit history (hash, author, date, message)
- Example:
  git log

### git diff
- Shows changes between working directory and staging area
- Example:
  git diff

### git log --oneline
- Shows compact commit history (one line per commit)
- Example:
  git log --oneline

---

## Undo / Restore

### git restore
- Discards changes in the working directory
- Example:
  git restore git-commands.md
  
---

Note: Updated from GitHub UI for Day 23 task

## Branching Commands

### `git branch`
- Lists all local branches
- Example:
  git branch

### `git branch -a`
- Lists all branches (local + remote)
- Example:
  git branch -a

### `git branch -r`
- Lists only remote branches
- Example:
  git branch -r

### `git branch --show-current`
- Shows only the current branch name
- Example:
  git branch --show-current

### `git branch <branch-name>`
- Creates a new branch
- Example:
  git branch feature-1

---

### git switch
- Switches to a branch (modern way)
- Example:
  git switch feature-1

### git checkout
- Switches branches (older method)
- Example:
  git checkout feature-1

---

### git switch -c
- Creates and switches to a new branch
- Example:
  git switch -c feature-2

### git checkout -b
- Creates and switches to a new branch (older method)
- Example:
  git checkout -b feature-3

---

### git branch -d
- Deletes a branch safely
- Example:
  git branch -d feature-2

### git branch -D
- Force deletes a branch
- Example:
  git branch -D feature-2

---

## Switching & Navigation

### git switch master
- Switches back to main/master branch
- Example:
  git switch master

### git switch -
- Switches to the previous branch
- Example:
  git switch -

### git branch
- Shows current branch
- Example:
  git branch

---

## View History (Branch Verification)

### git log --oneline
- Shows compact commit history (one line per commit)
- Example:
  git log --oneline

### `git log --oneline --decorate --graph`
- Shows commit graph with branch pointers
- Example:
  git log --oneline --decorate --graph

### `git log <branch1>..<branch2>`
- Shows commits present in second branch but not in first
- Example:
  git log master..feature-1

---

## Remote Repository Commands

### git remote add origin
- Adds a remote repository
- Example:
  git remote add origin git@github.com:username/repo.git

### git remote -v
- Displays remote repository URLs
- Example:
  git remote -v

### `git push origin <branch-name>`
- Pushes a branch to GitHub
- Example:
  git push origin feature-1

### `git push -u origin <branch-name>`
- Pushes branch and sets upstream tracking
- Example:
  git push -u origin feature-1

---

## Pull & Fetch

### `git pull origin <branch-name>`
- Fetches and merges changes from remote
- Example:
  git pull origin master

### git fetch origin
- Downloads changes without merging
- Example:
  git fetch origin

### git fetch --all
- Fetches updates from all remotes
- Example:
  git fetch --all

---

## Upstream (Fork Workflow)

### git remote add upstream
- Adds original repository as upstream
- Example:
  git remote add upstream git@github.com:original/repo.git

### git fetch upstream
- Fetches changes from upstream
- Example:
  git fetch upstream

### git merge upstream/master
- Merges upstream changes into current branch
- Example:
  git merge upstream/master

---

## Practice Commands (Day 23)

### echo
- Creates or updates a file
- Example:
  echo "feature work" >> file.txt

### git add .
- Stages all changes
- Example:
  git add .

### git commit -m
- Commits changes with a message
- Example:
  git commit -m "Added feature work"

### git log master..feature-1
- Shows commits in feature branch but not in master
- Example:
  git log master..feature-1

---

## Important Notes

- Branches only differ when new commits are made  
- If all branches point to the same commit → no real branching has happened
- git pull = git fetch + git merge

---

## Tip

- git switch is the modern alternative to git checkout  
- git checkout is older and does multiple things (switch + restore files)  
