# MERGING

## What is Merging?

- Merging is used to incorporate changes together from different branches.
- For e.g. Lets say there 2 branches: A and B. Branch A has feature 1 and branch B has feature 2 and we want both the features together. Hence, by merging, we will get the result feature 1 + feature 2.
- `git merge` is the command that is used
- Important points ->

  1. We merge branches and not specific commits
  2. We always merge to the current HEAD branch

- If we have to merge the master and a feature branch, then we must:

  a. Switch to master (or the branch we want to merge into)
  b. Use the git merge command to merge the changes into the current branch.

- If a branch has 3 commits and some other branch has 2 commits, then after merge the branch will have 5 commits.

## Merge Commits

- Not all merges are fast-forward merges.
- This kind of merge happens when there is a some kind of untracked progress on the branch we are trying to merge into.
- E.g. 2 branches: master and bugfix. We want to merge the bugfix branch with master branch but post making of the bugfix branch, there is some kind of work that has been done on the master branch. This kind of merge is not fast forward.

- If there is no conflict, then a new commit is done, also known as the **`merge commit`**
- Git might or might not perform a prompt that allows you to write a message (regarding message)
- Visualization - ![Visualization](2022-01-02-11-35-12.png)

## Merge Conflicts

- Merge conflicts happen when we changes do not merge with ease. i.e. That the changes that have occurred in the branches might have some kind of conflict or some kind of different changes that do not fit together automatically.
  ![Conflict Message](2022-01-02-12-37-09.png)
- Above is the message that appears when there is a conflict
- Conflict markers appear in the file that we are trying to merge telling us what kind of the changes are causing the conflict for both branches

- Fixing a conflict:

  1. Open up files that have conflict in it
  2. Edit the file and keep the changes that you want from the branches. Content of both branches can be kept too. It is up to how we want it
  3. Remove the conflict markers from the file
     `<<<<<<<HEAD(The current branch file)` |||||||||
     `>>>>>>>BranchName(The incoming changes)`
  4. Add changes and make the commit

- ![Conflict markers](2022-01-02-20-02-57.png)
- We can also use VS Code to make the changes with the options provided on the top of the conflict file
