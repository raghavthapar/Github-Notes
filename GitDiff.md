# GIT DIFF

## What is Git Diff? Why is it used

- Git diff is a command to view changes between commits, branches and files.
- Git diff lists all the changes in our working directory that are **_not staged_** for the next commit.

## Reading git diffs

1. This is the first line of the git diff and it tells about the files that are being compared.![Output](2022-01-03-08-48-43.png)

2. The next line is the metadata of the files being compared.![Output](2022-01-03-08-52-55.png)

3. The next line indicates that the file 'a' will be depicted by --- and file 'b' will be by +++. ![Output](2022-01-03-08-55-01.png)

4. These are known as chunks. And they provide a little bit of context as to where the changes have been done. A chunk contains lines that are not changed too. ![Output](2022-01-03-08-57-40.png)

5. Lines that begin with `'-'` are from file 'a' and those with `'+'` are from file 'b'. ![Output](2022-01-03-09-02-31.png)

6. The chunk header means that from file 'a' from line 3, 4 lines are extracted and from file 'b' from line 3, 5 lines are extracted. ![Output](2022-01-03-09-05-48.png)

## git diff with options

1. `git diff HEAD` - This command shows all the staged and unstaged changes since our last commit.
