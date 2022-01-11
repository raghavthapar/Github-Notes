# GITHUB COLLABORATION AND WORKFLOWS

## Centralized Workflows

---

- The most simple and basic of workflow
- Everyone works on the master branch (or a single branch)
- Good for tiny teams

- The shortcomings of this method are -
  1. Lot of time is spent in merging and solving conflict
  2. Main codebase is always at risk and no experiments can be done with the project
  3. Collaboration can only be possible if others get the incomplete code of one collaborator.

## Feature Branches

---

- Here, no one works on the master branch. For every tiny to big modification, the work is **done on different branches**
- Master/Main branch is treated as the official project history and must contain a working project on it
- Team mates can collaborate even on incomplete code

- Feature branches should be merged accordingly after discussion with the team mates.
- Usually, after merging, the branch is deleted but it is up to us if we want to delete it or not

### Pull Requests

1. Feature built into Github and GitBucket. Not native to Git itself
2. PRs are requests to merge your branch with the main branch but it goes to the project manager on Github which allows him to see what changes have been done etc.
3. PRs can have discussions over them and several other team members can also be included.
4. A PR can be rejected or accepted by the manager
5. If a PR is aaproved, then the changes can be merged successfully.
