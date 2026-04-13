\# Conventional Commits Notes



\## What are Conventional Commits?

Conventional commits is a specification for

writing standardized commit messages. It makes

commit history readable and enables automated

changelog generation.



\## Basic Format

\- type(scope): description

\- type — what kind of change

\- scope — what part of codebase

\- description — short summary



\## Commit Types



\### Primary Types

\- feat — new feature added

\- fix — bug fix

\- docs — documentation changes only

\- style — formatting no logic change

\- refactor — code restructure no feature or fix

\- test — adding or updating tests

\- chore — maintenance and tooling



\### Additional Types

\- perf — performance improvement

\- ci — CI/CD configuration changes

\- build — build system changes

\- revert — reverting a previous commit



\## Scope Examples

\- feat(auth): add Google login

\- fix(api): resolve timeout error

\- docs(readme): update installation steps

\- style(button): fix padding inconsistency

\- refactor(database): simplify query logic

\- test(user): add registration tests

\- chore(deps): update all dependencies



\## Breaking Changes

\- Add exclamation mark after type

\- feat!: remove deprecated API endpoints

\- fix!: change response format

\- Or add BREAKING CHANGE in commit body



\## Full Commit Message Format

\- feat(auth): add Google OAuth login

\- blank line

\- Adds support for Google OAuth 2.0

\- Users can now sign in with Google account

\- Requires GOOGLE\_CLIENT\_ID environment variable

\- blank line

\- Closes #42



\## Benefits of Conventional Commits



\### Automated Changelogs

\- Tools read commit history

\- Generate changelog automatically

\- Group by feat fix and breaking changes

\- No manual changelog writing needed



\### Semantic Versioning

\- feat commits trigger minor version bump

\- fix commits trigger patch version bump

\- Breaking changes trigger major version bump

\- Automated version management possible



\### Better Communication

\- Anyone can understand changes at a glance

\- Clear scope shows what area changed

\- Type shows impact and intent

\- Consistent across entire team



\## Tools that Use Conventional Commits

\- semantic-release — automates versioning

\- standard-version — changelog generation

\- commitizen — interactive commit helper

\- commitlint — enforces commit format

\- release-please — GitHub release automation



\## Commitizen Setup

\- npm install -g commitizen

\- git cz instead of git commit

\- Interactive prompts for type scope description

\- Ensures correct format every time



\## Commitlint Setup

\- Enforces conventional commits format

\- Fails commit if format is wrong

\- Works with git hooks

\- Keeps entire team consistent



\## Examples in Practice



\### Feature Addition

\- feat(search): add filter by date range



\### Bug Fix

\- fix(login): resolve session timeout issue



\### Documentation

\- docs(api): add authentication examples



\### Breaking Change

\- feat!: remove support for Node 14



\## Tips

\- Be consistent with scope naming

\- Keep description under 72 characters

\- Use present tense in description

\- Reference issues when relevant

\- Start with conventional commits early

\- Use commitizen to learn the format

