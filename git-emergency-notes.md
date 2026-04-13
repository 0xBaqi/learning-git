\# Git Emergency Notes



\## Common Git Emergencies and Fixes



\## Emergency 1 - Committed to Wrong Branch

\### Situation

\- Made commits on main instead of feature branch



\### Fix

1\. git log --oneline — copy commit hashes

2\. git switch -c feature/correct-branch

3\. git switch main

4\. git reset --hard origin/main

5\. Commits now on correct branch only



\## Emergency 2 - Accidentally Deleted Branch

\### Situation

\- Deleted branch with unmerged commits



\### Fix

1\. git reflog — find last commit of branch

2\. git switch -c recovered-branch <hash>

3\. All commits are back



\## Emergency 3 - Force Pushed Wrong Branch

\### Situation

\- Force pushed and overwrote teammates work



\### Fix

1\. Ask teammate for their local branch hash

2\. git push origin <hash>:main --force

3\. Remote restored to their version

4\. Apologize to teammate



\## Emergency 4 - Committed Secret or Password

\### Situation

\- Accidentally committed API key or password



\### Fix

1\. Immediately revoke the exposed secret

2\. Generate new secret

3\. git filter-repo --path <file> --invert-paths

4\. git push origin --force --all

5\. Update secret in secure location

6\. Add file to .gitignore



\## Emergency 5 - Merge Gone Wrong

\### Situation

\- Merge created conflicts everywhere



\### Fix

1\. git merge --abort — if still in progress

2\. git reset --hard HEAD\~1 — if just merged

3\. git revert -m 1 <merge-hash> — if pushed



\## Emergency 6 - Rebase Gone Wrong

\### Situation

\- Rebase created mess of conflicts



\### Fix

1\. git rebase --abort — if still in progress

2\. git reflog — find pre-rebase state

3\. git reset --hard HEAD@{n} — go back

4\. Rebase completely undone



\## Emergency 7 - Lost All Uncommitted Work

\### Situation

\- Did git reset --hard and lost all changes



\### Fix

1\. git reflog — look for recent changes

2\. git fsck --lost-found — find dangling blobs

3\. Check .git/lost-found/other/ folder

4\. Recovery not always possible



\## Emergency 8 - Pushed to Wrong Remote

\### Situation

\- Pushed sensitive code to wrong repository



\### Fix

1\. Contact repo owner immediately

2\. Ask them to delete the repo or branch

3\. Revoke any secrets in pushed code

4\. Review what was exposed



\## Emergency 9 - Git Repo Corrupted

\### Situation

\- Git commands returning object errors



\### Fix

1\. git fsck — check for corruption

2\. git gc — attempt cleanup

3\. Clone fresh copy from remote

4\. Copy any local only files over



\## Emergency 10 - Accidentally Ran Git Init in Wrong Folder

\### Situation

\- Created git repo in wrong place



\### Fix

1\. Remove-Item -Recurse -Force .git

2\. Deletes the git repo

3\. Folder returns to normal

4\. Run git init in correct folder



\## Prevention Checklist

\- Check git status before every operation

\- Check current branch before committing

\- Never force push to shared branches

\- Always use .gitignore from day one

\- Back up important work before risky operations

\- Read error messages carefully before acting

\- When in doubt git stash first



\## Emergency Contacts

\- git reflog — always check this first

\- git status — understand current state

\- git log --oneline — see recent history

\- git diff — see current changes

\- Stack Overflow — community help

\- Git documentation — git-scm.com

