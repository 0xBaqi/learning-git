\# Git Maintenance Notes



\## What is Git Maintenance?

Git maintenance keeps your repository healthy

and performing well. Over time repos can get

large and slow without regular maintenance.



\## Basic Maintenance Commands

\- git gc — garbage collection

\- git gc --aggressive — thorough garbage collection

\- git prune — remove unreachable objects

\- git fsck — check repository integrity

\- git maintenance start — enable automatic maintenance

\- git maintenance stop — disable automatic maintenance

\- git maintenance run — run maintenance manually



\## Git Garbage Collection

\- git gc

\- Compresses loose objects into pack files

\- Removes unreachable objects

\- Runs automatically sometimes

\- Manual run for better performance



\## Git Prune

\- git prune

\- Removes objects not reachable from any branch

\- Usually run as part of git gc

\- git remote prune origin — remove stale remote branches

\- git fetch --prune — fetch and prune together



\## Repository Health Check

\- git fsck

\- Checks integrity of objects

\- Finds corrupt or missing objects

\- Reports dangling commits and blobs

\- Good for diagnosing repo problems



\## Automatic Maintenance

\- git maintenance start

\- Sets up scheduled maintenance tasks

\- Runs in background automatically

\- Keeps repo healthy without manual work

\- git maintenance stop to disable



\## Maintenance Tasks

\- prefetch — prefetch remote objects

\- gc — garbage collection

\- commit-graph — update commit graph

\- loose-objects — pack loose objects

\- incremental-repack — repack efficiently



\## Signs Your Repo Needs Maintenance

\- Git commands feel slow

\- Repository size is very large

\- Many loose objects warning

\- Clone takes very long

\- Fetch is slow



\## Reducing Repository Size



\### Remove Large Files from History

\- Use git filter-repo tool

\- Removes files from entire history

\- Reduces repository size significantly

\- Requires force push after



\### Remove Old Branches

\- git branch -d old-branch

\- git push origin --delete old-branch

\- git fetch --prune

\- Keeps repo clean and small



\### Shallow Clone for Large Repos

\- git clone --depth 1 <url>

\- Only downloads recent history

\- Much smaller download size



\## Tips

\- Run git gc periodically on large repos

\- Use git fetch --prune regularly

\- Delete merged branches promptly

\- Avoid committing large binary files

\- Use git lfs for large file storage

\- Check repo size with git count-objects -vH

