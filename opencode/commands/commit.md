---
description: Analyze changes and generate a commit message matching repo style
---

Perform the following steps to create a commit:

1. **Read the following recent commit history** to understand the commit message style used in this repo:
!`git log --oneline -20`
!`git log -10 --format="%B"`

2. **Analyze the following changes** that are staged or modified:
!`git status`
!`git diff --staged`
!`git diff`

3. **Generate a commit message** that matches the style and conventions observed in the recent commit history.

4. **Commit the changes** using the generated message. Do NOT use GPG signing — use `--no-gpg-sign`:
`git commit --no-gpg-sign -m "YOUR_GENERATED_MESSAGE"`

5. **Remind the user** to run manually run `gcs` (a shell alias to `git commit --amend -S --no-edit`) to sign the commit. You **do not run** this command yourself.

If there are no changes to commit, report that instead.
