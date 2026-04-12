\# Git Commit Messages Notes



\## Why Good Commit Messages Matter

\- Help teammates understand your changes

\- Make debugging easier with git bisect

\- Generate changelogs automatically

\- Show professionalism and care

\- Make git log useful not just noise



\## Anatomy of a Good Commit Message



\### Subject Line

\- Maximum 50 characters

\- Use present tense

\- No period at the end

\- Capitalize first word

\- Be specific and descriptive



\### Body (optional)

\- Separate from subject with blank line

\- Maximum 72 characters per line

\- Explain what and why not how

\- Include context and motivation

\- Reference issues and PRs



\## Conventional Commits



\### Format

\- type(scope): description



\### Types

\- feat — new feature

\- fix — bug fix

\- docs — documentation changes

\- style — formatting changes

\- refactor — code restructuring

\- test — adding or updating tests

\- chore — maintenance tasks

\- perf — performance improvements

\- ci — CI/CD changes

\- build — build system changes



\### Examples

\- feat(auth): add Google login

\- fix(api): resolve timeout error

\- docs(readme): update installation steps

\- style(button): fix inconsistent padding

\- refactor(database): simplify query logic

\- test(user): add registration unit tests

\- chore(deps): update dependencies



\## Good vs Bad Examples



\### Bad Commit Messages

\- fix bug

\- update code

\- changes

\- wip

\- asdfgh

\- final version

\- last commit



\### Good Commit Messages

\- fix null pointer in user authentication

\- add dark mode toggle to settings page

\- update README with Docker instructions

\- remove deprecated payment gateway code

\- refactor search to improve performance



\## Tips

\- Write message before making changes

\- Read your message before committing

\- Ask yourself what does this commit do

\- If message needs and, split into two commits

\- Squash WIP commits before merging

\- Use git commit without -m for longer messages

