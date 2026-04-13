\# Git Multiple Accounts Notes



\## Why Use Multiple Accounts?

Many developers have separate GitHub accounts

for personal and work projects. Managing both

on the same machine requires some configuration.



\## Common Scenarios

\- Personal GitHub and work GitHub

\- Client projects needing separate accounts

\- Open source contributions from personal account

\- Different email per project required



\## Setting Up Multiple SSH Keys



\### Generate Keys for Each Account

1\. ssh-keygen -t ed25519 -C "personal@email.com" -f \~/.ssh/id\_personal

2\. ssh-keygen -t ed25519 -C "work@email.com" -f \~/.ssh/id\_work

3\. Two key pairs created in .ssh folder



\### Add Keys to SSH Agent

1\. ssh-add \~/.ssh/id\_personal

2\. ssh-add \~/.ssh/id\_work



\### Add Public Keys to GitHub

1\. cat \~/.ssh/id\_personal.pub — copy output

2\. Add to personal GitHub account SSH keys

3\. cat \~/.ssh/id\_work.pub — copy output

4\. Add to work GitHub account SSH keys



\### Create SSH Config File

1\. New-Item \~/.ssh/config

2\. notepad \~/.ssh/config

3\. Add configuration for each account



\### SSH Config Content

\- Host github-personal

\-   HostName github.com

\-   User git

\-   IdentityFile \~/.ssh/id\_personal

\- Host github-work

\-   HostName github.com

\-   User git

\-   IdentityFile \~/.ssh/id\_work



\## Using Different Accounts per Repo



\### Clone with Specific Account

\- git clone git@github-personal:username/repo.git

\- git clone git@github-work:company/repo.git

\- Uses alias from SSH config



\### Update Existing Repo Remote

\- git remote set-url origin git@github-personal:username/repo.git



\## Setting User per Repo

\- cd into repo folder

\- git config user.name "Personal Name"

\- git config user.email "personal@email.com"

\- Overrides global config for this repo only



\## Global vs Local Config

\- Global — applies to all repos

\- Local — applies to current repo only

\- Local always overrides global

\- Use local config for work repos



\## Verify Current Config

\- git config user.name

\- git config user.email

\- git config --list --local

\- Confirm correct identity before committing



\## Common Mistakes

\- Committing work code with personal email

\- Pushing personal project to work account

\- Using wrong SSH key for wrong account

\- Forgetting to set local config for work repos



\## Tips

\- Set global config to personal account

\- Set local config for every work repo

\- Test SSH connection before pushing

\- ssh -T git@github-personal to test

\- ssh -T git@github-work to test

\- Double check email before first commit

