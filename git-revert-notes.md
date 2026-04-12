\# Git Revert Notes



\## What is Git Revert?

Git revert creates a new commit that undoes

the changes from a previous commit. It is the

safe way to undo changes that have already

been pushed to a shared branch.



\## Basic Revert Commands

\- git revert <hash> — revert a specific commit

\- git revert HEAD — revert the latest commit

\- git revert HEAD\~1 — revert previous commit

\- git revert --no-commit <hash> — revert without committing

\- git revert --abort — cancel revert in progress



\## How Revert Works

\- Finds the changes in the specified commit

\- Creates opposite changes to undo them

\- Commits the opposite changes as new commit

\- Original commit stays in history

\- Safe for shared and pushed branches



\## Revert vs Reset



\### Git Revert

\- Creates new commit to undo changes

\- Preserves full commit history

\- Safe for pushed and shared branches

\- Recommended for public branches



\### Git Reset

\- Moves HEAD back to previous commit

\- Rewrites commit history

\- Dangerous for pushed branches

\- Only use on local unpushed commits



\## Revert Workflow

1\. git log --oneline — find bad commit hash

2\. git show <hash> — review what it changed

3\. git revert <hash> — create reverting commit

4\. Editor opens for commit message

5\. Save and close editor

6\. git push — push the revert commit



\## Revert Without Committing

\- git revert --no-commit <hash>

\- Applies reverse changes to staging area

\- Does not create commit immediately

\- Lets you combine multiple reverts

\- git commit -m "revert multiple commits" when done



\## Reverting Multiple Commits

\- git revert <hash1> <hash2> — revert two commits

\- git revert <hash1>..<hash3> — revert a range

\- Each creates its own revert commit

\- Or use --no-commit then commit once



\## Revert Merge Commits

\- git revert -m 1 <merge-hash>

\- -m 1 specifies mainline parent

\- More complex than reverting regular commits

\- Consider carefully before reverting merges



\## Common Revert Scenarios



\### Bad Feature Deployed

1\. git log --oneline — find feature commit

2\. git revert <hash>

3\. git push

4\. Bad feature is removed safely



\### Wrong File Committed

1\. git log --oneline -- <file>

2\. Find commit that added wrong file

3\. git revert <hash>

4\. File changes are undone



\### Breaking Change in Last Commit

1\. git revert HEAD

2\. Commit message editor open

3\. Save and close

4\. git push



\## Tips

\- Always use revert for pushed commits

\- Review commit with git show before reverting

\- Test after reverting to confirm fix

\- Write clear revert commit messages

\- Revert does not delete original commit

\- Use reset only for local unpushed commits

