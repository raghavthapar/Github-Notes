# Undoing Changes and Git Travelling

## GIT CHECKOUT COMMANDS

Git checkout has many uses -

### `git checkout <commit hash>`

- Can be used to view any commit that we have done.
- After doing this we get in a mode of _Detached HEAD_

Detached Head means that HEAD is no longer referencing a branch pointer, **it is referencing a commit**. And to get HEAD back to pointing to a branch, we can just simply switch to any branch.

- If we are in the detached HEAD mode then we can no longer make changes on the file. If we want to make some changes, then we can make a new branch and then do the required work.
