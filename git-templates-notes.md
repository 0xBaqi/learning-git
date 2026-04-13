\# Git Templates Notes



\## What are Git Templates?

Git templates are predefined files and folders

that are copied into every new repository you

create or clone. They help maintain consistency

across all your projects.



\## Types of Templates



\### Repository Templates

\- GitHub repos marked as templates

\- Create new repos based on template

\- Copies files structure and content

\- Great for project boilerplates



\### Git Init Templates

\- Local folder with template files

\- Copied into .git on every git init

\- Good for hooks and config defaults



\### GitHub Templates

\- Issue templates

\- Pull request templates

\- Stored in .github folder

\- Standardize contributions



\## Creating a GitHub Template Repo

1\. Create a repo with your boilerplate

2\. Go to repo Settings

3\. Check Template repository checkbox

4\. Repo is now a template

5\. Others click Use this template to start



\## Using a Template Repo

1\. Go to template repo on GitHub

2\. Click Use this template

3\. Click Create new repository

4\. Name your new repo

5\. New repo has all template files



\## Issue Templates

\- Create .github/ISSUE\_TEMPLATE/ folder

\- Add markdown files for each template

\- Users see template options when creating issues

\- Guides contributors to provide right info



\### Bug Report Template

\- Steps to reproduce

\- Expected behavior

\- Actual behavior

\- Environment details

\- Screenshots



\### Feature Request Template

\- Problem description

\- Proposed solution

\- Alternative solutions

\- Additional context



\## Pull Request Template

\- Create .github/PULL\_REQUEST\_TEMPLATE.md

\- Auto fills PR description box

\- Guides contributors on what to include

\- Checklist for PR requirements



\### Common PR Template Items

\- Description of changes

\- Type of change

\- Testing done

\- Screenshots if applicable

\- Checklist of requirements



\## Git Init Templates

\- git config --global init.templateDir \~/.git-templates

\- Create folder at that path

\- Add hooks or config files

\- Copied to every new repo automatically



\## Common Template Files



\### Every Repo Should Have

\- README.md

\- .gitignore

\- LICENSE

\- CHANGELOG.md



\### Team Repos Should Have

\- CONTRIBUTING.md

\- CODE\_OF\_CONDUCT.md

\- .github/ISSUE\_TEMPLATE/

\- .github/PULL\_REQUEST\_TEMPLATE.md

\- .github/workflows/ci.yml



\## Tips

\- Create templates for common project types

\- Keep templates updated as standards evolve

\- Document what each template includes

\- Use templates to onboard new projects fast

\- Share template repos with your team

\- Review and improve templates regularly

