# Undoing Changes and Git Travelling

## `GIT CHECKOUT COMMANDS`

Git checkout has many uses -

### `git checkout <commit hash>`

- Can be used to view any commit that we have done.
- After doing this we get in a mode of _Detached HEAD_

Detached Head means that HEAD is no longer referencing a branch pointer, **it is referencing a commit**. And to get HEAD back to pointing to a branch, we can just simply switch to any branch.

- If we are in the detached HEAD mode then we can no longer make changes on the file. If we want to make some changes, then we can make a new branch and then do the required work.

### `git checkout HEAD <filename>/ -- <filename>`

- This command is used to revert the changes that we have done to the file back on where it was on it's previous HEAD.
- We revert back to the file that was there initially when we had all our work committed.

## REFERENCING COMMITS RELATIVE TO HEAD

- This is done using the `'~'(tilde)` sign.
- We can reference a commit by using where the head currently is.
- For eg. We have 4 commits on master and HEAD is pointing to the most recent commit. Then the commit before that would be HEAD~1, before that
- For eg. We have 4 commits on master and HEAD is pointing to the most recent commit. Then the commit before that would be HEAD~1, before that HEAD~2 and before that, HEAD~3 and so on...

![Example](2022-01-05-12-33-41.png)

- If we do `git switch -`, then we will come back to where we left off i.e. the orignal position of the HEAD

## `GIT RESTORE`

- git restore is a command that replaces git checkout.
- **`git restore <filename>`** will restore the content to the most recent commit.
- **`git restore --source commitHash/HEAD~n <filename>`** will take the file back to a particular commit that we want. And to revert back to the orignal method, we can just use the first command.

- **`git restore --staged <filename>`** - this command unstages a file that is staged to be committed.

## `GIT RESET`

- Resets a repo back to a particular commit. Used to undo commits.

### `git reset <commit-hash>`

- The above reset is called a regular reset and although it reverts the commit, it does keep changes in the file/working directory.
- The no. of commits reduced till the commit we provided.
- This is used if we want to keep our work but we want to change the branch etc. type of reason

### `git reset --hard <commit-hash>`

- This is known as the hard commit.
- In this, we undo the commits and the changes that were present in the regular reset will also be deleted alongside the commit.
- This should be done really carefully as the changes are lost and cannot be recovered.

## `GIT REVERT`

- Similar to git reset but approach is different.

### `git revert <commit-hash>`

- Git revert creates a new commit which reverses the changes that were done in the commit that we are trying to revert.
- In Layman, git revert still keeps the changes we want to revert in the history of the repo but makes a new commit where those changes don't exist at all.

- git revert can cause some conflicts as well, especially when reverting from a long time ago.
