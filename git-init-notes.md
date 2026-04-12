\# Git Init Notes



\## What is Git Init?

Git init initializes a new git repository in

a folder. It creates a hidden .git folder that

tracks all changes to your project.



\## Basic Init Commands

\- git init — initialize repo in current folder

\- git init <folder> — create folder and initialize

\- git init --bare — create a bare repository



\## What Git Init Creates

\- .git/ folder — hidden git directory

\- .git/config — repo configuration

\- .git/HEAD — pointer to current branch

\- .git/hooks/ — git hook scripts

\- .git/objects/ — git object database

\- .git/refs/ — branch and tag references



\## After Git Init



\### Connect to GitHub

1\. Create repo on GitHub

2\. git remote add origin <url>

3\. git push -u origin main



\### First Commit Workflow

1\. git init

2\. New-Item README.md

3\. notepad README.md

4\. Add content and save

5\. git add README.md

6\. git commit -m "initial commit"

7\. git remote add origin <url>

8\. git push -u origin main



\## Bare Repository

\- git init --bare

\- No working directory

\- Used as central remote repo

\- GitHub repos are bare repos

\- Used on servers not local machines



\## Reinitializing

\- Running git init in existing repo is safe

\- Does not overwrite existing history

\- Can update templates if needed

\- Shows Reinitialized message



\## Checking if Folder is a Repo

\- git status — shows if inside a git repo

\- ls -la — look for .git folder

\- git log — shows history if repo exists



\## Common Init Mistakes



\### Init in Wrong Folder

\- Check location with pwd first

\- cd to correct folder then git init



\### Init Inside Another Repo

\- Avoid nested git repos

\- Check git status before init

\- Can cause confusion and errors



\### Forgetting to Connect Remote

\- Always add remote after init

\- git remote add origin <url>

\- Then push your first commit



\## Tips

\- Always init before adding files

\- Create README before first commit

\- Add .gitignore before first commit

\- Connect to GitHub right after init

\- Check git status after init to confirm

