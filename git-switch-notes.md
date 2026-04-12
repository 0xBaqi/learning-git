\# Git Switch Notes



\## What is Git Switch?

Git switch is a modern command for switching

between branches. It was introduced in git 2.23

as a cleaner alternative to git checkout for

branch operations.



\## Basic Switch Commands

\- git switch <branch> — switch to existing branch

\- git switch -c <branch> — create and switch to new branch

\- git switch -C <branch> — create or reset and switch

\- git switch - — switch to previous branch

\- git switch --detach <hash> — switch to specific commit



\## Switch vs Checkout

\- git switch — only for branch operations

\- git checkout — does branches and file operations

\- git switch is clearer and more focused

\- git checkout is older but still works

\- Both are valid to use



\## Creating and Switching

\- git switch -c feature/login

\- Creates branch and switches in one step

\- Equivalent to git checkout -b feature/login

\- Most common way to start new feature



\## Switching to Previous Branch

\- git switch -

\- Goes back to last branch you were on

\- Works like cd - in terminal

\- Useful for quick context switching



\## Switch with Uncommitted Changes

\- git switch fails if changes conflict

\- git stash first then switch

\- Or git switch --force to discard changes

\- Or commit changes before switching



\## Detached HEAD State

\- git switch --detach <hash>

\- Checks out specific commit not a branch

\- Good for exploring old code

\- Create branch to save work here

\- git switch -c new-branch to save work



\## Common Switch Workflows



\### Start New Feature

1\. git switch main

2\. git pull

3\. git switch -c feature/name

4\. Start working



\### Quick Context Switch

1\. Working on feature branch

2\. git stash

3\. git switch main

4\. Fix urgent issue

5\. git switch -

6\. git stash pop

7\. Continue feature work



\### Review Colleagues Branch

1\. git fetch origin

2\. git switch colleagues-branch

3\. Review and test code

4\. git switch - to go back



\## Error Messages



\### Branch Not Found

\- git switch feature/name

\- error: pathspec did not match

\- Branch does not exist locally

\- git fetch then try again



\### Uncommitted Changes

\- Cannot switch with conflicting changes

\- git stash or commit first

\- Then switch successfully



\## Tips

\- Use git switch for all branch operations

\- Use git switch - to bounce between branches

\- Always pull after switching to main

\- Check git status after switching

\- Use git switch -c for new features always

