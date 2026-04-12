\# Git Push Notes



\## What is Git Push?

Git push uploads your local commits to a remote

repository like GitHub. It shares your work with

others and backs up your code online.



\## Basic Push Commands

\- git push — push to tracked remote branch

\- git push origin main — push to specific branch

\- git push -u origin main — push and set upstream

\- git push --all — push all branches

\- git push --tags — push all tags

\- git push --force-with-lease — safe force push



\## Setting Upstream

\- git push -u origin main

\- Only needed on first push of a branch

\- After setting, just use git push

\- git branch -vv — see upstream tracking info



\## Force Push

\- git push --force — overwrite remote history

\- git push --force-with-lease — safer force push

\- Force with lease checks remote before pushing

\- Never force push to shared branches

\- Only use on your own feature branches



\## Push a New Branch

1\. git switch -c feature/name

2\. Make changes and commit

3\. git push -u origin feature/name

4\. Branch appears on GitHub



\## Delete Remote Branch

\- git push origin --delete feature/name

\- Removes branch from GitHub

\- Local branch still exists

\- git branch -d feature/name to delete locally



\## Push Tags

\- git push origin v1.0.0 — push specific tag

\- git push origin --tags — push all tags

\- git push --follow-tags — push commits and tags



\## Common Push Errors



\### Rejected Push

\- Remote has changes you don't have locally

\- git pull first then push again



\### No Upstream Branch

\- git push -u origin branch-name

\- Sets upstream and pushes



\### Permission Denied

\- Check your GitHub credentials

\- Regenerate personal access token

\- Verify remote URL is correct



\## Push Best Practices

\- Push at end of every work session

\- Never force push to main

\- Always pull before pushing

\- Push feature branches not main directly

\- Delete remote branches after merging



\## Tips

\- git push -u sets upstream permanently

\- After upstream is set just use git push

\- Check git status before pushing

\- Review git log before pushing

\- Push often to back up your work

