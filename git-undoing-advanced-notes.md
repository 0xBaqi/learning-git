\# Advanced Git Undoing Notes



\## Overview

Git has many ways to undo mistakes. Choosing

the right one depends on what went wrong and

whether the commits have been pushed or not.



\## Decision Guide



\### Not Yet Committed

\- git restore <file> — discard file changes

\- git restore --staged <file> — unstage file

\- git clean -fd — remove untracked files



\### Committed But Not Pushed

\- git reset --soft HEAD\~1 — undo keep staged

\- git reset HEAD\~1 — undo keep unstaged

\- git reset --hard HEAD\~1 — undo delete changes

\- git commit --amend — fix last commit



\### Already Pushed

\- git revert <hash> — safe undo with new commit

\- Never reset pushed commits on shared branches



\## Undoing Multiple Commits



\### Reset Multiple Commits

\- git reset HEAD\~3 — undo last 3 commits

\- git reset --hard HEAD\~3 — undo and delete

\- Only for unpushed commits



\### Revert Multiple Commits

\- git revert HEAD\~3..HEAD — revert last 3

\- Creates separate revert commit for each

\- Safe for pushed commits



\## Recovering Lost Work



\### After Hard Reset

\- git reflog — find commit before reset

\- git reset --hard <hash> — go back

\- Works within 90 day reflog window



\### After Deleting Branch

\- git reflog — find last commit of branch

\- git switch -c recovered <hash>

\- Branch restored with all commits



\### After Bad Rebase

\- git reflog — find pre-rebase state

\- git reset --hard HEAD@{5}

\- Rebase completely undone



\## Undoing Specific File Changes



\### Restore File from Commit

\- git restore --source=<hash> <file>

\- File restored to that commit state

\- Change is unstaged after restore



\### Remove File from History

\- Use git filter-repo tool

\- Removes file from entire history

\- Requires force push after



\## Undoing Merges



\### Merge Not Yet Pushed

\- git reset --hard HEAD\~1

\- Removes merge commit

\- Returns to pre-merge state



\### Merge Already Pushed

\- git revert -m 1 <merge-hash>

\- Creates revert of merge commit

\- Safe for shared branches



\## Undoing Rebases

\- git reflog — find pre-rebase commit

\- git reset --hard <hash>

\- Rebase is completely undone

\- Local only, not if already pushed



\## Prevention Tips

\- git status before every add

\- git diff --staged before every commit

\- git log before every push

\- Never force push to shared branches

\- Commit often so less to lose

\- Use branches to isolate risky work



\## Emergency Commands

\- git reflog — your safety net always

\- git stash — save work before risky action

\- git branch backup — create backup branch

\- git diff HEAD — see all current changes

