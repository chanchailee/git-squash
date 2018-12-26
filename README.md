# Git Squash Example

## Commit Steps

```shell
    git commit -m "line1"
    git add test.txt
    git commit -m "line2"
    git add test.txt
    git commit -m "line3"
    git add test.txt
    git commit -m "line4"
    ...
    git add test.txt
    git commit -m "line100"
    git reset --soft HEAD~3
    git commit -m "commit after squash"
    git push origin master
```

## Squash Steps

```shell
git reset --soft HEAD~3
git commit -m "commit after squash"
git push origin master
```

## Explanation

**`git reset --soft HEAD~3`** means it will squash the last 3 commits to the current commit.
Thus, when you commit a message after the git squash and push to the remote/branch, it will appear on
your repository as **1** commit.