\# Git Bisect Notes



\## What is Git Bisect?

Bisect helps you find which commit introduced a bug.

It uses binary search to narrow down commits quickly.

Instead of checking every commit manually, bisect

cuts the search in half each time.



\## Basic Bisect Commands

\- git bisect start — start bisect session

\- git bisect good <hash> — mark commit as working

\- git bisect bad <hash> — mark commit as broken

\- git bisect reset — end bisect and go back to HEAD

\- git bisect log — show bisect history



\## Basic Workflow

1\. git bisect start

2\. git bisect bad — mark current commit as bad

3\. git bisect good <hash> — mark last known good commit

4\. Git checks out a middle commit

5\. Test if bug exists

6\. git bisect good or git bisect bad

7\. Repeat until git finds the culprit commit

8\. git bisect reset — go back to normal



\## Example Session

\- git bisect start

\- git bisect bad HEAD

\- git bisect good v1.0

\- Git checks out commit in the middle

\- Test your code

\- git bisect good — if bug is not present

\- git bisect bad — if bug is present

\- Continue until git says "first bad commit"

\- git bisect reset



\## Automated Bisect

\- git bisect run <script>

\- Script returns 0 for good, non zero for bad

\- Git runs script automatically on each commit

\- Finds bad commit without manual testing



\## Tips

\- The more commits in range the more useful bisect is

\- Keep commits small for easier bisecting

\- Write automated tests to use with bisect run

\- Note the bad commit hash before resetting

\- Use git show <hash> to inspect the bad commit



\## When to Use Bisect

\- Bug appeared recently but cause is unknown

\- Large codebase with many commits

\- Cannot reproduce bug in isolation

\- Need to find exact commit that broke something

