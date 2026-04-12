\# Git Archive Notes



\## What is Git Archive?

Git archive creates a compressed archive file

of your repository at a specific point in time.

It exports your code without the git history

or .git folder.



\## Basic Archive Commands

\- git archive --format=zip HEAD > project.zip

\- git archive --format=tar HEAD > project.tar

\- git archive --format=zip HEAD -o project.zip

\- git archive <hash> --format=zip > old-version.zip

\- git archive <tag> --format=zip > release.zip



\## Archive Formats

\- zip — most common, works everywhere

\- tar — common on Linux and Mac

\- tar.gz — compressed tar archive



\## Archive Specific Version

\- git archive v1.0 --format=zip > v1.0.zip

\- git archive HEAD\~5 --format=zip > old.zip

\- git archive <hash> --format=zip > specific.zip



\## Archive Specific Folder

\- git archive HEAD src/ --format=zip > src.zip

\- Only exports the src folder contents

\- Useful for partial exports



\## Archive with Prefix

\- git archive --format=zip --prefix=myproject/ HEAD > project.zip

\- Adds folder prefix inside the zip

\- Files will be inside myproject/ folder

\- Good for clean distribution



\## Common Use Cases



\### Create Release Package

1\. git tag -a v1.0 -m "Release v1.0"

2\. git archive v1.0 --format=zip -o release-v1.0.zip

3\. Share the zip file with users



\### Export Without Git History

1\. git archive HEAD --format=zip -o export.zip

2\. Share code without exposing git history

3\. Good for client deliverables



\### Backup Specific Commit

1\. git log --oneline — find commit

2\. git archive <hash> --format=zip > backup.zip

3\. Keep as point in time backup



\## Archive vs Clone vs Download



\### Git Archive

\- No git history included

\- No .git folder

\- Clean export of just the code



\### Git Clone

\- Full git history included

\- Complete repository copy

\- Can push and pull



\### GitHub Download ZIP

\- Same as git archive basically

\- No git history

\- Done through GitHub UI



\## Tips

\- Use for creating release distributions

\- Good for sharing code without history

\- Combine with tags for version releases

\- Use prefix option for clean zip structure

\- Cannot archive uncommitted changes

\- Always test the archive after creating

