\# Git Add Notes



\## What is Git Add?

Git add moves changes from your working directory

to the staging area. It prepares changes to be

included in the next commit.



\## Basic Add Commands

\- git add . — stage all changes in current folder

\- git add <file> — stage a specific file

\- git add <folder> — stage an entire folder

\- git add -A — stage all changes everywhere

\- git add -p — interactively stage chunks

\- git add -u — stage modified and deleted only



\## Staging Area

\- Also called the index

\- Holds changes ready to commit

\- Lets you choose what goes in each commit

\- Review with git diff --staged



\## Add Specific Files

\- git add README.md

\- git add src/index.js

\- git add src/ — all files in src folder

\- git add \*.js — all JavaScript files



\## Interactive Staging

\- git add -p

\- Shows each change chunk by chunk

\- Options for each chunk:

&#x20; - y — stage this chunk

&#x20; - n — skip this chunk

&#x20; - s — split into smaller chunks

&#x20; - e — manually edit the chunk

&#x20; - q — quit interactive mode



\## Add vs Commit

\- git add — moves changes to staging area

\- git commit — saves staging area as a commit

\- You can add multiple times before committing

\- Staging lets you group related changes



\## Common Add Mistakes



\### Adding from Wrong Folder

\- git add . only adds from current folder down

\- Check pwd before running git add .

\- cd to project root first



\### Adding Sensitive Files

\- Accidentally staging .env or config files

\- Add to .gitignore before running git add

\- git restore --staged <file> to unstage



\### Adding Everything When You Shouldnt

\- Use git add <file> for selective staging

\- Use git status to review before addings

\- Use git add -p for precise control



\## Unstaging Files

\- git restore --staged <file> — unstage specific file

\- git restore --staged . — unstage everything

\- Changes are kept in working directory



\## Tips

\- Always check git status before git add

\- Use git add -p for careful commits

\- Stage related changes together

\- Review staged changes with git diff --staged

\- Unstage with git restore --staged if needed

\- Never add node\_modules or build folders

