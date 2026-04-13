\# Git Commit Signing Notes



\## What is Commit Signing?

Commit signing verifies that commits actually

came from you. It adds a cryptographic signature

to each commit proving your identity. GitHub

shows a Verified badge on signed commits.



\## Why Sign Commits

\- Prove commits are genuinely from you

\- Prevent commit author impersonation

\- Required by some organizations

\- Verified badge on GitHub looks professional

\- Adds extra layer of security



\## Signing Methods



\### GPG Signing

\- Most common signing method

\- Uses GPG key pair

\- Widely supported

\- Works with all git hosts



\### SSH Signing

\- Newer signing method

\- Uses existing SSH key

\- Simpler setup than GPG

\- Supported by GitHub since 2022



\### S/MIME Signing

\- Uses X.509 certificates

\- Common in enterprise environments

\- More complex setup



\## Setting Up GPG Signing



\### Generate GPG Key

1\. gpg --full-generate-key

2\. Choose RSA and RSA

3\. Choose 4096 bits

4\. Set expiry date

5\. Enter name and email

6\. Create passphrase



\### Get Your Key ID

1\. gpg --list-secret-keys --keyid-format LONG

2\. Copy the key ID after rsa4096/



\### Configure Git to Use GPG

1\. git config --global user.signingkey <keyid>

2\. git config --global commit.gpgsign true

3\. git config --global gpg.program gpg



\### Add GPG Key to GitHub

1\. gpg --armor --export <keyid>

2\. Copy the output

3\. GitHub Settings > SSH and GPG keys

4\. New GPG key > paste and save



\## Setting Up SSH Signing



\### Configure Git for SSH Signing

1\. git config --global gpg.format ssh

2\. git config --global user.signingkey \~/.ssh/id\_ed25519.pub

3\. git config --global commit.gpgsign true



\### Add to GitHub

1\. GitHub Settings > SSH and GPG keys

2\. Add as Signing Key not Authentication Key



\## Signing Commits



\### Sign All Commits Automatically

\- git config --global commit.gpgsign true

\- Every commit signed automatically

\- No extra steps needed



\### Sign Individual Commits

\- git commit -S -m "signed commit"

\- Only signs that specific commit



\### Sign Tags

\- git tag -s v1.0 -m "signed tag"

\- git tag -v v1.0 — verify signed tag



\## Verifying Signatures

\- git log --show-signature

\- Shows signature status per commit

\- Good — signature is valid

\- Bad — signature is invalid

\- No signature — commit not signed



\## GitHub Verified Badge

\- Green Verified badge on signed commits

\- Shows commit is authentic

\- Unsigned commits show no badge

\- Required by some organizations



\## Tips

\- Enable signing early in your git journey

\- Use SSH signing for simpler setup

\- Back up your GPG key securely

\- Set expiry on GPG keys for security

\- Sign tags as well as commits

\- Require signed commits in branch protection

