\# Git Blame Notes



\## What is Git Blame?

Git blame shows who last modified each line

of a file and when. It helps track down who

made a specific change and why.



\## Basic Blame Commands

\- git blame <file> — show blame for entire file

\- git blame -L 10,20 <file> — blame lines 10 to 20

\- git blame -L 10,+5 <file> — blame 5 lines from line 10

\- git blame <hash> <file> — blame at specific commit

\- git blame --since="2 weeks" <file> — blame recent changes



\## Reading Blame Output

\- Each line shows commit hash

\- Author name and email

\- Date and time of change

\- Line number

\- Line content



\## Useful Blame Options

\- git blame -w <file> — ignore whitespace changes

\- git blame -M <file> — detect moved lines

\- git blame -C <file> — detect copied lines

\- git blame -e <file> — show email instead of name

\- git blame --date=short <file> — show short date format



\## Git Blame on GitHub

\- Open any file in a repo

\- Click Blame button top right

\- See line by line history

\- Click commit hash for details

\- Navigate through history



\## Common Use Cases



\### Finding Bug Source

1\. git log --oneline <file> — find when bug appeared

2\. git blame <file> — find who changed that line

3\. git show <hash> — see full commit details

4\. Understand context of the change



\### Code Review

\- Check who wrote a section before reviewing

\- Understand history of complex code

\- Find original author to ask questions



\### Understanding Old Code

\- Find when code was written

\- Find the commit that introduced it

\- Read commit message for context



\## Git Blame vs Git Log

\- git blame — focuses on specific lines

\- git log — focuses on commits over time

\- git blame -L shows line history

\- git log -p shows file history



\## Tips

\- Use blame to understand not to assign fault

\- Always read the commit message after blame

\- Blame shows last change not original author

\- Use GitHub blame for easier navigation

\- Combine with git show for full context



\## Note on Culture

\- Blame is a tool for understanding code

\- Not for pointing fingers at teammates

\- Use it to find context and ask questions

\- Approach findings with curiosity not judgment

