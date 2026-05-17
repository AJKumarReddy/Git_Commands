# Git_Commands Cheat Sheet

## Setup
git config --global user.name "Your Name"
  → Sets your name that will appear on all your commits

git config --global user.email "you@example.com"
  → Sets your email linked to your commits (use your GitHub email)

## Starting Out
git init
  → Creates a brand new Git repository in the current folder.
     A hidden .git folder is created to track all changes.

git clone <url>
  → Downloads a remote repository to your local machine,
     including all files, branches, and history.

## Daily Workflow
git status
  → Shows which files are modified, staged, or untracked.
     Your go-to command to see what's going on.

git add .
  → Stages ALL changed files, making them ready to commit.

git add <file>
  → Stages only a specific file for the next commit.

git commit -m "message"
  → Saves a snapshot of your staged changes with a description.
     This is how you record progress in your project history.

git push
  → Uploads your local commits to the remote repository (e.g. GitHub).

git pull
  → Downloads and merges the latest changes from the remote repo
     into your current branch.

## Branching
git branch
  → Lists all local branches. The current branch is marked with *.

git branch <name>
  → Creates a new branch but does NOT switch to it.

git checkout <name>
  → Switches to an existing branch.

git checkout -b <name>
  → Creates a new branch AND switches to it immediately.

git merge <branch>
  → Merges the specified branch into your current branch.
     Used to combine work from different branches.

git branch -d <name>
  → Deletes a local branch (only if it has been merged).

## Undoing Things
git restore <file>
  → Discards all unstaged changes in a file, reverting it
     to the last committed version.

git reset HEAD <file>
  → Unstages a file without losing the changes you made.

git reset --soft HEAD~1
  → Undoes the last commit but keeps your changes staged.
     Useful if you committed too early.

git reset --hard HEAD~1
  → Completely undoes the last commit AND discards all changes.
     WARNING: This cannot be undone.

## Viewing History
git log
  → Shows the full commit history with author, date, and message.

git log --oneline
  → Shows a compact, one-line summary of each commit.
     Great for a quick overview.

git diff
  → Shows the exact line-by-line changes that are NOT yet staged.

## Remote
git remote -v
  → Lists all connected remote repositories and their URLs.

git remote add origin <url>
  → Connects your local repo to a remote repository (e.g. on GitHub).

git push -u origin main
  → Pushes your local main branch to GitHub and sets it as
     the default upstream for future git push commands.

git push origin --delete <branch>
  → Deletes a branch from the remote repository on GitHub.

## Stashing
git stash
  → Temporarily saves your uncommitted changes so you can
     switch branches or pull without losing your work.

git stash pop
  → Restores the most recently stashed changes back into
     your working directory.