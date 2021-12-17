# Answer 1
We should create new branches for features off of production branch. Because the master branch is for testing and should only contain executable codes that are finished. We use the production branch to merge the new features and when that particular version of the branch is executable and considered finished, we merge it into master for later testing.

```
  git checkout production

  git pull

  git branch feature

  git checkout feature
```