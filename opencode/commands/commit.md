---
description: Analyze changes and generate a commit message matching repo style
agent: general
---

Perform the following steps to create a commit:

1. **Read the following recent commit history** to understand the commit message style used in this repo:
<context name="recent-commit-history">
!`git log --oneline -20`
!`git log -10 --format="%B"`
</context>

2. **Analyze the following changes** that are staged or modified:
<context name="current-git-status">
!`git status`
!`git diff --staged`
!`git diff`
</context>

3. **Generate a commit message** that matches the style and conventions observed in the recent commit history. If a clear style is not observed, prefer to use **"Conventional Commits"**.

4. **Commit the changes** using the generated message. Do NOT use GPG signing — use `--no-gpg-sign`:
`git commit --no-gpg-sign -m "YOUR_GENERATED_MESSAGE"`

5. **Remind the user** to run manually run `gcs` (a shell alias to `git commit --amend -S --no-edit`) to sign the commit. You **do not run** this command yourself.

If there are no changes to commit, report that instead.
