\# Git Merge Notes



\## What is Git Merge?

Git merge combines two branches into one.

It integrates changes from one branch into

another creating a unified history.



\## Basic Merge Commands

\- git merge <branch> — merge branch into current

\- git merge --no-ff <branch> — force merge commit

\- git merge --squash <branch> — squash all commits

\- git merge --abort — cancel a merge in progress

\- git merge --continue — continue after conflict



\## Types of Merges



\### Fast Forward Merge

\- Happens when no new commits on target branch

\- Simply moves branch pointer forward

\- No merge commit created

\- Clean linear history



\### Three Way Merge

\- Happens when both branches have new commits

\- Creates a new merge commit

\- Preserves branch history

\- Shows where branches diverged



\### Squash Merge

\- Combines all branch commits into one

\- Adds as single commit to target

\- Clean history on main branch

\- Loses individual commit details



\## Merge Workflow

1\. git switch main — go to target branch

2\. git pull — update target branch

3\. git merge feature/name — merge feature in

4\. Resolve conflicts if any

5\. git push — push merged result



\## No Fast Forward Merge

\- git merge --no-ff feature/name

\- Always creates merge commit

\- Preserves branch history

\- Makes it clear where feature was added

\- Recommended for feature branches



\## Merge Conflicts

\- Happen when same lines edited in both branches

\- Git cannot auto resolve these

\- Must be resolved manually

\- Look for conflict markers in files



\## Resolving Conflicts

1\. git status — see conflicted files

2\. Open each conflicted file

3\. Find conflict markers

4\. Choose which code to keep

5\. Remove all conflict markers

6\. git add <file>

7\. git commit -m "resolve merge conflict"



\## Aborting a Merge

\- git merge --abort

\- Cancels merge in progress

\- Returns to state before merge

\- Use when conflicts are too complex



\## After Merging

\- git branch -d feature/name — delete local branch

\- git push origin --delete feature/name — delete remote

\- git push — push merged changes

\- git log --oneline --graph — verify merge



\## Merge vs Rebase

\- Merge — preserves history, creates merge commit

\- Rebase — rewrites history, linear result

\- Merge is safer for shared branches

\- Rebase is cleaner for local branches



\## Tips

\- Always pull before merging

\- Test after merging before pushing

\- Delete branches after successful merge

\- Use no fast forward for feature branches

\- Never rebase after merging to shared branch

\- Communicate with team before merging large features

