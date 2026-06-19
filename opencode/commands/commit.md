---
description: Analyze changes and generate a commit message matching repo style
---

Perform the following steps to create a commit:

1. **Read the following recent commit history** to understand the commit message style used in this repo:
<context name="recent-commit-history">
!`git log --oneline -20`
!`git log -10 --format="%B"`
</context>

2. **Analyze the following staged changes**:
<context name="current-git-status">
!`git status`
!`git diff --staged`
</context>

3. **Use conversation context** (if the conversation was not empty): Review the discussion above for any relevant details about what was being worked on, why changes were made, or specific instructions from the user. Consider/incorporate this context when generating the commit message.

4. **Generate a commit message** that matches the style and conventions observed in the recent commit history. If a clear style is not observed, prefer to use **"Conventional Commits"**.

5. **Commit the changes** using the generated message. Do NOT use GPG signing - use `--no-gpg-sign`:
`git commit --no-gpg-sign -m "YOUR_GENERATED_MESSAGE"`

6. **Remind the user** to run manually run `gcs` (a shell alias to `git commit --amend -S --no-edit`) to sign the commit. You **do not run** this command yourself.

If there are no changes to commit, report that instead.
