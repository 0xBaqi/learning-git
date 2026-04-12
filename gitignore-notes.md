\# .gitignore Notes



\## What is .gitignore?

A file that tells git which files and folders to ignore.

Ignored files are not tracked or committed.



\## How to create it

\- New-Item .gitignore (PowerShell)

\- touch .gitignore (Mac/Linux)



\## Common patterns

\- \*.log — ignore all log files

\- node\_modules/ — ignore node modules folder

\- .env — ignore environment variables file

\- build/ — ignore build folder

\- \*.tmp — ignore all temp files

\- !important.log — exception, don't ignore this file



\## Common .gitignore files by project type



\### Node.js

\- node\_modules/

\- .env

\- dist/



\### Python

\- \_\_pycache\_\_/

\- \*.pyc

\- .env

\- venv/



\### General

\- .DS\_Store

\- Thumbs.db

\- \*.log

