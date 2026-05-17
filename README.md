## GitHub Commands

# Git Commands Cheat Sheet

## Setup
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

## Starting Out
git init                  # Initialize a new repo
git clone <url>           # Clone a remote repo

## Daily Workflow
git status                # Check what's changed
git add .                 # Stage all changes
git add <file>            # Stage a specific file
git commit -m "message"   # Commit staged changes
git push                  # Push to remote
git pull                  # Pull latest changes

## Branching
git branch                # List branches
git branch <name>         # Create a branch
git checkout <name>       # Switch to a branch
git checkout -b <name>    # Create + switch in one step
git merge <branch>        # Merge branch into current
git branch -d <name>      # Delete a branch

## Undoing Things
git restore <file>        # Discard unstaged changes
git reset HEAD <file>     # Unstage a file
git reset --soft HEAD~1   # Undo last commit (keep changes)
git reset --hard HEAD~1   # Undo last commit (discard changes)

## Viewing History
git log                   # Full commit history
git log --oneline         # Compact history
git diff                  # See unstaged changes

## Remote
git remote -v                        # View remotes
git remote add origin <url>          # Add remote
git push -u origin main              # Push & set upstream
git push origin --delete <branch>    # Delete remote branch

## Stashing
git stash                 # Save uncommitted changes temporarily
git stash pop             # Restore stashed changes