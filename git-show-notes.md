\# Git Show Notes



\## What is Git Show?

Git show displays detailed information about

a specific git object like a commit, tag, or blob.

Most commonly used to inspect a specific commit.



\## Basic Show Commands

\- git show — show latest commit details

\- git show <hash> — show specific commit

\- git show HEAD — show current commit

\- git show HEAD\~1 — show previous commit

\- git show HEAD\~3 — show 3 commits ago

\- git show <tag> — show tagged commit



\## Show Output

\- Commit hash

\- Author name and email

\- Date and time

\- Commit message

\- Diff of changes made



\## Show Options

\- git show --stat — show file change summary

\- git show --name-only — show only changed filenames

\- git show --name-status — show filenames with status

\- git show -p — show full patch diff

\- git show --no-patch — show without diff



\## Show Specific File in Commit

\- git show <hash>:<file> — show file at that commit

\- git show HEAD:README.md — show README at HEAD

\- git show HEAD\~1:src/index.js — show file one commit ago



\## Show Branch Tips

\- git show main — show latest commit on main

\- git show origin/main — show latest on remote main

\- git show feature/name — show latest on feature branch



\## Show Tags

\- git show v1.0 — show annotated tag details

\- git show v1.0 --stat — show tag with file changes



\## Common Use Cases



\### Review a Specific Commit

1\. git log --oneline — find the commit hash

2\. git show <hash> — see full details

3\. Understand what changed and why



\### Check File at Previous State

1\. git log --oneline -- <file>

2\. Find commit when file was correct

3\. git show <hash>:<file>

4\. View file content at that point



\### Verify a Tag

1\. git tag — list all tags

2\. git show v1.0

3\. See tag message and commit details



\### Review Before Reverting

1\. git log --oneline — find bad commit

2\. git show <hash> — review what it changed

3\. git revert <hash> — revert if needed



\## Show vs Log vs Diff

\- git show — details of one specific commit

\- git log — list of many commits

\- git diff — differences between states



\## Tips

\- Use git show after git log to inspect commits

\- Use git show HEAD to review last commit

\- Copy hash from git log then use git show

\- Use --stat for quick file change overview

\- Use git show <hash>:<file> to recover old content

