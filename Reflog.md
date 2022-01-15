# GIT REFLOG

- Git keeps track of the changes in the tips of the branches and other reference and keeps a log. These logs can be obtained by git reflog command.
- These logs are under .git directory and can be seen under the HEAD file
- It tracks any movement that we make with HEAD in our repo
- It not only keeps the track of the HEAD, but each of the individual branches

## Limitations

- Reflogs are local and do not carry on if we are working in a collaboration meaning that you won't be able to see the reflogs of other contributors
- They expire after 90days but this can be changed too
