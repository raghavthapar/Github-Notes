# BRANCHING

## What is branching?

- Branching is required where we need to work on different contexts. For e.g. if we need to implement an experimental feature, or we need to do something that will break the code in some way etc.
- Branches are kind of alternative timelines for the project
- If we make changes on one branch, then it doesn't affect any other branch.
- We can merge branches as well which will result in both the branches being put together.
- Branches exists in isolation

## What is a master branch?

- We are always on a branch and the default is the master branch
- Master branch is just like any other branch
- Master branch is something that many of us use that can be the main branch where nothing should go wrong etc.
- Github renamed the master branch to 'main'
- We can also change the name of the branches according to our own choice, even the master/main one.

## What is Head->master in git log?

- HEAD is simply a pointer that refers to the current location in our repo
- HEAD in simple words is the current branch/location that we are checking out/viewing/working on
- HEAD is a pointer and a reference to the branch pointer. (The branch pointer is where a branch currently is)

## Working with branches

1. `git branch` -> this command is used to view the current branches in our repository

   - The branch that will be active will have an `*(asterisk)` in front of it

2. `git branch <branch-name>` -> This command makes a branch

   - The HEAD doesn't change due to this. The HEAD remains on the branch that we currently were in.

   - When we make a new branch, that is a reference pointer, it points to the same commit as the current HEAD is on. For e.g. Let's say we have the master branch and have 2 commits on it. The master branch (the master reference pointer) points to the recent commit, and the new branch reference pointer also points to the recent commit (See Image)
     ![Example](2021-12-19-19-49-35.png)

3. `git switch <branch-name>` -> This command is used to switch between existing branching
   - This is a new command that is used in Git.
   - When commiting in a branch, the file may or may not show the commits that you have made in mother branches.
   - Also, the file's content changes based on what branch we are in.

> It does matter where we switch from. As the contents may vary from branch to branch and what branch the new branch has been made.

4. `git checkout <branch-name>` -> This command is used for switching branches.
   - The command does a lot of stuff and hence switch is used over checkout.

\*We can create and switch to a branch at the same time. This is done using the `git switch` command with the `-c` flag (-c stands from create).

Q. What if we try to switch a branch while there are changes that are not committed to it?

A.- In this case, if we try to switch a branch, then git proceeds to show an `error` that the changes that have been done in the branch will be overwritten. Hence, it advices to either commit the changes or stash(More on this later) them.
However, if there are any `untracked files/folders`, that would not cause any kind of conflict in git, then the switch will happen easily.

5. `git branch -d <branchName>` -> This command is used to delete a branch.

   - We cannot delete the branch that we are currently are
   - If we switch and then try to delete the branch, then error pops up - **`The branch <branchName> is not fully merged`**
   - Hence, it is advised that we use the `-D` option which is equal to **--delete --force**

6. `git branch -m <newBranchName>` -> This command is used to rename a branch.

   - The only catch is that we have to be on the branch that we have to delete.
