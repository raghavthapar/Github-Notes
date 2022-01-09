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

Command -

### `git push remote <local-branch>:<remote branch>`

- Git push can be automated too. It can be done using the -u option on the git push command once.

Command -

### `git push -u <branch-name>/ <local-branch> : <repo-branch>`

1. `-u` stands for 'Upstream'
2. This tells git that whenever we say _git push_ then it knows that what branch to push on and to to which remote
3. Not only this, but if we want to send our local branch data to some other branch and not the same branch, upstreaming comes in handy

**Note**: When cloning an existing repo, the remote is already configured

## Remote Tracking Branch

- When we clone a branch, from Github or somewhere else, we get 2 pointers - the master and the origin/master.
- `master` - is a local branch reference and can be moved around by us.
- `origin/master` - this is known as a **Remote tracking branch**. It is a reference to the state of the master branch on the remote(aka hosted repo).
- In layman terms, it is just a bookmark pointing to the last known commit on the master branch on origin. We can't move it by ourselves.
- They follow the pattern `<remote>/<branch>`
- If we are ahead in our local repo and we want to see what the repo looked like on <remote>/<branch> then we can just simply checkout to it.

Commands -

### `git branch -r` (To see all the local and remote branches)

### `git checkout <remote>/<branch>` (To go back to the most recent commit of remote)

## Remote Branches

- Remote branches are something that when we clone the remote repo, they don't show up as our normal branches. Only the main branch shows up if we run the command git branch.
- Now, the main branch is the one that points to all the remote branches beacause we have not told git that we want branches for other remote branches as well.
- To make a branch that will point to the same remote branch we use -

### `git switch <remote-branch-name>`

### `git checkout <remote-name>/<remote-branch-name>`

- Through these commands, we tell Git that we want a branch that can point to the remote branch of the same name.
