\# Git Environment Notes



\## What are Environment Files?

Environment files store configuration values

that change between environments like development

staging and production. They contain sensitive

data that should never be committed to git.



\## Common Environment Files

\- .env — main environment file

\- .env.local — local overrides

\- .env.development — development values

\- .env.staging — staging values

\- .env.production — production values

\- .env.test — test environment values



\## What Goes in Environment Files

\- API keys and secrets

\- Database connection strings

\- Third party service credentials

\- Feature flags

\- Server URLs and ports

\- Email service credentials



\## Protecting Environment Files



\### Add to .gitignore Immediately

\- .env

\- .env.local

\- .env.\*.local

\- Add before first git add

\- Never remove from .gitignore



\### Create .env.example

\- Copy .env structure without real values

\- Replace real values with placeholders

\- Commit .env.example to repo

\- Team members copy and fill in values



\### Example .env.example

\- DATABASE\_URL=your\_database\_url\_here

\- API\_KEY=your\_api\_key\_here

\- SECRET\_KEY=your\_secret\_key\_here

\- PORT=3000



\## If You Accidentally Commit .env



\### Not Yet Pushed

1\. git reset HEAD\~1

2\. Add .env to .gitignore

3\. git add .gitignore

4\. git commit -m "add env to gitignore"



\### Already Pushed

1\. Immediately revoke all exposed secrets

2\. Generate new secrets

3\. git filter-repo --path .env --invert-paths

4\. git push origin --force --all

5\. Update secrets everywhere they are used

6\. Notify team of the incident



\## Environment Variables in CI/CD

\- Never put secrets in workflow files

\- Use GitHub Secrets for sensitive values

\- Settings > Secrets and Variables > Actions

\- Reference as secrets.MY\_SECRET\_NAME

\- Masked in logs automatically



\## Managing Secrets Securely



\### Tools for Secret Management

\- GitHub Secrets — for CI/CD pipelines

\- AWS Secrets Manager — enterprise scale

\- HashiCorp Vault — self hosted option

\- Doppler — developer friendly secrets

\- 1Password Secrets — team password manager



\### Best Practices

\- Rotate secrets regularly

\- Use different secrets per environment

\- Minimum required permissions per secret

\- Audit secret access regularly

\- Never share secrets in chat or email



\## .gitignore for Environment Files

\- .env

\- .env.local

\- .env.development.local

\- .env.test.local

\- .env.production.local

\- \*.env



\## Tips

\- Add .gitignore before any git add

\- Create .env.example on day one

\- Document all required variables

\- Use secret management tools for teams

\- Audit commits for accidental secret exposure

\- Treat leaked secrets as compromised always

