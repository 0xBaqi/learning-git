\# GitHub Actions Notes



\## What is GitHub Actions?

GitHub Actions is a CI/CD platform built into GitHub.

It automates tasks like testing, building, and deploying code.



\## Key Concepts



\### Workflow

\- A automated process defined in a YAML file

\- Stored in .github/workflows/ folder

\- Triggered by events like push or pull request



\### Event

\- What triggers the workflow

\- Examples: push, pull\_request, schedule, manual



\### Job

\- A set of steps that run on the same machine

\- Jobs run in parallel by default

\- Can be configured to run sequentially



\### Step

\- A single task within a job

\- Can run commands or use actions



\### Action

\- A reusable unit of code

\- Can be from GitHub Marketplace

\- Or custom written



\## Basic Workflow Example  



\## Common Use Cases

\- Run tests automatically on push

\- Build and deploy to production

\- Send notifications on failure

\- Auto assign issues and PRs

\- Generate documentation

\- Publish packages to npm



\## GitHub Actions Benefits

\- Free for public repositories

\- Integrated with GitHub

\- Large marketplace of actions

\- Supports all major languages

\- Matrix builds for multiple OS



\## Tips

\- Start with simple workflows

\- Use marketplace actions when possible

\- Cache dependencies for faster builds

\- Set up branch protection rules

\- Monitor workflow run times



