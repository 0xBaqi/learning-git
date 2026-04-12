\# Git Security Notes



\## What to Never Commit

\- Passwords and secrets

\- API keys and tokens

\- .env files

\- Private keys and certificates

\- Database credentials

\- Personal information



\## Preventing Accidents



\### Use .gitignore

\- Add .env to .gitignore before first commit

\- Add config files with secrets

\- Add key files and certificates



\### Check Before Committing

\- git diff --staged — review changes before commit

\- git status — see what files are staged

\- git log -p — see what was committed



\## If You Accidentally Commit a Secret



\### If not pushed yet

\- git reset HEAD\~1 — undo last commit

\- Remove the secret from file

\- Add file to .gitignore

\- git add .

\- git commit -m "remove sensitive data"



\### If already pushed

\- Immediately revoke the exposed secret

\- Generate a new secret

\- git rm --cached <file>

\- Add file to .gitignore

\- git commit -m "remove sensitive file"

\- git push origin main

\- Consider repo history as compromised



\## Personal Access Tokens

\- Use tokens instead of passwords

\- Set expiry dates on tokens

\- Use minimum required permissions

\- Revoke tokens when no longer needed

\- Never share tokens with anyone



\## SSH Keys

\- More secure than HTTPS

\- Generate with ssh-keygen

\- Add public key to GitHub

\- Use git@github.com URLs



\## Best Practices

\- Always use .gitignore from day one

\- Review every commit before pushing

\- Use environment variables for secrets

\- Rotate secrets regularly

\- Enable two factor auth on GitHub

