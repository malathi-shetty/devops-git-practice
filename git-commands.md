# Git Commands Reference

## Setup & Config

### git config
- Sets user configuration like name and email
- Example:
  git config --global user.name "Your Name"
  git config --global user.email "your@email.com"

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
