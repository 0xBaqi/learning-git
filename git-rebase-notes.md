\# Git Rebase Notes



\## What is Rebase?

Rebase moves or combines commits from one branch onto another.

It rewrites commit history for a cleaner, linear history.



\## Basic Rebase

\- git rebase main — rebase current branch onto main

\- git rebase --abort — cancel a rebase

\- git rebase --continue — continue after resolving conflict

\- git rebase --skip — skip current commit



\## Interactive Rebase

\- git rebase -i HEAD\~3 — interactive rebase last 3 commits



\### Interactive Commands

\- pick — keep commit as is

\- reword — keep commit but edit message

\- edit — keep commit but pause to amend

\- squash — combine with previous commit

\- fixup — combine with previous, discard message

\- drop — delete commit completely



\## Common Use Cases



\### Clean up commits before merging

1\. git rebase -i HEAD\~5

2\. squash small commits together

3\. reword commit messages

4\. drop unnecessary commits



\### Update feature branch with main

1\. git switch feature/name

2\. git rebase main

3\. Resolve any conflicts

4\. git push --force-with-lease origin feature/name



\## Rebase vs Merge

\- Rebase — linear history, cleaner log

\- Merge — preserves branch history, safer



\## Golden Rule

Never rebase commits that have been pushed

to a shared branch. Only rebase local commits.



\## Conflict Resolution

1\. Fix the conflict in the file

2\. git add <file>

3\. git rebase --continue

4\. Repeat until rebase is complete

