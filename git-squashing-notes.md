\# Git Squashing Notes



\## What is Squashing?

Squashing combines multiple commits into one.

It cleans up messy commit history before merging

a feature branch into main.



\## Why Squash Commits

\- Clean up WIP commits

\- Combine related small changes

\- Make git log easier to read

\- One commit per feature or fix

\- Easier to revert if needed



\## How to Squash with Interactive Rebase



\### Step by Step

1\. git log --oneline — count commits to squash

2\. git rebase -i HEAD\~3 — open last 3 commits

3\. Editor opens with list of commits

4\. Change pick to squash on commits to combine

5\. Save and close editor

6\. Edit combined commit message

7\. Save and close editor again

8\. Squash is complete



\### Interactive Rebase Commands

\- pick — keep commit as is

\- squash — combine with previous commit

\- fixup — combine, discard commit message

\- reword — keep commit, edit message

\- drop — delete commit completely



\### Example

\- pick abc1234 add login page

\- squash def5678 fix login typo

\- squash ghi9012 fix login styling

\- All three become one commit



\## Squash on GitHub

\- When merging a pull request

\- Click dropdown next to Merge button

\- Select Squash and merge

\- Edit the combined commit message

\- Click Confirm squash and merge

\- All PR commits become one commit on main



\## Squash vs Merge vs Rebase on GitHub



\### Merge Commit

\- Preserves all commits

\- Creates a merge commit

\- Full history visible



\### Squash and Merge

\- Combines all PR commits into one

\- Clean linear history on main

\- Loses individual commit history



\### Rebase and Merge

\- Replays commits on top of main

\- No merge commit created

\- Linear history preserved



\## When to Squash

\- Before merging feature branch

\- After finishing a feature

\- When commits are messy or unclear

\- When PR has many small WIP commits



\## When Not to Squash

\- When individual commits are meaningful

\- When commits need to be reviewed separately

\- After pushing to shared branch



\## Tips

\- Squash before pushing to remote

\- Never squash commits others have based work on

\- Use fixup for commits that just fix typos

\- Write a good squashed commit message

\- Squash and merge is safest option on GitHub

