\# Git Deployment Notes



\## What is Deployment?

Deployment is the process of releasing your

code to a live server where users can access

it. Git plays a central role in modern

deployment workflows.



\## Deployment Strategies



\### Manual Deployment

\- SSH into server

\- git pull origin main

\- Restart application

\- Simple but error prone



\### Automated Deployment

\- Push to GitHub triggers deployment

\- CI/CD pipeline handles everything

\- No manual steps required

\- More reliable and consistent



\### Blue Green Deployment

\- Two identical environments

\- Switch traffic between them

\- Zero downtime deployments

\- Easy rollback if issues arise



\### Rolling Deployment

\- Update servers one at a time

\- No downtime during deployment

\- Gradual rollout to users

\- Monitor for issues during rollout



\## Git Based Deployment Workflow



\### Feature to Production Flow

1\. git switch -c feature/name

2\. Develop and commit changes

3\. git push origin feature/name

4\. Open pull request

5\. Code review and CI checks

6\. Merge to main

7\. CI/CD deploys to staging

8\. Test on staging environment

9\. Promote to production

10\. Monitor for issues



\### Hotfix Deployment

1\. git switch -c hotfix/critical-bug

2\. Fix the issue quickly

3\. git push origin hotfix/critical-bug

4\. Fast track review process

5\. Merge to main immediately

6\. Deploy to production urgently

7\. Monitor closely after deploy



\## Deployment Environments



\### Development

\- Local machine

\- Developers test here first

\- Not accessible to users



\### Staging

\- Mirror of production

\- Final testing before release

\- QA team tests here

\- Should match production exactly



\### Production

\- Live environment for real users

\- Requires careful change management

\- Monitor closely after deployments



\## Git Tags for Deployments

\- Tag every production deployment

\- git tag -a v1.0.0 -m "Production release"

\- git push origin --tags

\- Easy to roll back to tagged version

\- Track what version is deployed



\## Rollback Strategy



\### Rollback with Revert

\- git revert <hash>

\- git push origin main

\- CI/CD deploys reverted code

\- Safe for shared branches



\### Rollback with Reset

\- Only for emergency situations

\- git reset --hard <tag>

\- git push --force origin main

\- Coordinate with team first



\### Rollback with Tags

\- git checkout v1.0.0

\- Deploy the tagged version

\- Stable

