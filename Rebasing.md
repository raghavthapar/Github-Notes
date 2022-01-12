# GIT REBASE

There are two ways in which git rebase is used -

1. Alternative to merging
2. As a cleanup tool

Git Rebase is a useful command but we should also know **_when not to use it_**.

### What problems does Merging have that Rebasing solves?

- If the master branch is active, which leads to lot of merge commits in the feature branch, so the feature branch's history is muddied
- Rebasing rewrites the history of the branch.
- Rebasing a feature branch would mean that the feature branch starts at the tip of the master branch. So Git makes new commits for the feature branch which ensure that the work is linear.

### When not to Rebase: The Golden Rule

Rebasing should not be used if the code that you are using is used by someone else too.

**\*Never rebase commits if those commits have been shared with someone else**

## Interactive Rebase

### Rewriting History

With Git Rebase, we can -

1. Rewrite
2. Rename
3. Delete
4. Reorder Commits

Command used to do this - `git rebase -i HEAD~n` (n - no. of commit before HEAD and -i for interactive)

Once we are in the process of rebasing we get a list of commits (depending on what number of commits you have gone back), we need to use some commands. They are -

1. **pick** - use the commit
2. **reword** - use the commit but edit the message
3. **edit** - use commit, but stop for ammending
4. **fixup** - use commit contents but join with the previous commit and discard the changes
5. **drop** - remove the commit
