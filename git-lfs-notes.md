\# Git LFS Notes



\## What is Git LFS?

Git Large File Storage is an extension that

replaces large files with text pointers inside

git while storing the actual files on a remote

server. It keeps your repo fast and small.



\## Why Use Git LFS

\- Git is not designed for large binary files

\- Large files slow down clone and fetch

\- Images videos and audio bloat repo size

\- LFS stores large files separately

\- Repo stays fast and lightweight



\## Installing Git LFS

\- Download from git-lfs.com

\- git lfs install — enable LFS in git

\- Run once per user account

\- Then set up per repository



\## Basic LFS Commands

\- git lfs install — enable LFS

\- git lfs track "\*.psd" — track file pattern

\- git lfs track "\*.mp4" — track video files

\- git lfs ls-files — list LFS tracked files

\- git lfs status — show LFS file status

\- git lfs pull — download LFS files

\- git lfs push origin main — push LFS files



\## Setting Up LFS in a Repo

1\. git lfs install

2\. git lfs track "\*.png"

3\. git lfs track "\*.jpg"

4\. git add .gitattributes

5\. git commit -m "add LFS tracking"

6\. Now add and commit large files normally



\## .gitattributes File

\- Created automatically by git lfs track

\- Contains LFS tracking patterns

\- Must be committed to repo

\- Shared with all contributors



\## Common File Types for LFS

\- Images — png jpg gif psd ai

\- Videos — mp4 mov avi mkv

\- Audio — mp3 wav flac

\- Archives — zip tar gz

\- Binaries — exe dmg pkg

\- Datasets — csv (large ones)

\- Game assets — fbx obj blend



\## LFS on GitHub

\- GitHub supports LFS natively

\- Free accounts get 1GB LFS storage

\- 1GB bandwidth per month free

\- Purchase more storage as needed



\## LFS Workflow

1\. Set up LFS tracking for file types

2\. Add large files normally with git add

3\. Git automatically uses LFS for tracked types

4\. git push uploads to LFS storage

5\. git pull downloads LFS files as needed



\## Cloning Repos with LFS

\- git clone <url> — downloads LFS files automatically

\- git lfs pull — manually download LFS files

\- git clone --no-checkout then git lfs pull



\## Tips

\- Set up LFS before adding large files

\- Track by file extension not individual files

\- Commit .gitattributes file always

\- Check GitHub LFS storage limits

\- Use LFS for all binary and media files

\- Never commit large files without LFS

