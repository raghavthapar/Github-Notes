                                       ================== > COMMITING IN DETAIL < ==================

## Atomic Commits

- Each commit should have only one feature, change or fix.
- Keep each commit fixed on a single thing

Why?
It makes easier to see what changes you have done so far and then if needed, the rollback is also easy.

## How to write commit messages?

- Always keep the messages in present tense.
- The final say comes in your preference.
- Present tense is the prime choice tho.

## Closer look into Git Log

> git log --pretty=oneline

- The above command provides short logs and just a part of the commit message
- Makes it easy to see the history much more clearer

<!-- Just making some changes to reflect in the GUI part of the git -->

## Ammending Immediate Commits

- Ammending can be required if we miss something in a commit or the message is missing.
- We can redo the previous commit using the `--amend`
- We can only amend the previous commit

## Ignoring files using Git

- We do not want to add any kind of files tkhat are sensitive or that will just increase the load of the repository or has no use being in the repository.
- The files can be - _Secrets, API Keys, credentials, OS files, log files, dependencies and packages(for eg. Node and all)_

- We make a `.gitignore` directory all by ourselves and we type in the names of the files/folders that we don't want to track at all. We can keep adding files in that file itself and track that in git.
