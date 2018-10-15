# How we use Git

Git is an extremely powerful tool with many possible workflows. Our Git workflow should make it easier to achieve or larger goal with tickets/work: merging tickets quickly.

Generally, we stick to Atlassian's (Simple Git Workflow)[https://www.atlassian.com/blog/git/simple-git-workflow-simple]. Due to the nature of our release process, there are some additional steps one needs to take during the review portion of the dev cycle.

## Master Branch
The `master` branch should be deployable at any time and identical to what is on production at the moment. No one should be able to merge anything into `master` from their machine, and the commits are mostly merge commits from the release branch. 

## Staging Branch
