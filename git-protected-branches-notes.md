\# Git Protected Branches Notes



\## What are Protected Branches?

Protected branches are branches with rules that

prevent accidental changes. They enforce code

quality and collaboration standards by requiring

reviews and passing checks before merging.



\## Why Protect Branches

\- Prevent direct pushes to main

\- Require code review before merging

\- Enforce CI checks to pass

\- Prevent force pushes

\- Maintain stable codebase

\- Enforce team workflow standards



\## Setting Up Branch Protection on GitHub

1\. Go to repo on GitHub

2\. Click Settings

3\. Click Branches in sidebar

4\. Click Add branch protection rule

5\. Enter branch name pattern

6\. Select protection options

7\. Click Create or Save changes



\## Branch Protection Options



\### Require Pull Request Reviews

\- Require at least one approval

\- Dismiss stale reviews on new commits

\- Require review from code owners

\- Restrict who can dismiss reviews



\### Require Status Checks

\- Require CI to pass before merging

\- Select specific checks required

\- Require branches to be up to date

\- Prevents merging broken code



\### Restrict Push Access

\- Only specific people can push

\- Protect from accidental direct commits

\- Enforce pull request workflow



\### Other Options

\- Require signed commits

\- Require linear history

\- Include administrators in restrictions

\- Allow force pushes for specific users

\- Allow deletions



\## Common Protection Setups



\### Solo Developer

\- Require CI checks to pass

\- Prevent force pushes

\- Keep history clean



\### Small Team

\- Require one pull request review

\- Require CI to pass

\- Prevent direct pushes to main



\### Large Team

\- Require two pull request reviews

\- Require specific team review

\- Require all CI checks to pass

\- Require up to date branches

\- Restrict who can merge



\## CODEOWNERS File

\- Create .github/CODEOWNERS

\- Assign owners to specific files or folders

\- Owners automatically requested for review

\- Example: src/ @username

\- Enforces right people review right code



\## Bypassing Protection

\- Repository administrators can bypass

\- Can grant bypass to specific people

\- Should be used sparingly

\- Always document why bypass was needed



\## Branch Naming Patterns

\- main — protect exact branch name

\- release/\* — protect all release branches

\- v\* — protect version branches

\- feature/\* — can protect feature branches too



\## Tips

\- Always protect main branch

\- Set up protection before team starts working

\- Require CI before requiring reviews

\- Start with fewer rules and add more later

\- Document your branch protection policy

\- Review and update rules as team grows

