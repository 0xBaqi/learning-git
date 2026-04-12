\# Git Versioning Notes



\## What is Versioning?

Versioning is a system for tracking and managing

different versions of your software over time.

It helps users know what changed between releases.



\## Semantic Versioning (SemVer)



\### Format

\- MAJOR.MINOR.PATCH

\- Example: v2.4.1



\### Rules

\- MAJOR — breaking changes, incompatible API

\- MINOR — new features, backwards compatible

\- PATCH — bug fixes, backwards compatible



\### Examples

\- v1.0.0 — first stable release

\- v1.1.0 — added new feature

\- v1.1.1 — fixed a bug

\- v2.0.0 — breaking changes made



\## Pre-release Versions

\- v1.0.0-alpha — early testing

\- v1.0.0-beta — feature complete, testing

\- v1.0.0-rc.1 — release candidate

\- v1.0.0 — stable release



\## Git Tags for Versioning

\- git tag -a v1.0.0 -m "First stable release"

\- git push origin v1.0.0

\- git push origin --tags



\## Changelog

\- Document all changes per version

\- Keep a CHANGELOG.md file

\- Follow keepachangelog.com format



\### Changelog Format

\- Added — new features

\- Changed — changes in existing functionality

\- Deprecated — soon to be removed features

\- Removed — removed features

\- Fixed — bug fixes

\- Security — security fixes



\## Release Workflow

1\. Finish all features for version

2\. Update version number in code

3\. Update CHANGELOG.md

4\. git add .

5\. git commit -m "chore: release v1.0.0"

6\. git tag -a v1.0.0 -m "Release v1.0.0"

7\. git push origin main

8\. git push origin --tags

9\. Create GitHub Release from tag



\## GitHub Releases

\- Go to repo on GitHub

\- Click Releases

\- Click Draft a new release

\- Choose your tag

\- Add release title and notes

\- Attach build files if needed

\- Publish release



\## Tips

\- Start versioning from v0.1.0

\- Never reuse version numbers

\- Tag every release

\- Write detailed release notes

\- Automate releases with GitHub Actions

\- Communicate breaking changes clearly

