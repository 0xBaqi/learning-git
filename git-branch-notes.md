\# Git Branch Notes



\## What is a Branch?

A branch is an independent line of development.

It lets you work on features or fixes without

affecting the main codebase. Branches are

lightweight and fast to create in git.



\## Basic Branch Commands

\- git branch — list all local branches

\- git branch -r — list remote branches

\- git branch -a — list all branches

\- git branch <name> — create a new branch

\- git branch -d <name> — delete merged branch

\- git branch -D <name> — force delete branch

\- git branch -m <old> <new> — rename a branch

\- git branch -vv — show tracking information



\## Creating Branches

\- git branch feature/login — create branch

\- git switch -c feature/login — create and switch

\- git checkout -b feature/login — older syntax



\## Switching Branches

\- git switch main — switch to main

\- git switch feature/login — switch to feature

\- git checkout main — older syntax



\## Deleting Branches



\### Local Branch

\- git branch -d feature/login — safe delete

\- git branch -D feature/login — force delete

\- Safe delete fails if branch not merged



\### Remote Branch

\- git push origin --delete feature/login

\- Removes branch from GitHub



\## Branch Naming Conventions

\- feature/feature-name — new features

\- fix/bug-description — bug fixes

\- docs/what-you-updated — documentation

\- hotfix/critical-fix — urgent fixes

\- release/v1.0.0 — release branches

\- chore/task-name — maintenance tasks



\## Viewing Branch Info

\- git branch — current branch marked with star

\- git branch -v — show last commit per branch

\- git branch -vv — show tracking and ahead behind

\- git branch --merged — branches merged into current

\- git branch --no-merged — branches not yet merged



\## Branch and Remote Tracking

\- git push -u origin feature/name — set upstream

\- git branch --set-upstream-to=origin/main main

\- git branch -vv — see tracking info



\## Common Branch Workflows



\### Feature Branch

1\. git switch main

2\. git pull

3\. git switch -c feature/name

4\. Make changes and commit

5\. git push -u origin feature/name

6\. Open pull request

7\. Merge and delete branch



\### Hotfix Branch

1\. git switch main

2\. git switch -c hotfix/critical-bug

3\. Fix the bug and commit

4\. git push origin hotfix/critical-bug

5\. Open pull request

6\. Merge immediately



\## Tips

\- Always branch from updated main

\- Keep branch names short and descriptive

\- Delete branches after merging

\- Use git branch --merged to find stale branches

\- Never work directly on main

\- One feature per branch

