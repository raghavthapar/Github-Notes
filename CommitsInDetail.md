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