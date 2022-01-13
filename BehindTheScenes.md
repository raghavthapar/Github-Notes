# BEHIND THE SCENES OF GIT

## CONFIG FILE

The config file is something that remains from repo to repo. It contains the information of the user and some pretty general stuff. The config file is both local and global (different files).

# REFS FOLDER

- This is also there in the .git folder
- The **Heads** folder inside the refs folder contains a file for every branch and that file contains the recent commit hash
- It also contains a remote folder (which keeps track of the progress on the branches that we don't have on our local repo) and a tags folder in which there is a file for every tag that we have made
-
