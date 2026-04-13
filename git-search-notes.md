\# Git Search Notes



\## Why Search in Git?

Git has powerful search tools that go beyond

searching current files. You can search through

commit history, file contents, and changes

across your entire project history.



\## Searching File Contents



\### Git Grep

\- git grep "keyword" — search all tracked files

\- git grep -n "keyword" — show line numbers

\- git grep -l "keyword" — show filenames only

\- git grep -i "keyword" — case insensitive

\- git grep -w "keyword" — whole word only

\- git grep "keyword" -- \*.js — specific file type



\### Search in Other Branches

\- git grep "keyword" main — search main branch

\- git grep "keyword" feature/name — search feature

\- git grep "keyword" HEAD\~5 — search old commit



\## Searching Commit History



\### Search Commit Messages

\- git log --grep="keyword" — find by message

\- git log --grep="fix" --oneline — compact results

\- git log --grep="bug" --all — all branches



\### Search Code Changes

\- git log -S "keyword" — commits adding keyword

\- git log -G "regex" — commits matching pattern

\- git log -S "function\_name" — find when added

\- git log -S "keyword" --oneline — compact view



\### Search by Author

\- git log --author="Baqi" — commits by author

\- git log --author="Baqi" --oneline

\- git log --committer="name" — by committer



\### Search by Date

\- git log --since="2 weeks ago"

\- git log --until="2024-01-01"

\- git log --since="2024-01-01" --until="2024-06-01"

\- git log --after="yesterday"



\## Searching for Files



\### Find Deleted Files

\- git log --all --full-history -- filename

\- Shows commits that touched the file

\- Even if file no longer exists



\### Find When File was Added

\- git log --follow <file>

\- Tracks file through renames

\- Shows complete file history



\### Find File at Old Commit

\- git show <hash>:<filepath>

\- Shows file content at that commit

\- Good for recovering deleted content



\## Advanced Search Combinations



\### Find Bug Introduction

\- git log -S "buggy code" --oneline

\- Find when problematic code was added

\- Combine with git bisect for precision



\### Search Specific Folder History

\- git log -- src/ — commits touching src folder

\- git grep "keyword" -- src/ — search in src only

\- Narrow scope for large projects



\### Search Across All Branches

\- git log --all --grep="feature"

\- git grep "keyword" --all

\- Find anything anywhere in repo



\## Searching GitHub



\### GitHub Search

\- Search within a specific repo

\- Press T to search files

\- Use GitHub search bar for code search

\- Filter by language, file type, path



\## Tips

\- Use git grep instead of regular grep in repos

\- Use git log -S to find when code was introduced

\- Combine filters for precise results

\- git log --all searches every

