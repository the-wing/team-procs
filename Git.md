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
To do work, you will cut a new branch off of `staging`. Once you have passed code review and UAT, you will merge your feature branch back into `staging`. We try to avoid branching new feature work off of other feature branches as much as possible so make sure during [Sprint Planner](Sprint.md) that tickets are written and prioritized in such a way that allows for this.

### Develop
Some of our projects lack preview links for pull requests. In these instances, you should merge your in-review feature branch into the weekly `develop` branch for UAT. This branch is pruned and reset to `staging` 

## Workflow Example
Lets say you are picking up a new ticket from Jira, WING-123:

```
$ git checkout staging
$ git pull --ff-only
$ git checkout -b WING-123-some-new-feature
$ git push -u origin WING-123-some-new-feature
```

All of your commit messages should be prepended with the `[Ticket Number]` so in this case:

```
$ git commit -m "[WING-123] added migration for new feature"
```

If you want to keep your feature branch up to date with the latest version of `staging`, you should use the rebase method instead of a merge method. Here is an example of updating our feature branch to include the latest changes from `staging`.
```
$ git checkout WING-123-some-new-feature
$ git fetch
$ git rebase origin/staging
$ git push -f
```

NOTE: you will need to force push your branch after the rebase. Make sure you alert other engineers who may be pairing with you before you force push.

Open pull requests against `staging` early and give them tag of WIP (work in progress). In the case that your repo does not have automated preview links, you may need to do a manual merge of your work onto the `develop` branch for UAT testing. To do this:

```
$ git checkout develop
$ git pull --ff-only
$ git merge WING-123-some-new-feature 
$ git push
```

Once you have gotten full approval on all fronts (code, UAT, design) you may merge your feature work into staging using the Github pull request merge button. 

## Tips and tricks
Because we want to rebase or local version of `develop`, `staging`, and `master` off of the remote version, you are encouraged to add the following to your global git config:

```
$ git config --global branch.autosetuprebase always 
$ git config --global pull.rebase preserve
```
