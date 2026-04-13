\# Git Monorepo Notes



\## What is a Monorepo?

A monorepo is a single repository that contains

multiple projects or packages. Instead of separate

repos for each service, everything lives together

in one place.



\## Monorepo vs Polyrepo



\### Monorepo

\- All projects in one repository

\- Shared tooling and dependencies

\- Easier code sharing

\- Single place to search and review

\- Large companies like Google use this



\### Polyrepo

\- Each project has its own repository

\- Independent versioning per project

\- Smaller focused repos

\- More common in smaller teams



\## Benefits of Monorepo

\- Easy code sharing between projects

\- Single source of truth

\- Atomic commits across projects

\- Simplified dependency management

\- Easier refactoring across projects

\- One CI/CD pipeline to manage



\## Challenges of Monorepo

\- Repository grows very large over time

\- Slower git operations on large repos

\- Build times can increase

\- Need tooling to manage complexity

\- Access control more complex



\## Monorepo Tools



\### Turborepo

\- Build system for JavaScript monorepos

\- Caches build outputs for speed

\- Parallel task execution

\- Popular with Next.js projects



\### Nx

\- Powerful monorepo toolkit

\- Works with many languages

\- Smart rebuilds only affected projects

\- Great developer experience



\### Lerna

\- JavaScript package manager for monorepos

\- Manages npm packages in monorepo

\- Version management across packages

\- Publishing multiple packages together



\### Yarn Workspaces

\- Built into Yarn package manager

\- Manages dependencies across packages

\- Hoists shared dependencies

\- Simple setup for JavaScript



\## Common Monorepo Structure

\- apps/ — deployable applications

\- packages/ — shared libraries

\- tools/ — development tooling

\- docs/ — documentation

\- scripts/ — utility scripts



\## Git Tricks for Monorepos



\### Sparse Checkout

\- Check out only folders you need

\- git sparse-checkout set apps/frontend

\- Faster for large monorepos



\### Shallow Clone

\- git clone --depth 1 <url>

\- Only download recent history

\- Much faster for large repos



\### Partial Clone

\- git clone --filter=blob:none <url>

\- Download objects on demand

\- Good balance of speed and access



\## Commit Conventions in Monorepo

\- feat(frontend): add login page

\- fix(backend): resolve auth error

\- docs(shared): update API documentation

\- Include project scope in commit message

\- Makes history easier to filter



\## Tips

\- Use sparse checkout for large monorepos

\- Set up CI to only build changed projects

\- Use commit scopes to identify project

\- Invest in good tooling from the start

\- Document monorepo structure in README

\- Consider polyrepo if team is very small

