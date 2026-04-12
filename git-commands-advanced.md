\# Advanced Git Commands



\## Rebase

\- git rebase main — rebase current branch onto main

\- git rebase -i HEAD\~3 — interactive rebase last 3 commits

\- git rebase --abort — cancel a rebase

\- git rebase --continue — continue after resolving conflict



\## Cherry Pick

\- git cherry-pick <hash> — apply a specific commit to current branch

\- git cherry-pick --abort — cancel cherry pick

\- git cherry-pick --continue — continue after resolving conflict



\## Reflog

\- git reflog — show all recent HEAD movements

\- git reset --hard <hash> — go back to a specific point

\- useful for recovering lost commits



\## Bisect

\- git bisect start — start binary search

\- git bisect good <hash> — mark commit as good

\- git bisect bad <hash> — mark commit as bad

\- git bisect reset — end bisect session



\## Submodules

\- git submodule add <url> — add a submodule

\- git submodule update --init — initialize submodules

\- git clone --recurse-submodules <url> — clone with submodules



\## Tags

\- git tag — list all tags

\- git tag v1.0 — create lightweight tag

\- git tag -a v1.0 -m "message" — create annotated tag

\- git push origin --tags — push all tags

\- git tag -d v1.0 — delete a tag



\## Stash

\- git stash — stash current changes

\- git stash list — list all stashes

\- git stash pop — apply last stash

\- git stash drop — delete last stash

\- git stash clear — delete all stashes

