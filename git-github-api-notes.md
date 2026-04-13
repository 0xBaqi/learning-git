\# GitHub API Notes



\## What is the GitHub API?

The GitHub API lets you interact with GitHub

programmatically. You can automate tasks, build

tools, and access GitHub data from your own

applications.



\## API Versions



\### REST API

\- Traditional HTTP endpoints

\- Returns JSON responses

\- Easy to use and understand

\- Well documented at docs.github.com



\### GraphQL API

\- Single endpoint for all data

\- Request exactly what you need

\- More efficient for complex queries

\- Requires learning GraphQL syntax



\## Authentication



\### Personal Access Token

\- Most common authentication method

\- Generate at GitHub Settings

\- Include in request headers

\- Authorization: Bearer your\_token\_here



\### GitHub Apps

\- More secure for production use

\- Fine grained permissions

\- Can act as installation not user

\- Better for automated tools



\## Common REST API Endpoints



\### Repositories

\- GET /repos/owner/repo — get repo info

\- GET /repos/owner/repo/commits — list commits

\- GET /repos/owner/repo/branches — list branches

\- POST /user/repos — create new repo



\### Issues

\- GET /repos/owner/repo/issues — list issues

\- POST /repos/owner/repo/issues — create issue

\- PATCH /repos/owner/repo/issues/number — update issue

\- POST /repos/owner/repo/issues/number/comments



\### Pull Requests

\- GET /repos/owner/repo/pulls — list PRs

\- POST /repos/owner/repo/pulls — create PR

\- PUT /repos/owner/repo/pulls/number/merge — merge PR



\### Users

\- GET /user — get authenticated user

\- GET /users/username — get any user

\- GET /user/repos — list your repos



\## Making API Requests



\### With Curl

\- curl -H "Authorization: Bearer token"

\- https://api.github.com/user

\- Returns your user information as JSON



\### With JavaScript Fetch

\- fetch with Authorization header

\- Parse JSON response

\- Handle errors appropriately



\### With Octokit

\- Official GitHub API client

\- Available for JavaScript and other languages

\- Simplifies API interactions

\- Handles authentication automatically



\## Rate Limiting

\- Unauthenticated — 60 requests per hour

\- Authenticated — 5000 requests per hour

\- Check headers for remaining requests

\- X-RateLimit-Remaining header

\- X-RateLimit-Reset shows when limit resets



\## GitHub API Use Cases



\### Automation

\- Auto create issues from external systems

\- Close issues when tasks complete

\- Post comments automatically

\- Generate reports from repo data



\### Analytics

\- Track commit frequency

\- Monitor PR merge times

\- Analyze contributor activity

\- Generate custom dashboards



\### Integrations

\- Connect GitHub to other tools

\- Sync issues with project management

\- Post GitHub events to Slack

\- Trigger external deployments



\## Webhooks

\- GitHub sends events to your server

\- Real time notifications of activity

\- Push events trigger your code

\- Great for building integrations

\- Set up in repo Settings > Webhooks



\## Tips

\- Always authenticate API requests

\- Cache responses to avoid rate limits

\- Use GraphQL for complex data needs

\- Test with curl before building apps

\- Read pagination headers for large results

\- Store tokens securely never in code

