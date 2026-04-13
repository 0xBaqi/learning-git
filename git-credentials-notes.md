\# Git Credentials Notes



\## What are Git Credentials?

Git credentials are the username and password

or token used to authenticate with remote

repositories like GitHub. Managing them properly

saves you from typing them every time.



\## Authentication Methods



\### Personal Access Token

\- GitHub no longer accepts passwords

\- Generate token at GitHub Settings

\- Use token as password when prompted

\- More secure than passwords



\### SSH Keys

\- Key pair based authentication

\- No username or password needed

\- Most convenient for daily use

\- Set up once per machine



\### GitHub CLI

\- gh auth login — authenticate via browser

\- Handles credentials automatically

\- Easiest setup for beginners



\## Personal Access Token Setup

1\. Go to github.com

2\. Click profile picture

3\. Click Settings

4\. Click Developer Settings

5\. Click Personal Access Tokens

6\. Click Generate new token

7\. Select scopes needed

8\. Copy token immediately

9\. Use as password when git asks



\## Token Scopes

\- repo — full repository access

\- read:org — read organization data

\- workflow — update GitHub Actions

\- Select minimum needed for security



\## Credential Helpers



\### Store Credentials

\- git config --global credential.helper store

\- Saves credentials in plain text file

\- Never prompted again after first use

\- Less secure but convenient



\### Cache Credentials

\- git config --global credential.helper cache

\- Keeps credentials in memory temporarily

\- Default timeout is 15 minutes

\- git config --global credential.helper "cache --timeout=3600"



\### Windows Credential Manager

\- git config --global credential.helper manager

\- Stores in Windows Credential Manager

\- Secure and convenient

\- Default on Windows git install



\## Viewing Stored Credentials

\- Windows — search Credential Manager

\- Look for git credentials entries

\- Can update or delete from there



\## Removing Stored Credentials

\- git credential reject — remove specific credential

\- Clear from Windows Credential Manager manually

\- Useful when token expires or changes



\## Troubleshooting Authentication



\### Token Expired

\- Generate new token on GitHub

\- Update in Windows Credential Manager

\- Or run git push and enter new token



\### Permission Denied

\- Check token has correct scopes

\- Verify remote URL is correct

\- Try regenerating token



\### Wrong Username

\- git config --global user.name "correct name"

\- Update credential in manager



\## Tips

\- Use SSH for most convenient setup

\- Set token expiry to reasonable time

\- Never share tokens with anyone

\- Regenerate tokens if exposed

\- Use credential manager on Windows

\- Enable two factor auth on GitHub

