\# Git Fetch Notes



\## What is Git Fetch?

Git fetch downloads changes from a remote repo

without merging them into your local branch.

It lets you see what others have done before

deciding to integrate their changes.



\## Basic Fetch Commands

\- git fetch — fetch from default remote

\- git fetch origin — fetch from origin

\- git fetch --all — fetch from all remotes

\- git fetch origin main — fetch specific branch

\- git fetch --prune — remove deleted remote branches



\## Fetch vs Pull

\- git fetch — download only, no merge

\- git pull — download and merge automatically

\- git pull = git fetch + git merge

\- Fetch is safer, pull is faster



\## Workflow with Fetch



\### Check Before Merging

1\. git fetch origin

2\. git log HEAD..origin/main --oneline

3\. See what commits are incoming

4\. git diff HEAD origin/main

5\. Review the changes

6\. git merge origin/main

7\. Merge when ready



\### Update Remote Tracking Branches

1\. git fetch --all

2\. git branch -r — see all remote branches

3\. git switch -c feature origin/feature

4\. Work on remote branch locally



\## Fetch and Prune

\- git fetch --prune — clean up stale branches

\- Removes remote tracking branches that no longer exist

\- Keeps your local repo clean

\- Good habit to run regularly



\## Viewing Fetched Changes

\- git log HEAD..origin/main — see incoming commits

\- git diff HEAD origin/main — see incoming changes

\- git branch -r — see all remote branches

\- git status — shows if branch is behind remote



\## When to Use Fetch

\- Before starting work each day

\- Before merging a branch

\- When you want to see remote changes safely

\- When working with multiple remotes

\- Before rebasing onto main



\## Multiple Remotes

\- git remote add upstream <url>

\- git fetch upstream

\- git fetch --all

\- git merge upstream/main

\- Useful when working with forks



\## Tips

\- Fetch often to stay up to date

\- Always fetch before rebasing

\- Use fetch to preview incoming changes

\- Combine with git log to review changes

\- Fetch is always safe, it never changes local code

