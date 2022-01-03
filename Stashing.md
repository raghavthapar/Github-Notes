# STASHING

## Need of Git Stash

- There are times when we need to switch to a branch but the work on the current branch is premature/not ready to be commited. There are 2 things that could happen -
  1. If they are non-conflicting changes/work, then the progress will come over to the branch we want to switch to.
  2. If there is some conflicting work, then Git won't let us change our branch. It would want us to either commit the changes or _stash_ our changes.

## Commands

1. `git stash`

   - Helps to save the changes that we don't want to commit and we can come back to them later.
   - Running it will take all the uncommitted changes (staged/unstaged) and stash them, reverting the chnages in the working copy.
   - Same as git stash save
   - After stashing, the work that has not been committed will disappear.

2. `git stash pop`

   - Removes the most recently stashed changes in the stash and reapply them to the working copy.
   - The stash becomes free of the most recent change and it can't be retrieved after that.

3. `git stash apply`

   - This is used to apply the changes to a branch but the stash does not get rid of the most recent stash.

## Multiple Stashing

- Multiple stashes can be done and they can be popped out in the order we saved them into.
- This works like a queue and has First In First Out technique.
- We can see all the stashes using `git stash list`.
- We can apply specific changes using the stashing ID via `git stash apply stash@{2}` (example)
