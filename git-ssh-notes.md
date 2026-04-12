\# Git SSH Notes



\## What is SSH?

SSH (Secure Shell) is a secure protocol for

connecting to remote servers and services.

It is more secure than HTTPS for git operations.



\## SSH vs HTTPS

\- SSH — uses key pair, no password needed

\- HTTPS — uses username and token

\- SSH — faster and more secure

\- HTTPS — easier to set up initially



\## Setting Up SSH for GitHub



\### Step 1 - Generate SSH Key

\- ssh-keygen -t ed25519 -C "your@email.com"

\- Press Enter to accept default location

\- Add a passphrase for extra security



\### Step 2 - Start SSH Agent

\- eval "$(ssh-agent -s)"

\- ssh-add \~/.ssh/id\_ed25519



\### Step 3 - Copy Public Key

\- cat \~/.ssh/id\_ed25519.pub

\- Copy the output



\### Step 4 - Add to GitHub

\- Go to GitHub Settings

\- Click SSH and GPG keys

\- Click New SSH key

\- Paste your public key

\- Click Add SSH key



\### Step 5 - Test Connection

\- ssh -T git@github.com

\- Should say "Hi username! You have successfully authenticated"



\## Using SSH URLs

\- HTTPS: https://github.com/username/repo.git

\- SSH: git@github.com:username/repo.git



\## Switch Existing Repo to SSH

\- git remote set-url origin git@github.com:username/repo.git

\- git remote -v — verify the change



\## SSH Key Management

\- Keep private key secure, never share it

\- Add passphrase for extra security

\- Generate separate keys per device

\- Revoke old keys when changing devices

\- Back up your private key securely



\## Troubleshooting

\- Permission denied — check key is added to GitHub

\- Connection timeout — check firewall settings

\- Wrong key — verify with ssh -T git@github.com

