\# Git Notes Notes



\## What are Git Notes?

Git notes let you add extra information to

commits without changing the commit itself.

They are stored separately from commits and

can be added after the fact.



\## Basic Notes Commands

\- git notes add -m "note" <hash> — add a note

\- git notes show <hash> — show note for commit

\- git notes list — list all notes

\- git notes edit <hash> — edit a note

\- git notes remove <hash> — remove a note

\- git notes append -m "more" <hash> — append to note



\## Adding Notes

\- git notes add -m "reviewed by team" HEAD

\- git notes add -m "deployed to staging" <hash>

\- Adds note without changing commit hash

\- Original commit stays exactly the same



\## Viewing Notes

\- git notes show — show note for HEAD

\- git notes show <hash> — show note for commit

\- git log --show-notes — show notes in log output

\- git log --notes — same as above



\## Pushing and Fetching Notes

\- git push origin refs/notes/commits

\- git fetch origin refs/notes/commits

\- Notes are not pushed with regular git push

\- Must push notes ref explicitly



\## Common Use Cases



\### Code Review Notes

\- Add review status to commits

\- git notes add -m "approved by lead" <hash>

\- Track review progress without new commits



\### Deployment Tracking

\- git notes add -m "deployed to production" <hash>

\- Record when commit was deployed

\- Useful for deployment history



\### Bug Tracking

\- git notes add -m "related to issue #42" <hash>

\- Link commits to issues after the fact

\- Add context discovered later



\### Test Results

\- git notes add -m "all tests passing" <hash>

\- Record test status for commits

\- CI systems sometimes use this



\## Notes vs Commit Messages

\- Commit message — part of the commit

\- Git notes — separate, can be added later

\- Notes can be changed without changing commit

\- Notes must be explicitly pushed to remote



\## Notes Namespaces

\- git notes --ref=review add -m "approved" <hash>

\- Create custom namespaces for notes

\- Organize different types of notes

\- git notes --ref=review show <hash>



\## Tips

\- Notes are rarely used but useful to know

\- Must explicitly push notes to share them

\- Good for adding context after the fact

\- Use commit messages for important information

\- Notes can be lost if not pushed carefully

\- Consider using commit messages instead

