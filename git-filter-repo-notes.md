\# Git Filter Repo Notes



\## What is Git Filter Repo?

Git filter-repo is a tool for rewriting git

history. It can remove files, rename paths,

and clean up repository history. It replaces

the older git filter-branch command.



\## Why Rewrite History

\- Remove accidentally committed secrets

\- Remove large files from history

\- Rename files or folders in history

\- Split one repo into multiple repos

\- Merge multiple repos into one

\- Remove sensitive personal information



\## Installing Git Filter Repo

\- pip install git-filter-repo

\- Or download from github.com/newren/git-filter-repo

\- Verify with git filter-repo --version



\## Basic Filter Repo Commands

\- git filter-repo --path <file> --invert-paths

\- git filter-repo --path src/ — keep only src

\- git filter-repo --to-subdirectory-filter <folder>

\- git filter-repo --path-rename old:new



\## Remove a File from History

1\. git filter-repo --path secret.env --invert-paths

2\. File removed from entire git history

3\. git remote add origin <url>

4\. git push origin --force --all

5\. git push origin --force --tags



\## Remove Folder from History

1\. git filter-repo --path node\_modules/ --invert-paths

2\. Entire folder removed from all commits

3\. Repository size reduces significantly



\## Keep Only Specific Folder

1\. git filter-repo --path src/

2\. Only src folder kept in history

3\. Used to split monorepo into separate repos



\## Rename Path in History

1\. git filter-repo --path-rename old-name:new-name

2\. All commits updated with new path

3\. History looks like new name always existed



\## Remove Sensitive Data



\### Step by Step

1\. Identify the sensitive file or data

2\. Add file to .gitignore immediately

3\. git filter-repo --path <file> --invert-paths

4\. Verify file is gone from history

5\. Force push to remote

6\. Immediately revoke any exposed secrets

7\. Generate new secrets



\## Important Warnings

\- Filter repo rewrites entire history

\- All commit hashes change after running

\- Teammates must re-clone the repository

\- Coordinate with team before running

\- Cannot be undone after force push

\- Always work on a backup copy first



\## Before Running Filter Repo

\- Create backup of repository

\- Notify all teammates

\- Plan for re-cloning after

\- Revoke exposed secrets immediately

\- Test on backup first



\## After Running Filter Repo

\- git remote add origin <url>

\- git push origin --force --all

\- git push origin --force --tags

\- All contributors must re-clone

\- Old clones will have conflicts



\## Tips

\- Only use when absolutely necessary

\- Always back up repo before running

\- Communicate clearly with team

\- Immediately revoke exposed credentials

\- Prevention is better than cure

\- Use .gitignore from day one to avoid need

