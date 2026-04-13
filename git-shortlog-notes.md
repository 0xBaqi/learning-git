\# Git Shortlog Notes



\## What is Git Shortlog?

Git shortlog summarizes git log output by grouping

commits by author. It is useful for generating

changelogs and seeing contribution stats.



\## Basic Shortlog Commands

\- git shortlog — group commits by author

\- git shortlog -s — show only commit counts

\- git shortlog -n — sort by number of commits

\- git shortlog -sn — count sorted by most commits

\- git shortlog -e — show email addresses

\- git shortlog -sne — count with emails sorted



\## Reading Shortlog Output

\- Author name appears as header

\- Their commits listed below

\- Commit count shown with -s flag

\- Sorted alphabetically by default



\## Shortlog Options

\- -s or --summary — show count only

\- -n or --numbered — sort by commit count

\- -e or --email — show email addresses

\- -c or --committer — group by committer

\- --no-merges — exclude merge commits



\## Common Shortlog Uses



\### See Top Contributors

\- git shortlog -sn

\- Shows who committed most

\- Great for project statistics



\### Generate Changelog Authors

\- git shortlog v1.0..v2.0

\- Shows commits between two versions

\- Group by author for changelog



\### Check Your Own Commits

\- git shortlog --author="Baqi"

\- See all your commits listed

\- Good for reviewing your work



\### Project Activity Overview

\- git shortlog -sn --no-merges

\- Clean view of real contributions

\- Excludes automated merge commits



\## Shortlog for Specific Range

\- git shortlog HEAD\~10..HEAD — last 10 commits

\- git shortlog v1.0..v2.0 — between versions

\- git shortlog --since="1 month ago" — recent period

\- git shortlog main..feature — branch comparison



\## Shortlog vs Log

\- git log — detailed view of each commit

\- git shortlog — summary grouped by author

\- Use log for investigating specific commits

\- Use shortlog for contribution overview



\## Tips

\- Use git shortlog -sn for quick stats

\- Combine with date filters for periods

\- Great for writing release notes

\- Use --no-merges for cleaner results

\- Pipe to file for reports

\- Good habit to run before releases

