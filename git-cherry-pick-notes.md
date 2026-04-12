\# Git Cherry Pick Notes



\## What is Cherry Pick?

Cherry pick applies a specific commit from one

branch to another. It lets you pick individual

commits without merging the whole branch.



\## Basic Cherry Pick

\- git cherry-pick <hash> — apply a specific commit

\- git cherry-pick --abort — cancel cherry pick

\- git cherry-pick --continue — continue after conflict

\- git cherry-pick --skip — skip current commit



\## Finding the Commit Hash

\- git log --oneline — find the hash you need

\- git log --oneline --all — search all branches

\- git log --oneline feature/name — search specific branch



\## Cherry Pick Multiple Commits

\- git cherry-pick <hash1> <hash2> — pick multiple commits

\- git cherry-pick <hash1>..<hash2> — pick a range of commits



\## Cherry Pick Without Committing

\- git cherry-pick -n <hash> — apply changes but dont commit

\- Lets you modify changes before committing

\- Then git add . and git commit -m "message"



\## Common Use Cases



\### Bug fix on wrong branch

1\. Fix bug on feature branch

2\. Realize fix is needed on main too

3\. git log --oneline — copy the fix commit hash

4\. git switch main

5\. git cherry-pick <hash>



\### Partial feature release

1\. Feature branch has 10 commits

2\. Only 3 commits are ready for release

3\. Cherry pick those 3 commits to main



\### Recover lost commits

1\. Accidentally deleted a branch

2\. git reflog — find the commit hash

3\. git cherry-pick <hash> — recover the commit



\## Cherry Pick vs Merge

\- Cherry pick — specific commits only

\- Merge — entire branch history

\- Cherry pick — creates new commit with same changes

\- Merge — preserves original commit



\## Notes

\- Cherry pick creates a new commit with same changes

\- Original commit still exists on source branch

\- Can cause duplicate commits if branch is merged later

\- Use sparingly, prefer merge or rebase when possible

