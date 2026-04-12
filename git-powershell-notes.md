\# Git with PowerShell Notes



\## What is PowerShell?

PowerShell is the default terminal on Windows.

It has slightly different syntax from Command Prompt.



\## Essential PowerShell Commands

\- cd <folder> — change directory

\- cd .. — go back one level

\- dir — list files in current folder

\- mkdir <folder> — create a new folder

\- New-Item <file> — create a new file

\- Remove-Item <file> — delete a file

\- Rename-Item <old> <new> — rename a file

\- notepad <file> — open file in notepad

\- cls — clear the terminal

\- pwd — show current directory



\## PowerShell vs Command Prompt

\- dir works in both

\- ls works in PowerShell only

\- %USERPROFILE% works in CMD only

\- $env:USERPROFILE works in PowerShell only

\- New-Item is PowerShell only

\- touch works in CMD only



\## Common PowerShell Git Workflow

1\. cd C:\\Users\\NURUDEEN\\MyProject

2\. git status

3\. git switch -c feature/name

4\. New-Item <file>

5\. notepad <file>

6\. git add .

7\. git commit -m "message"

8\. git push origin feature/name



\## Useful Shortcuts

\- Up arrow — previous command

\- Tab — autocomplete

\- Ctrl + C — cancel command

\- Ctrl + L — clear screen

\- q — quit git log view



\## Environment Variables

\- $env:USERPROFILE — user folder path

\- $env:USERNAME — current username

\- $env:COMPUTERNAME — computer name



\## Tips

\- Always confirm location with pwd before git add .

\- Use Tab to autocomplete folder and file names

\- Use Up arrow to reuse previous commands

\- Check git status before every commit

