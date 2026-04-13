\# Git Code Review Notes



\## What is Code Review?

Code review is the process of examining code

changes before they are merged into the main

branch. It improves code quality and spreads

knowledge across the team.



\## Why Code Review Matters

\- Catches bugs before they reach production

\- Improves code quality and consistency

\- Spreads knowledge across team members

\- Enforces coding standards

\- Mentors junior developers

\- Creates shared ownership of code



\## Code Review with Git



\### Pull Request Review on GitHub

1\. Author opens pull request

2\. Reviewers are requested or assigned

3\. Reviewers examine the diff

4\. Leave comments on specific lines

5\. Approve or request changes

6\. Author addresses feedback

7\. Reviewer approves when satisfied

8\. PR is merged



\## Reviewing a PR Locally

\- gh pr checkout <number> — check out PR locally

\- Test the changes on your machine

\- Run the test suite

\- Check for edge cases

\- git switch - to go back after review



\## What to Look for in Code Review



\### Correctness

\- Does the code do what it claims

\- Are edge cases handled

\- Are error cases handled properly

\- Does it match the requirements



\### Code Quality

\- Is the code readable and clear

\- Are variable names descriptive

\- Is there unnecessary complexity

\- Are there code smells



\### Performance

\- Are there obvious performance issues

\- Unnecessary database queries

\- Inefficient algorithms or loops

\- Memory leaks or resource issues



\### Security

\- Are inputs validated and sanitized

\- Are there SQL injection risks

\- Are secrets hardcoded anywhere

\- Are permissions checked properly



\### Tests

\- Are new features tested

\- Are edge cases covered

\- Do existing tests still pass

\- Is test coverage maintained



\## Giving Good Review Feedback



\### Be Specific

\- Point to exact line of code

\- Explain why it is an issue

\- Suggest how to fix it



\### Be Kind

\- Assume good intent

\- Ask questions instead of demanding

\- Praise good code too

\- Focus on code not the person



\### Use Prefixes

\- nit: — minor style issue

\- suggestion: — optional improvement

\- question: — asking for clarification

\- blocker: — must fix before merging



\## Receiving Review Feedback

\- Do not take feedback personally

\- Ask for clarification if unclear

\- Discuss disagreements respectfully

\- Thank reviewers for their time

\- Learn from every review



\## Review Checklist

\- Code does what PR description says

\- No obvious bugs or logic errors

\- No hardcoded secrets or passwords

\- Tests included and passing

\- Documentation updated if needed

\- Follows team coding standards

\- No unnecessary code or files



\## Tips

\- Review in small chunks not all at once

\- Review the diff not just the files

\- Test locally for complex changes

\- Be timely with reviews

\- Keep PRs small for easier review

\- Use review templates for consistency

