# STASHING

## Need of Git Stash

- There are times when we need to switch to a branch but the work on the current branch is premature/not ready to be commited. There are 2 things that could happen -
  1. If they are non-conflicting changes/work, then the progress will come over to the branch we want to switch to.
  2. If there is some conflicting work, then Git won't let us change our branch. It would want us to either commit the changes or _stash_ our changes.
