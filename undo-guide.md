# Git Undo Guide

| Situation | Command | Safe after push? (yes/no) |
| :--- | :--- | :--- |
| Discard unstaged changes in a working file | `git restore <file>` | yes (local only) |
| Unstage a file without losing its changes | `git restore --staged <file>` | yes (local only) |
| Edit the last commit message or add forgotten files | `git commit --amend` | no |
| Safely undo a public commit by creating a new opposite commit | `git revert <commit>` | yes |
| Undo the last commit and keep changes staged | `git reset --soft HEAD~1` | no |
| Completely delete recent commits and all local changes | `git reset --hard HEAD~1` | no |
| Temporarily save uncommitted changes and clean working directory | `git stash` | yes (local only) |
