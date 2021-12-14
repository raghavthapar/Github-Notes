# Some md notes -

- **For bold**
- _For Italics_
- ~~Strikethrough~~
- ![ImageName](URL)
- > Quotes
- `forEach()` Writing code

# Terminal Crash Course

## Commands for the Git Bash Terminal

1. clear - clears the screen
2. pwd - present working directory/print working directory
3. cd - change directory. Eg. cd folderName
4. cd.. - Backspace for the terminal. Takes us one folder back
5. start. - Opens the current directory that you are in
6. touch <fileName> - Creates a file in the directory
7. mkdir <directoryName> - Creates a new folder
8. rm <filename> - Deletes the file with the name provided
9. rm -rf <directoryName> - rm command with flags (r-recursive f-force)

# Git Repository

- Repository is a workspace which tracks and manages files within a folder.
- A new project means a new repository. Different repositories have different histories and content.
- Is like a story. A new story has different characters, different storyline etc.
- Any amount of repositories can be created.
- Its encapsulates all the things that are in the project.
- A new folder doesn't mean that a new repository is created. We need to tell Git that we need to make a repo in that project folder.

# Git Commands

## git status

- Gives info on the current status of a git repo and it's contents.
- If we are not in any repository, then it tells that the folder we are is not a git repo (Add screenshot here).
- If we are in a repo, then it gives us the info of the branch, repo etc.

## git init

- Used to initialize a new git repo.
- The first thing that we do before doing anything else. Initalizing a repo is the initial step to git managing the stuff.
- Needs to be done oncen only per project/folder.
- This command needs to be executed in the top level folder that consists all other files of the project.

<!------------------ NOTE ----------------------->

-> Usually when we do this kind of stuff, it shows nothing in the folder that we initialize the repo in.
-> git init creates an empty .git directory. As the folder's name is preceeded with (.), the folder is hidden. But we can look it up using ls -a.
-> If the .git folder is deleted then the git history also gets deleted.

<!----------------------------------------------->

- Once a directory has been made into a git repo, then git will watch everything that happens in that directory including the child, grandchild and all the subdirectories of sudirectories.

[Note] -
**Do not initialize another repo inside of an already existing repo**
_Always use the git status command to verify if you are inside a repo or not_

Reason - Git can get confused and hence things can go wrong. If you do it by mistake then you can delete the .git folder inside the sub-directory that you initialized by mistake.

## git commit

1. git commit basically means adding a snapshot of your project at that moment.

2. Usually takes a message alongside that just to make sure what we are commiting although it means nothing at all.

> Difference between Commit and Saving a file.

- There is actually a lot of difference between both of them. We save files all the time. Commit does not mean saving a particular file. Commit means that we our grouping the changes that we have done to a folder overall and adding it as a savepoint in time to revisit if necessary.
- Example _Save can be done on a single file whereas commit can mean that multiple changes have occured throughout multiple files say html, js and css files alongside some images are added into the folder._

3. Commit is a multi-step process. Work on stuff(Make new files, edit delete etc.), Add changes (grouping the changes) and commit(Commiting everything that was previously added).

4. We can group specific changes together. Not necessarily all the changes need to be commit at a single time.

5. **git add** is used to group the changes. **git commit** is used to commit the grouped changes.

6. Commiting in a nutshell - PWD [gitadd] -> Staging Area [gitcommit] -> Repository

7. Used to actually commit the changes from the staging area.

8. `git commit -m "Message for the commit"` - -m flag allows us to pass an inline commit message.

## git add

- Used as `git add file1 file2 ...`

- git add does not mean commiting the changes. This is just grouping the changes together so that they can be committed together.

- _git add . is used to stage all the changes at once._

## Git Messages

- Not necessarily a command but an important part of committing.
  > Messages summarize or describe the changes that we have done in that commit

## git log

- git log is a command that shows the timeline of what changes have been committed and what messages have been included with those commits.
- Shows the whole history of the repository.
