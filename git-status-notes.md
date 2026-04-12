\# Git Status Notes



\## What is Git Status?

Git status shows the current state of your

working directory and staging area. It tells

you what has changed, what is staged, and

what is untracked.



\## Basic Status Commands

\- git status — full status output

\- git status -s — short compact output

\- git status -b — show branch information

\- git status -sb — short output with branch



\## Reading Status Output



\### Clean Working Tree

\- nothing to commit, working tree clean

\- No changes since last commit



\### Untracked Files

\- Files git is not tracking yet

\- Need git add to start tracking

\- Shown in red



\### Changes Not Staged

\- Tracked files that have been modified

\- Need git add to stage them

\- Shown in red



\### Changes to be Committed

\- Files staged and ready to commit

\- Need git commit to save them

\- Shown in green



\## Short Status Output

\- git status -s

\- ?? — untracked file

\- A — new file staged

\- M — modified file

\- MM — modified staged and unstaged

\- D — deleted file



\## Common Status Messages



\### Nothing to Commit

\- Working tree is clean

\- Everything is committed



\### Untracked Files Present

\- New files not yet tracked

\- Use git add to track them



\### Changes Not Staged

\- Modified files not yet staged

\- Use git add to stage them



\### Branch Ahead of Remote

\- You have commits not pushed yet

\- Use git push to upload them



\### Branch Behind Remote

\- Remote has commits you dont have

\- Use git pull to download them



\### Branch Diverged

\- Both local and remote have new commits

\- Need to pull and resolve before pushing



\## Status in Workflow

1\. git status — check before starting work

2\. Make changes to files

3\. git status — see what changed

4\. git add . — stage changes

5\. git status — confirm staging

6\. git commit -m "message" — commit

7\. git status — confirm clean tree

8\. git push — push to remote



\## Tips

\- Run git status constantly

\- Check status before every add and commit

\- Check status after every operation

\- Status never changes your code

\- Use git status -s for quick overview

\- Read status messages carefully

