\# Git Statistics Notes



\## Why Track Git Statistics?

Git statistics help you understand project

activity, contributor patterns, and codebase

growth. Useful for project management and

performance reviews.



\## Basic Statistics Commands

\- git shortlog -sn — commit count per author

\- git log --oneline | wc -l — total commit count

\- git branch -a | wc -l — total branch count

\- git tag | wc -l — total tag count

\- git count-objects -vH — repo size info



\## Commit Statistics



\### Total Commits

\- git rev-list --count HEAD

\- Shows total number of commits on branch



\### Commits per Author

\- git shortlog -sn

\- git shortlog -sn --no-merges

\- Sorted by most commits first



\### Commits in Time Range

\- git log --since="1 month ago" --oneline | wc -l

\- git log --since="2024-01-01" --until="2024-06-01"



\### Commits per Day

\- git log --format="%ad" --date=short

\- Lists date of every commit

\- Pipe to sort and uniq for counts



\## Code Statistics



\### Lines Changed per Commit

\- git log --stat --oneline

\- Shows files and lines per commit



\### Total Lines Added and Removed

\- git log --numstat --oneline

\- Numbers of additions and deletions



\### Files Changed Most Often

\- git log --name-only --format="" | sort | uniq -c | sort -rn

\- Shows which files change most frequently



\## Repository Size

\- git count-objects -vH

\- Shows loose objects and pack files

\- Total size of repository

\- Useful for maintenance decisions



\## Branch Statistics

\- git branch -a | wc -l — count all branches

\- git branch --merged | wc -l — merged branches

\- git branch --no-merged | wc -l — unmerged branches



\## Contributor Statistics



\### First and Last Commit

\- git log --reverse --oneline | head -1

\- git log --oneline | head -1

\- Shows project start and latest commit



\### Most Active Contributors

\- git shortlog -sn --no-merges

\- Excludes merge commits for accuracy



\### Your Personal Stats

\- git log --author="Baqi" --oneline | wc -l

\- Count your own commits

\- git log --author="Baqi" --stat



\## GitHub Statistics

\- Insights tab on any GitHub repo

\- Contributors graph

\- Commit activity over time

\- Code frequency additions and deletions

\- Traffic and clone statistics

\- Dependency network



\## Third Party Tools

\- gitstats — generates HTML reports

\- git-quick-stats — terminal statistics

\- GitHub Insights — built into GitHub

\- Code Climate — code quality metrics



\## Tips

\- Check statistics before performance reviews

\- Use insights to find bottlenecks

\- Track commit frequency for consistency

\- Monitor repo size for maintenance needs

\- Compare statistics across time periods

\- Use GitHub Insights for visual overview

