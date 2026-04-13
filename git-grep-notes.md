\# Git Grep Notes



\## What is Git Grep?

Git grep searches through your repository content

for a pattern or keyword. It is faster than

regular grep because it only searches tracked

files and respects .gitignore.



\## Basic Grep Commands

\- git grep "keyword" — search all tracked files

\- git grep "keyword" <branch> — search specific branch

\- git grep "keyword" HEAD\~1 — search previous commit

\- git grep -n "keyword" — show line numbers

\- git grep -l "keyword" — show only filenames

\- git grep -c "keyword" — show count per file



\## Search Options

\- git grep -i "keyword" — case insensitive search

\- git grep -w "keyword" — whole word match only

\- git grep -v "keyword" — show lines not matching

\- git grep -r "keyword" — recursive search

\- git grep -E "regex" — use extended regex



\## Search in Specific Files

\- git grep "keyword" -- \*.md — search markdown files

\- git grep "keyword" -- src/ — search src folder

\- git grep "keyword" -- \*.js — search JavaScript files



\## Search Across Commits

\- git grep "keyword" HEAD — search current state

\- git grep "keyword" HEAD\~5 — search 5 commits ago

\- git grep "keyword" v1.0 — search at tag v1.0

\- git grep "keyword" main — search main branch



\## Combining with Log

\- git log -S "keyword" — find commits adding keyword

\- git log -G "regex" — find commits matching pattern

\- More powerful for historical searching



\## Common Use Cases



\### Find Where Function is Used

\- git grep "functionName"

\- Shows every file and line using it

\- Faster than searching in editor



\### Find TODO Comments

\- git grep "TODO"

\- git grep "FIXME"

\- Find all outstanding tasks in code



\### Find Configuration Values

\- git grep "API\_KEY"

\- git grep "localhost"

\- Find hardcoded values quickly



\### Search Before Refactoring

\- git grep "oldFunctionName"

\- Find all places to update

\- Ensure nothing is missed



\## Git Grep vs Regular Grep

\- git grep — only searches tracked files

\- git grep — respects .gitignore

\- git grep — can search other branches

\- git grep — faster in git repositories

\- Regular grep — searches all files

\- Regular grep — does not know about git



\## Tips

\- Use git grep instead of find in git repos

\- Add -n for line numbers always

\- Use -l when you just need filenames

\- Combine with --and for multiple patterns

\- git grep is much faster than grep in large repos

\- Search other branches without switching

