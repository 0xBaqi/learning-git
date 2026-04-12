\# Git Tags Notes



\## What are Tags?

Tags mark specific points in your repo history.

Usually used to mark release versions like v1.0, v2.0.



\## Types of Tags



\### Lightweight Tags

\- Just a pointer to a commit

\- git tag v1.0



\### Annotated Tags

\- Full objects with message, date, author

\- git tag -a v1.0 -m "First release"

\- Recommended for releases



\## Basic Tag Commands

\- git tag — list all tags

\- git tag v1.0 — create lightweight tag

\- git tag -a v1.0 -m "message" — create annotated tag

\- git tag -d v1.0 — delete a local tag

\- git show v1.0 — show tag details



\## Tagging Old Commits

\- git log --oneline — find the commit hash

\- git tag -a v1.0 <hash> -m "message" — tag old commit



\## Pushing Tags

\- git push origin v1.0 — push specific tag

\- git push origin --tags — push all tags

\- git push origin --follow-tags — push commits and tags



\## Deleting Remote Tags

\- git push origin --delete v1.0



\## Checking Out Tags

\- git checkout v1.0 — view code at that tag

\- git switch -c release/v1.0 v1.0 — create branch from tag



\## Versioning Convention

\- v1.0.0 — Major.Minor.Patch

\- Major — breaking changes

\- Minor — new features

\- Patch — bug fixes

