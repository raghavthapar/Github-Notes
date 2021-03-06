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

## Hashing Functions

- Hashing functions map input data of some arbitrary size to fixed size values
- Git uses a hash function called `SHA-1`
- SHA-1 always generates 40-digit hexadecimal values
- Commit hashes are output of SHA-1

\*\* Git is a key value data store. We can store anything in Git and then it provides us a unique key which can be used to retrieve that piece of information from Git.

### `echo '<text>' | git hash-object --stdin -w / git hash-object <filename> -w`

This stores the text/file in a Git directory and also returns a hash that is eventually stored in the objects directory of the .git folder

### `git cat-file -p <object-hash>`

This command returns the data that is stored in the hash that we have provided it

## Blobs

- Abbreviation of Binary Large Objects.
- These are the object types which Git uses to store content of our files
- These don't even store the name of the file or any other data related to it. It just stores the contents of the file

## Trees

- Trees are Git objects that are used to store the contents of a directory
- A tree contains pointers that contains blobs and trees
- It also keeps track of the names of the files/directorties

### `git cat-file -p master^{tree}/hash`

This command gives us the most recent tree and the info that it stores

### `git cat-file -t <hash>`

This command tells us the type of the object that hash is storing/referencing

## Commits

- It combines the tree with the information about the context that led to that tree in the first place
- They store -
  1. Tree that has the contents of that commit
  2. A reference to the parent commit
  3. The author
  4. The commiter
  5. The commit message
