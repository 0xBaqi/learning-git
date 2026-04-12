\# Git Reflog Notes



\## What is Reflog?

Reflog records every movement of HEAD in your repo.

It is like a safety net that saves you from mistakes.

Even deleted branches and lost commits can be recovered.



\## Basic Reflog Commands

\- git reflog — show all HEAD movements

\- git reflog show <branch> — show branch reflog

\- git reflog expire — clean up old reflog entries

\- git reflog delete — delete specific reflog entry



\## Reading Reflog Output

\- HEAD@{0} — current position

\- HEAD@{1} — one step back

\- HEAD@{2} — two steps back

\- Each line shows hash, action, and description



\## Common Recovery Scenarios



\### Recover Deleted Branch

1\. git reflog — find last commit of deleted branch

2\. Copy the commit hash

3\. git switch -c recovered-branch <hash>

4\. Branch is restored with all commits



\### Recover After Hard Reset

1\. git reflog — find commit before reset

2\. Copy the commit hash

3\. git reset --hard <hash>

4\. Back to state before reset



\### Recover Dropped Stash

1\. git reflog show refs/stash — find stash commits

2\. Copy the stash commit hash

3\. git stash apply <hash>

4\. Stash is recovered



\### Undo a Rebase Gone Wrong

1\. git reflog — find commit before rebase

2\. git reset --hard HEAD@{5} — go back to that point

3\. Rebase is undone



\## Reflog Expiry

\- Reflog entries expire after 90 days by default

\- Unreachable commits expire after 30 days

\- Can be configured with gc.reflogExpire setting



\## Tips

\- Always check reflog before panicking

\- Reflog is local only, not pushed to GitHub

\- Act quickly before entries expire

\- Use git show <hash> to verify before recovering

\- Reflog is your best friend after mistakes



\## Notes

\- Reflog only exists locally on your machine

\- Cannot recover from someone elses machine

\- Clone does not include reflog

\- Good reason to not use hard reset carelessly

