# GIT REFLOG

- Git keeps track of the changes in the tips of the branches and other reference and keeps a log. These logs can be obtained by git reflog command.
- These logs are under .git directory and can be seen under the HEAD file
- It tracks any movement that we make with HEAD in our repo
- It not only keeps the track of the HEAD, but each of the individual branches

## Limitations

- Reflogs are local and do not carry on if we are working in a collaboration meaning that you won't be able to see the reflogs of other contributors
- They expire after 90days but this can be changed too

## Commands

### `git reflog show HEAD/<branch-name>`

We see the log that has been stored. HEAD@{n} means that the log is showing all 1-n entries. The logs can be based on the HEAD or the branch that we want to see the reflogs for

### `git reflog show HEAD@{n}`

We can pass a qualifier and then see the reflog from that till the end. Eg if we pass 10, then the reflog will show from HEAD@{10} till HEAD@{n}
