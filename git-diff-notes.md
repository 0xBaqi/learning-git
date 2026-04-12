\# Git Diff Notes



\## Basic Diff

\- git diff — show unstaged changes

\- git diff --staged — show staged changes

\- git diff HEAD — show all changes since last commit



\## Comparing Branches

\- git diff main feature/name — compare two branches

\- git diff main..feature/name — same as above

\- git diff main...feature/name — changes since branch was created



\## Comparing Commits

\- git diff <hash1> <hash2> — compare two commits

\- git diff HEAD\~1 HEAD — compare last two commits

\- git diff HEAD\~3 — compare with 3 commits ago



\## Comparing Files

\- git diff <file> — show changes in a specific file

\- git diff --staged <file> — show staged changes in a file

\- git diff main feature/name <file> — compare file between branches



\## Diff Options

\- git diff --stat — show summary of changes

\- git diff --name-only — show only changed file names

\- git diff --word-diff — show word level changes

\- git diff --color-words — highlight changed words



\## Reading a Diff

\- Lines starting with + are additions

\- Lines starting with - are deletions

\- Lines starting with @@ show location in file

\- Lines without + or - are unchanged context

