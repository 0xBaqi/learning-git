\# Git Worktree Notes



\## What is Git Worktree?

Git worktree lets you check out multiple branches

at the same time in different folders. You can

work on two branches simultaneously without

switching or stashing.



\## Basic Worktree Commands

\- git worktree list — list all worktrees

\- git worktree add <path> <branch> — add new worktree

\- git worktree remove <path> — remove a worktree

\- git worktree prune — clean up stale worktrees

\- git worktree move <path> <new-path> — move worktree



\## Adding a Worktree

\- git worktree add ../hotfix hotfix/urgent-fix

\- Creates new folder at ../hotfix

\- Checks out hotfix/urgent-fix branch there

\- Original folder keeps current branch



\## Common Use Cases



\### Work on Hotfix While on Feature

1\. git worktree add ../hotfix hotfix/urgent

2\. cd ../hotfix

3\. Fix the urgent issue

4\. git add . and git commit

5\. git push origin hotfix/urgent

6\. cd back to original folder

7\. Continue feature work



\### Review Colleagues Branch

1\. git worktree add ../review colleagues-branch

2\. cd ../review

3\. Test and review the code

4\. cd back to main worktree

5\. git worktree remove ../review



\### Compare Two Branches Side by Side

1\. git worktree add ../branch-b feature/b

2\. Open both folders in editor

3\. Compare implementations directly



\## Worktree Rules

\- Each branch can only be checked out once

\- Cannot check out same branch in two worktrees

\- All worktrees share the same git history

\- Commits in any worktree appear in all



\## Worktree vs Stash vs Clone



\### Worktree

\- Multiple branches simultaneously

\- Shared git history

\- Fast and lightweight



\### Stash

\- Save changes temporarily

\- Switch branch then come back

\- One branch at a time



\### Clone

\- Completely separate copy

\- Independent git history

\- More disk space used



\## Removing Worktrees

\- git worktree remove ../hotfix

\- Deletes the folder and cleans up

\- Branch still exists after removal

\- git worktree prune for stale entries



\## Tips

\- Great for urgent hotfixes during feature work

\- Use descriptive folder names

\- Remove worktrees when done

\- Run git worktree list to see all active

\- Worktrees share objects so very efficient

