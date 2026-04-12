\# Git Checkout Notes



\## What is Git Checkout?

Git checkout is an older versatile command that

switches branches, restores files, and navigates

commit history. Newer git versions split its

functionality into git switch and git restore.



\## Basic Checkout Commands

\- git checkout <branch> — switch to branch

\- git checkout -b <branch> — create and switch

\- git checkout <hash> — go to specific commit

\- git checkout <hash> <file> — restore file from commit

\- git checkout -- <file> — discard file changes



\## Checkout vs Switch vs Restore



\### git checkout <branch>

\- Same as git switch <branch>

\- Switches to existing branch



\### git checkout -b <branch>

\- Same as git switch -c <branch>

\- Creates and switches to new branch



\### git checkout -- <file>

\- Same as git restore <file>

\- Discards changes in working directory



\### git checkout <hash> <file>

\- Same as git restore --source=<hash> <file>

\- Restores file from specific commit



\## Detached HEAD with Checkout

\- git checkout <hash>

\- Puts repo in detached HEAD state

\- You are not on any branch

\- Good for exploring old code

\- git checkout -b new-branch to save work

\- git switch main to go back



\## Common Checkout Uses



\### Switch Branch

\- git checkout main

\- git checkout feature/login

\- git checkout -b feature/new



\### Restore Old File Version

1\. git log --oneline -- <file>

2\. Find commit with correct version

3\. git checkout <hash> -- <file>

4\. File restored to that version

5\. git add and commit to save



\### Explore Old Commit

1\. git log --oneline

2\. git checkout <hash>

3\. Look around at old code

4\. git checkout main to return



\## Checkout Remote Branch

\- git fetch origin

\- git checkout origin/feature/name

\- git checkout -b feature/name origin/feature/name

\- Creates local branch tracking remote



\## Why Switch and Restore Exist

\- git checkout does too many things

\- Confusing for beginners

\- git switch — only for branches

\- git restore — only for files

\- Clearer intent and less mistakes

\- git checkout still works and always will



\## Tips

\- Prefer git switch for branch operations

\- Prefer git restore for file operations

\- Use git checkout for compatibility

\- Know both old and new syntax

\- git checkout -- file discards changes permanently

\- Always check git status after checkout

