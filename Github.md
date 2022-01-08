# GITHUB

## What is Github?

- Hosting platform for git repos.
- We can put them on Cloud which allows us to share them, access them anywhere we want and collaborate with people.
- Just an online place alongside Gitlab, BitBucket and Gerrit.

## Why to use it?

- Collaboration is the biggest reason as we can share our work with anyone in the world.
- Open Source Projects(where codebase is available to make contribuitions) E.g. React
- Gives exposure and showcases your work that you have been doing.
- Looks really good on your resume
- Helps to stay up to date, technology wise.

## Cloning

- Using this, we can get a copy of any public repo on the local machine.
- This is when the repository is already existing on Github.
- Cloning initializes a new repo automatically on our machine.
- Cloning a repo gives us the access to the whole history of the repo.
- Make sure that you are not inside a repo when you clone a repo.

Command -

### `git clone <git-repo-url>`

- Anyone can clone any repo on Github (Private ones do not show up at all).
- git clone is not bound to Github and we can clone any repo that is hosted anywhere.

## Creating Repos on Github

- If an existing repo exists then ->

  1. Create a new repo on Github
  2. Connect your local repo (add a remote)
  3. Push your changes to Github

- If no repo exists ->

  1. Create a brand new repo on Github
  2. Clone the repo to our machine
  3. Do work locally and push changes to Github

## Git Remotes

- Before we can push, we need to tell Git about the remote repo on Github i.e. we need to setup a destination to push up to.
- This destination is referred to as remote.
- This remote is simply a URL where a repo is hosted.

- Commands -

  1. ### `git remote`
  2. ### `git remote -v` (verbose for more info)
  3. ### `git remote add <name> <url>` (To add a new remote)
  4. ### `git remote rename <old> <new>` (For renaming the remote)
  5. ### `git remote remove <name>` (To remove a remote)

- `Origin` is the most common name for a remote but not the only one. The name can be kept to anything else.

## Git Push

- `git push <remote> <branch>` command is used to push the changes up to Github.
- When we push the very first time, the push command actually makes the master branch on the Github repo which at the first place **_doesn't have any branch at all_**.

- Not necessary that we push a local branch to the same remote branch, we can push it to any other local branch too.
- Command -

  1. ### `git push remote <local-branch>:<remote branch>`
