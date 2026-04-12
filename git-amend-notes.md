\# Git Amend Notes



\## What is Git Amend?

Git amend modifies the most recent commit.

It lets you fix the commit message, add missed

files, or remove accidentally staged files

without creating a new commit.



\## Basic Amend Commands

\- git commit --amend — amend last commit

\- git commit --amend -m "new message" — change message

\- git commit --amend --no-edit — amend without changing message



\## Amend Commit Message

1\. git commit --amend

2\. Editor opens with current message

3\. Edit the message

4\. Save and close editor

5\. Commit is updated



\## Amend to Add Missed File

1\. git add missed-file.md

2\. git commit --amend --no-edit

3\. File is added to last commit

4\. Message stays the same



\## Amend to Remove Wrong File

1\. git restore --staged wrongfile.md

2\. git commit --amend --no-edit

3\. File removed from last commit

4\. Changes kept in working directory



\## Important Warning

\- Never amend commits already pushed

\- Amend rewrites commit history

\- Force push required after amending pushed commit

\- Causes problems for teammates

\- Only amend local unpushed commits



\## When to Use Amend

\- Typo in commit message

\- Forgot to add a file

\- Added wrong file by mistake

\- Want to improve commit quality

\- Before pushing to remote



\## Amend vs Revert vs Reset

\- Amend — fix last commit before pushing

\- Revert — safely undo pushed commits

\- Reset — undo commits locally only



\## Tips

\- Check git log after amending to verify

\- Only amend the very last commit

\- Use --no-edit to keep existing message

\- Never amend shared or pushed commits

\- Amend is for cleanup before pushing

