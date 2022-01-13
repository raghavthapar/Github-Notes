# BEHIND THE SCENES OF GIT

## CONFIG FILE

The config file is something that remains from repo to repo. It contains the information of the user and some pretty general stuff. The config file is both local and global (different files).

## REFS FOLDER

- This is also there in the .git folder
- The **Heads** folder inside the refs folder contains a file for every branch and that file contains the recent commit hash
- It also contains a remote folder (which keeps track of the progress on the branches that we don't have on our local repo) and a tags folder in which there is a file for every tag that we have made

## HEAD File

- HEAD is a file that keeps track of where HEAD points
- HEAD usually points to the branch pointer which further points to the recent commit on that branch
- If we are in checkout mode, then HEAD refers to a particular commit

## OBJECTS Folder

- Is the core of the Git
- This directory contains all the repo files, commits in the repo and much more
- The files are all compressed and encrypted in this folder
- The files are not the snapshots of the differences but actual files

- 4 types of Git Objects -
  1. Commit
  2. Tree
  3. Blob
  4. Annotated Tags