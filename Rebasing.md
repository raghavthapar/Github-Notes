# GIT REBASE

There are two ways in which git rebase is used -

1. Alternative to merging
2. As a cleanup tool

Git Rebase is a useful command but we should also know **_when not to use it_**.

### What problems does Merging have that Rebasing solves?

- If the master branch is active, which leads to lot of merge commits in the feature branch, so the feature branch's history is muddied
- Rebasing rewrites the history of the branch.
- Rebasing a feature branch would mean that the feature branch starts at the tip of the master branch. So Git makes new commits for the feature branch which ensure that the work is linear.
