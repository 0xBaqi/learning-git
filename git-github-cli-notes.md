\# GitHub CLI Notes



\## What is GitHub CLI?

GitHub CLI is a command line tool that brings

GitHub features into your terminal. You can

manage pull requests, issues, and repos without

opening a browser.



\## Installing GitHub CLI

\- Download from cli.github.com

\- Windows — winget install GitHub.cli

\- Verify with gh --version



\## Authentication

\- gh auth login

\- Follow prompts to authenticate

\- Choose GitHub.com

\- Login via browser or token

\- Credentials saved automatically



\## Basic CLI Commands

\- gh auth login — authenticate with GitHub

\- gh auth status — check authentication status

\- gh auth logout — log out of GitHub



\## Repository Commands

\- gh repo create — create a new repo

\- gh repo clone <repo> — clone a repo

\- gh repo view — view repo details

\- gh repo list — list your repositories

\- gh repo fork — fork a repository



\## Pull Request Commands

\- gh pr create — create a pull request

\- gh pr list — list open pull requests

\- gh pr view — view a pull request

\- gh pr merge — merge a pull request

\- gh pr checkout <number> — checkout a PR locally

\- gh pr review — review a pull request

\- gh pr close — close a pull request



\## Issue Commands

\- gh issue create — create a new issue

\- gh issue list — list open issues

\- gh issue view <number> — view an issue

\- gh issue close <number> — close an issue

\- gh issue comment <number> — comment on issue



\## Workflow Commands

\- gh workflow list — list GitHub Actions workflows

\- gh workflow run — trigger a workflow manually

\- gh run list — list recent workflow runs

\- gh run view — view workflow run details



\## Creating a Pull Request with CLI

1\. git switch -c feature/name

2\. Make changes and commit

3\. git push origin feature/name

4\. gh pr create

5\. Follow prompts for title and description

6\. PR created without opening browser



\## Common CLI Workflows



\### Full Feature Workflow

1\. gh repo clone username/repo

2\. git switch -c feature/name

3\. Make changes and commit

4\. git push origin feature/name

5\. gh pr create --title "Add feature" --body "Description"

6\. gh pr merge when approved



\### Quick Issue Creation

1\. gh issue create --title "Bug found" --body "Description"

2\. Issue created instantly

3\. gh issue list to verify



\## Tips

\- gh makes PR creation much faster

\- Use gh pr checkout to test others PRs

\- gh repo create for quick repo setup

\- Combine with git for powerful workflow

\- gh --help for full command list

\- Tab completion available after setup

