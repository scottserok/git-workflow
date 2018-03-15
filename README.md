# Git

<https://git-scm.com/>

## git branch

### master

This branch is packaged and deployed to production.

### staging

This branch is packaged and deployed to staging.

### [author]/[feature name]

These branches are created locally for bug fixes and feature development.
Example feature branch: `ss/feature_branch_1`

## Workflow

### From feature development to `staging` to `master`

1. Create your feature branch off of staging. `git checkout -b
   ss/feature_branch_1`.

1. Make one or more commits on your feature branch.

1. Push your branch to origin. `git push origin ss/feature_branch_1`.

1. Create a PR against `staging`.

1. Squash and merge.

1. Create a PR from `staging` into `master`.

1. Merge. This creates a merge commit on `master` that does not exist in `staging`.

1. Create a PR from `master` into `staging`.

1. Merge. This brings the release commit into `staging`.

1. Update your local branch of `staging`. `git checkout staging && git pull
   origin staging`.

1. Create your next feature branch, starting back at step 1.
