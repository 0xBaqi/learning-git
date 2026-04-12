\# Undoing Things in Git



\## Unstage a file

\- git restore --staged <file>



\## Discard changes in working directory

\- git restore <file>



\## Undo last commit (keep changes)

\- git reset HEAD\~1



\## Undo last commit (delete changes)

\- git reset --hard HEAD\~1



\## Undo a pushed commit safely

\- git revert <hash>



\## Stash changes temporarily

\- git stash

\- git stash pop



\## Delete untracked files

\- git clean -fd



\## Notes

\- reset is for local commits only

\- revert is safe for shared/pushed commits

\- always check git status before undoing anything

