# How we use Git

Git is an extremely powerful tool with many possible workflows. Our Git workflow should make it easier to achieve or larger goal with tickets/work: merging tickets quickly.

Generally, we stick to Atlassian's (Simple Git Workflow)[https://www.atlassian.com/blog/git/simple-git-workflow-simple]. Due to the nature of our release process, there are some additional steps one needs to take during the review portion of the dev cycle.

## Branches
We use three types of branches for our workflow.

### Master
The `master` branch should be deployable at any time and identical to what is on production at the moment. No one should be able to merge anything into `master` from their machine, and the commits are mostly merge commits from the release branch. 

### Staging
This branch is where all work is based, and where all fully approved work is merged.

### Feature branches
To do work, you will cut a new branch off of `staging`. Once you have passed code review and UAT, you will merge your feature branch back into `staging`. We try to avoid branching new feature work off of other feature branches as much as possible so make sure during (Sprint Planner)[Sprint.md] that tickets are written and prioritized in such a way that allows for this.

### Develop
Some of our projects lack preview links for pull requests. In these instances, you should merge your in-review feature branch into the weekly `develop` branch for UAT. This branch is pruned and reset to `staging` 

## Workflow
Once again, please read through (Simple Git Workflow)[https://www.atlassian.com/blog/git/simple-git-workflow-simple] first. 
