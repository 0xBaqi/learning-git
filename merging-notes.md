\# Merging in Git



\## What is merging?

Merging combines two branches into one.



\## Types of merges

\- Fast-forward merge — no merge commit, clean history

\- No-fast-forward merge — creates a merge commit

\- Merge conflict — happens when two branches edit the same line



\## Commands

\- git merge <branch> — merge branch into current

\- git merge --no-ff <branch> — force a merge commit

\- git merge --abort — cancel a merge

\- git status — check for conflicts



\## Resolving conflicts

1\. Open the conflicted file

2\. Look for <<<<<<< and >>>>>>> markers

3\. Keep the code you want

4\. Remove the markers

5\. git add <file>

6\. git commit -m "resolve merge conflict"

