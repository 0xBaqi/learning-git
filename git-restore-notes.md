\# Git Restore Notes



\## What is Git Restore?

Git restore is used to undo changes in your

working directory or staging area. It replaces

the older git checkout and git reset for

discarding changes.



\## Basic Restore Commands

\- git restore <file> — discard changes in working directory

\- git restore . — discard all changes in working directory

\- git restore --staged <file> — unstage a file

\- git restore --staged . — unstage all files

\- git restore --source=HEAD\~1 <file> — restore from previous commit



\## Restore Working Directory

\- git restore <file>

\- Discards all uncommitted changes in file

\- Reverts file to last committed state

\- Cannot be undone easily

\- Use with caution



\## Restore Staging Area

\- git restore --staged <file>

\- Moves file from staging back to working directory

\- Changes are kept but unstaged

\- Safe to use anytime



\## Restore from Specific Commit

\- git restore --source=HEAD\~1 <file>

\- Restores file from one commit ago

\- git restore --source=<hash> <file>

\- Restores file from specific commit

\- Change is unstaged after restore



\## Restore vs Reset vs Revert



\### git restore

\- Discards changes in working directory

\- Unstages files from staging area

\- Does not affect commit history



\### git reset

\- Moves HEAD to different commit

\- Can unstage files

\- Affects commit history



\### git revert

\- Creates new commit that undoes changes

\- Safe for pushed commits

\- Preserves commit history



\## Common Restore Scenarios



\### Accidentally Modified Wrong File

1\. git status — confirm which file

2\. git restore <file>

3\. File is back to last committed state



\### Staged Wrong File

1\. git status — see staged files

2\. git restore --staged <file>

3\. File is unstaged but changes kept



\### Want Old Version of File

1\. git log --oneline — find commit hash

2\. git restore --source=<hash> <file>

3\. File restored to that version

4\. git add and commit to save it



\## Tips

\- Always check git status before restoring

\- git restore working directory is permanent

\- git restore --staged is always safe

\- Use git diff to review changes before restoring

\- Cannot restore if file was never committed

\- Use git stash as safer alternative

