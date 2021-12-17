# Answer 1
We should create new branches for features off of production branch. Because the master branch is for testing and should only contain executable codes that are finished. We use the production branch to merge the new features and when that particular version of the branch is executable and considered finished, we merge it into master for later testing.

```
  git checkout production

  git pull

  git branch feature

  git checkout feature
```

# Answer 2
We will have to stash our changes on our current branch, then go to the bugged branch, pull it and start resolving the bug.

```
  git stash save -u "name of stash"

  git checkout feature

  git pull

  //resolve the bug and commit, then push to the feature branch

  git checkout old_branch_you_were_working_on

  git stash apply stash@{index_of_your_stash}

  //continue working on your code
```

# Answer 3
We will use the revert command to revert the merge (by adding a new commit that undoes the changes in the merge). By doing this, we will have to resolve the conflicts manually to decide what to keep and what to omit.

```
  git revert commitID_of_the_merge

  //resolve conflicts

  git add .

  git commit -m 'revert merge'
```