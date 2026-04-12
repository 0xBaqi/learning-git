\# Git Aliases Notes



\## What are Aliases?

Aliases are shortcuts for long git commands.

They save time and reduce typing errors.



\## Creating Aliases

\- git config --global alias.st status

\- git config --global alias.co checkout

\- git config --global alias.br branch

\- git config --global alias.cm "commit -m"



\## Using Aliases

\- git st — runs git status

\- git co main — runs git checkout main

\- git br — runs git branch

\- git cm "message" — runs git commit -m "message"



\## Useful Aliases to Set Up



\### Basic

\- git config --global alias.st status

\- git config --global alias.co checkout

\- git config --global alias.br branch

\- git config --global alias.df diff



\### Log Aliases

\- git config --global alias.lg "log --oneline"

\- git config --global alias.lgg "log --oneline --graph"

\- git config --global alias.lga "log --oneline --graph --all"



\### Commit Aliases

\- git config --global alias.cm "commit -m"

\- git config --global alias.cam "commit -am"

\- git config --global alias.amend "commit --amend"



\### Branch Aliases

\- git config --global alias.sw switch

\- git config --global alias.swc "switch -c"



\### Undo Aliases

\- git config --global alias.unstage "restore --staged"

\- git config --global alias.undo "reset HEAD\~1"



\## Viewing Aliases

\- git config --list | grep alias



\## Removing an Alias

\- git config --global --unset alias.st



\## Notes

\- Aliases are stored in .gitconfig file

\- Can also edit .gitconfig directly to add aliases

\- Aliases cannot override built in git commands

