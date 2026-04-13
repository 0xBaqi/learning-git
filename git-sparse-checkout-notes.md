\# Git Sparse Checkout Notes



\## What is Sparse Checkout?

Sparse checkout lets you check out only specific

folders or files from a repository instead of

the entire codebase. Useful for large monorepos

where you only need part of the code.



\## Basic Sparse Checkout Commands

\- git sparse-checkout init — enable sparse checkout

\- git sparse-checkout set <folder> — set folders to checkout

\- git sparse-checkout list — list current patterns

\- git sparse-checkout add <folder> — add more folders

\- git sparse-checkout disable — disable sparse checkout



\## Setting Up Sparse Checkout



\### New Clone with Sparse Checkout

1\. git clone --no-checkout <url>

2\. cd into repo folder

3\. git sparse-checkout init --cone

4\. git sparse-checkout set src docs

5\. git checkout main

6\. Only src and docs folders downloaded



\### Enable on Existing Repo

1\. git sparse-checkout init --cone

2\. git sparse-checkout set <folder>

3\. Other folders become hidden locally



\## Cone Mode vs No Cone Mode

\- Cone mode — faster, works with folders only

\- No cone mode — slower, supports file patterns

\- Cone mode recommended for most use cases

\- git sparse-checkout init --cone for cone mode



\## Adding More Folders

\- git sparse-checkout add tests

\- git sparse-checkout add config

\- Adds to existing sparse checkout patterns

\- Does not remove previously set folders



\## Viewing Sparse Checkout Patterns

\- git sparse-checkout list

\- Shows which folders are checked out

\- Helps understand current state



\## Disabling Sparse Checkout

\- git sparse-checkout disable

\- All files become visible again

\- Returns to normal full checkout

\- Does not delete any files



\## Common Use Cases



\### Large Monorepo

\- Repository has hundreds of folders

\- You only work on one service

\- Sparse checkout that service folder only

\- Faster clones and less disk space



\### Documentation Only

\- Only need docs folder to write documentation

\- git sparse-checkout set docs

\- Skip all source code folders



\### Frontend Only Work

\- Full stack repo with backend and frontend

\- git sparse-checkout set frontend

\- Only download frontend code



\## Benefits

\- Faster clone times for large repos

\- Less disk space used

\- Faster git operations overall

\- Focus on relevant code only



\## Tips

\- Best for very large repositories

\- Use cone mode for better performance

\- Combine with shallow clone for speed

\- git sparse-checkout list to verify setup

\- Not needed for small or medium repos

\- Check with team before using on shared repos

