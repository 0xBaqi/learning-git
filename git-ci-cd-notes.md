\# Git CI/CD Notes



\## What is CI/CD?

CI/CD stands for Continuous Integration and

Continuous Deployment. It automates testing

and deploying code every time you push to

your repository.



\## Continuous Integration (CI)

\- Automatically runs tests on every push

\- Catches bugs before they reach main

\- Ensures code quality standards

\- Runs on every pull request

\- Fails PR if tests do not pass



\## Continuous Deployment (CD)

\- Automatically deploys passing code

\- No manual deployment steps needed

\- Code goes from push to production

\- Faster release cycles

\- More reliable deployments



\## CI/CD with GitHub Actions



\### Basic CI Workflow

\- Triggers on push or pull request

\- Runs on GitHub hosted servers

\- Installs dependencies

\- Runs test suite

\- Reports pass or fail



\### Basic CD Workflow

\- Triggers on merge to main

\- Builds the application

\- Deploys to hosting platform

\- Sends notification on success



\## Common CI/CD Platforms

\- GitHub Actions — built into GitHub

\- CircleCI — popular third party

\- Travis CI — popular for open source

\- Jenkins — self hosted option

\- GitLab CI — built into GitLab



\## GitHub Actions CI Example

\- Create .github/workflows/ci.yml

\- Define trigger events

\- Set up job and steps

\- Install dependencies

\- Run tests

\- Report results



\## Branch Protection with CI

\- Require CI to pass before merging

\- GitHub Settings > Branches

\- Add branch protection rule

\- Check require status checks

\- Select your CI workflow

\- PRs cannot merge if CI fails



\## Common CI Steps

\- Checkout code

\- Set up language runtime

\- Install dependencies

\- Run linting

\- Run unit tests

\- Run integration tests

\- Generate coverage report

\- Build application



\## Common CD Steps

\- Checkout code

\- Install dependencies

\- Build for production

\- Run final tests

\- Deploy to server

\- Clear cache

\- Send success notification



\## CI/CD Best Practices

\- Keep builds fast under 10 minutes

\- Fix broken builds immediately

\- Never merge with failing CI

\- Test in same environment as production

\- Use secrets for sensitive values

\- Cache dependencies for speed



\## Environment Variables in CI

\- Store secrets in GitHub Settings

\- Settings > Secrets and Variables

\- Reference in workflow as secrets.NAME

\- Never hardcode secrets in workflow files



\## Tips

\- Start with simple CI before adding CD

\- Test your workflow file carefully

\- Use marketplace actions when possible

\- Monitor build times and optimize

\- Set up notifications for failures

\- Green CI builds build team confidence

