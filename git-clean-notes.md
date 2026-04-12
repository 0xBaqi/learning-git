\# Git Clean Notes



\## What is Git Clean?

Git clean removes untracked files and folders

from your working directory. It helps keep your

project clean by removing files git is not

tracking.



\## Basic Clean Commands

\- git clean -n — dry run, show what would be deleted

\- git clean -f — force delete untracked files

\- git clean -fd — delete untracked files and folders

\- git clean -fx — delete untracked and ignored files

\- git clean -fX — delete only ignored files

\- git clean -i — interactive mode



\## Always Dry Run First

\- git clean -n

\- Shows what would be deleted

\- Does not actually delete anything

\- Review output before running git clean -f

\- Safety step before destructive operation



\## Clean Options Explained



\### -n or --dry-run

\- Preview what would be deleted

\- No files are actually removed

\- Always run this first



\### -f or --force

\- Required to actually delete files

\- Git requires force flag for safety

\- Deletes untracked files only



\### -d

\- Also removes untracked directories

\- Without this folders are kept

\- Combine with -f to delete folders



\### -x

\- Also removes ignored files

\- Files in .gitignore are deleted too

\- Use for completely clean state



\### -X

\- Only removes ignored files

\- Keeps untracked non ignored files

\- Good for cleaning build artifacts



\### -i or --interactive

\- Interactive mode

\- Choose what to delete step by step

\- Safer than force delete



\## Common Clean Scenarios



\### Remove Build Artifacts

\- git clean -fX

\- Removes only ignored files

\- Keeps your untracked source files

\- Good before a fresh build



\### Complete Clean State

\- git clean -fdx

\- Removes everything not committed

\- Like a fresh clone

\- Use with extreme caution



\### Remove Accidental Files

\- git clean -n — preview first

\- git clean -f — delete untracked files

\- Removes files created by mistake



\### Clean After Merge Conflict

\- git clean -fd

\- Remove conflict leftover files

\- Start fresh after messy merge



\## Git Clean vs Git Restore

\- git clean — removes untracked files

\- git restore — restores tracked files

\- Use both together for fully clean state

\- git restore . then git clean -fd



\## Protecting Files

\- Add to .gitignore to prevent tracking

\- Ignored files need -x flag to clean

\- Important files should be committed



\## Tips

\- Always run git clean -n before git clean -f

\- Cannot undo git clean easily

\- Deleted files go to trash sometimes

\- Use git stash for tracked file changes

\- Combine with git restore for full reset

\- Be very careful with git clean -fdx

