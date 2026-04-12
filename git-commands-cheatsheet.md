\# Git Commands Cheatsheet



\## Setup

\- git config --global user.name "Name"

\- git config --global user.email "email"

\- git config --global core.editor "code"

\- git config --global init.defaultBranch main

\- git config --list



\## Starting a Repo

\- git init

\- git clone <url>

\- git remote add origin <url>



\## Staging \& Committing

\- git status

\- git add .

\- git add <file>

\- git commit -m "message"

\- git commit -am "message"

\- git commit --amend



\## Viewing History

\- git log

\- git log --oneline

\- git log --oneline --graph

\- git log --oneline --all

\- git diff

\- git diff --staged

\- git show <hash>

\- git blame <file>



\## Branching

\- git branch

\- git branch <name>

\- git branch -d <name>

\- git branch -D <name>

\- git switch <branch>

\- git switch -c <branch>

\- git merge <branch>

\- git merge --abort



\## Remote

\- git remote -v

\- git remote add origin <url>

\- git fetch

\- git pull

\- git push origin main

\- git push -u origin main

\- git push --force-with-lease



\## Undoing

\- git restore <file>

\- git restore --staged <file>

\- git reset HEAD\~1

\- git reset --soft HEAD\~1

\- git reset --hard HEAD\~1

\- git revert <hash>

\- git clean -fd



\## Stash

\- git stash

\- git stash pop

\- git stash list

\- git stash drop

\- git stash clear



\## Rebase

\- git rebase main

\- git rebase -i HEAD\~3

\- git rebase --abort

\- git rebase --continue



\## Tags

\- git tag

\- git tag v1.0

\- git tag -a v1.0 -m "message"

\- git push origin --tags

\- git tag -d v1.0



\## Advanced

\- git cherry-pick <hash>

\- git bisect start

\- git reflog

\- git submodule add <url>

\- git archive --format=zip HEAD

