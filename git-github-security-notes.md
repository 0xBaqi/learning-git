\# GitHub Security Notes



\## GitHub Security Features

GitHub has built in security features to help

keep your code and accounts safe. Understanding

these features protects you and your projects.



\## Account Security



\### Two Factor Authentication

\- Enable in GitHub Settings > Security

\- Use authenticator app not SMS

\- Save backup codes in safe place

\- Required by GitHub for all users

\- Prevents unauthorized account access



\### Personal Access Tokens

\- Use instead of passwords

\- Set minimum required scopes

\- Set expiry dates on all tokens

\- Revoke immediately if compromised

\- Never share tokens with anyone



\### SSH Keys

\- More secure than HTTPS

\- Generate separate key per device

\- Add passphrase to private key

\- Remove old keys when changing devices

\- Review authorized keys regularly



\## Repository Security



\### Dependabot

\- Automatically scans dependencies

\- Creates PRs to update vulnerable packages

\- Alerts you to security vulnerabilities

\- Enable in repo Security settings

\- Review and merge Dependabot PRs promptly



\### Secret Scanning

\- Scans commits for exposed secrets

\- Alerts when API keys are detected

\- Works with many secret formats

\- Enabled by default on public repos

\- Revoke any detected secrets immediately



\### Code Scanning

\- Static analysis of your code

\- Finds security vulnerabilities

\- Uses CodeQL analysis engine

\- Set up via GitHub Actions

\- Reviews findings in Security tab



\## Security Advisories

\- Report vulnerabilities privately

\- Create advisories for your projects

\- Coordinate disclosure with researchers

\- GitHub assists with CVE assignment

\- Protects users before patch is ready



\## Branch Protection for Security

\- Require signed commits

\- Require pull request reviews

\- Require status checks to pass

\- Prevent force pushes to main

\- Restrict who can push to branches



\## Dependency Security



\### Viewing Dependencies

\- Insights tab > Dependency graph

\- See all project dependencies

\- Find vulnerable packages

\- Track dependency licenses



\### Dependabot Alerts

\- Automatic vulnerability notifications

\- Links to security advisories

\- Severity ratings for each alert

\- Fix suggestions included

\- Enable in Security settings



\### Dependabot Security Updates

\- Automatic PRs for vulnerable deps

\- Updates to safe version automatically

\- Review and merge to fix vulnerability

\- Works with many package managers



\## Security Best Practices



\### For Your Account

\- Enable two factor authentication

\- Use strong unique password

\- Review authorized apps regularly

\- Check active sessions regularly

\- Use passkeys when available



\### For Your Repositories

\- Never commit secrets or credentials

\- Use environment variables for secrets

\- Enable Dependabot alerts

\- Enable secret scanning

\- Review collaborator access regularly

\- Archive inactive repositories



\### For Your Code

\- Validate all user inputs

\- Use parameterized queries

\- Keep dependencies updated

\- Follow OWASP guidelines

\- Conduct regular security reviews



\## Reporting Security Issues

\- Use private vulnerability reporting

\- Never report security bugs in public issues

\- Give maintainers time to fix before disclosure

\- Follow responsible disclosure principles

\- GitHub Security Advisory for coordination



\## Tips

\- Security tab shows all security features

\- Enable all free security features immediately

\- Review security alerts weekly

\- Treat all alerts as high priority

\- Security is everyones responsibility

\- Stay updated on common vulnerabilities

