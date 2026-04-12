\# Git Reset Notes



\## Three Types of Reset



\### Soft Reset

\- git reset --soft HEAD\~1

\- Undoes last commit

\- Keeps changes staged

\- Safe to use



\### Mixed Reset (default)

\- git reset HEAD\~1

\- Undoes last commit

\- Keeps changes but unstages them

\- Safe to use



\### Hard Reset

\- git reset --hard HEAD\~1

\- Undoes last commit

\- Deletes all changes permanently

\- Use with caution



\## Reset to Specific Commit

\- git reset --soft <hash>

\- git reset --mixed <hash>

\- git reset --hard <hash>



\## Reset a Single File

\- git reset HEAD <file> — unstage a file

\- git restore --staged <file> — same as above



\## When to Use Reset

\- Soft — want to redo commit message

\- Mixed — want to reorganize changes

\- Hard — want to completely start over



\## Important Notes

\- Never reset commits that have been pushed

\- Use git revert for pushed commits instead

\- git reflog can help recover from bad resets

\- Always check git log before resetting



\## Recovery

\- git reflog — find lost commits

\- git reset --hard <hash> — go back to specific point

