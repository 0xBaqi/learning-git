\# Git Productivity Notes



\## Git Aliases for Speed

\- git config --global alias.st status

\- git config --global alias.co checkout

\- git config --global alias.br branch

\- git config --global alias.lg "log --oneline --graph"

\- git config --global alias.sw switch

\- git config --global alias.cm "commit -m"

\- git config --global alias.undo "reset HEAD\~1"

\- git config --global alias.unstage "restore --staged"



\## Terminal Shortcuts

\- Up arrow — repeat last command

\- Tab — autocomplete branch and file names

\- Ctrl + C — cancel current command

\- Ctrl + R — search command history

\- Ctrl + L — clear terminal screen

\- q — exit git log view



\## Faster Branch Switching

\- git switch - — switch to previous branch

\- Bounce between two branches instantly

\- No need to type branch name



\## Quick Status Check

\- git status -s — compact status view

\- git log --oneline -5 — last 5 commits

\- git branch — see current branch with star



\## Stash for Quick Switches

\- git stash — save work instantly

\- git switch main — switch to main

\- Do urgent work

\- git switch - — back to feature

\- git stash pop — restore work



\## Useful One Liners

\- git log --oneline --graph --all --decorate

\- git diff --stat HEAD\~1

\- git branch --merged main

\- git remote prune origin

\- git fetch --all --prune



\## VS Code Git Integration

\- Source Control tab shows git status

\- Click plus to stage files

\- Click commit button to commit

\- Inline diff shows changes

\- GitLens extension for blame and history



\## Git GUI Tools

\- GitHub Desktop — easiest for beginners

\- GitKraken — powerful visual interface

\- Sourcetree — free and feature rich

\- VS Code built in — good for daily use



\## Saving Keystrokes



\### Stage and Commit in One

\- git commit -am "message"

\- Only works for tracked files

\- Does not stage new untracked files



\### Push Current Branch

\- git push origin HEAD

\- Pushes current branch without typing name

\- Works on any branch



\### Quick Fixup Commit

\- git commit --fixup <hash>

\- Creates fixup commit for specific hash

\- Use with git rebase --autosquash later



\## Working Faster with Remotes

\- git fetch --all --prune — update everything

\- git pull --rebase — cleaner than regular pull

\- git push -u origin HEAD — push new branch fast



\## Daily Routine for Speed

1\. git fetch --all --prune

2\. git log --oneline origin/main -5

3\. git pull --rebase

4\. git switch -c feature/name

5\. Work and commit often

6\. git push -u origin HEAD

7\. Open PR with GitHub CLI



\## Tips

\- Learn keyboard shortcuts for your tools

\- Set up aliases for most used commands

\- Use Tab completion constantly

\- Commit small and often

\- Push at end of every session

\- Review git log daily to stay oriented

