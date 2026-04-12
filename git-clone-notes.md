\# Git Clone Notes



\## What is Git Clone?

Git clone creates a local copy of a remote

repository on your machine. It downloads the

entire project history and sets up the remote

connection automatically.



\## Basic Clone Commands

\- git clone <url> — clone into folder named after repo

\- git clone <url> <folder> — clone into specific folder

\- git clone --depth 1 <url> — shallow clone latest only

\- git clone --branch <branch> <url> — clone specific branch

\- git clone --recurse-submodules <url> — clone with submodules



\## Clone URLs



\### HTTPS

\- https://github.com/username/repo.git

\- Requires username and token to push

\- Works everywhere



\### SSH

\- git@github.com:username/repo.git

\- Requires SSH key setup

\- More secure and convenient



\## After Cloning

\- cd into the cloned folder

\- git remote -v — verify remote connection

\- git branch — see available branches

\- git log --oneline — see commit history

\- Start working immediately



\## Shallow Clone

\- git clone --depth 1 <url>

\- Downloads only latest commit

\- Much faster for large repos

\- Less disk space required

\- Cannot access full history



\## Clone Specific Branch

\- git clone --branch develop <url>

\- Clones repo and checks out develop

\- All branches still available

\- git switch main to switch branches



\## Clone vs Fork vs Download



\### Clone

\- Local copy of any repo

\- Connected to remote

\- Can push if you have permission



\### Fork

\- Your own copy on GitHub

\- For contributing to others projects

\- Fork then clone your fork



\### Download ZIP

\- No git history

\- No remote connection

\- Just the files



\## Common Clone Workflows



\### Clone Your Own Repo

1\. Create repo on GitHub

2\. Copy HTTPS or SSH URL

3\. git clone <url>

4\. cd into folder

5\. Start working



\### Clone Others Repo to Contribute

1\. Fork the repo on GitHub

2\. Copy your fork URL

3\. git clone <your-fork-url>

4\. git remote add upstream <original-url>

5\. Start contributing



\## Tips

\- Always clone into a dedicated projects folder

\- Use SSH URL if SSH is set up

\- Check README after cloning

\- Run git log to understand project history

\- Never clone inside another git repo

