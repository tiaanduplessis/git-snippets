# git-snippets

> Collection of useful git snippets

## Table of Contents

- [About](#about)
- [Snippets](#snippets)
- [License](#license)

## About

This is just a bunch of `git` related snippets. Collected from around the internet.

## Snippets

### Delete untracked files

```sh
git clean -fn
```

### Set local branch to track another local branch

```sh
git branch --set-upstream BRANCH ANOTHER_BRANCH
```

### Clear git cache and add files back

```sh
git rm -r --cached .
git add .
git commit -m "fix .gitignore"
```

### Undo the last local commit

To unstage changes

```sh
git reset HEAD~1
```

To completely undo

```sh
git reset --hard HEAD~1
```

### Create tracked local branch

```sh
git checkout -b NEW_BRANCH
git push --set-upstream ORIGIN NEW_BRANCH
```

### Undo a merge

```sh
git merge --abort
```

### Compare commit messages on two branches

```sh
git log --cherry-mark --oneline A_BRANCH..ANOTHER_BRANCH
```

### See the files changed in a specific commit

```sh
git diff-tree --no-commit-id --name-only -r THE_COMMIT_ID
```

### Get commits per author

```sh
git shortlog -sn --all --no-merges
```

### Configure your details

```sh
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

### Update and merge your current branch with a remote

if `ORIGIN` is the remote repository, and `MASTER` the remote branch.

```sh
git pull ORIGIN MASTER
```

### See previous git commands executed

```sh
history | grep git
```

### Delete all untracked files and directories

```sh
git clean -f -d
```

### Push to new remote branch and set as upstream

if `ORIGIN` is the remote repository, and `MASTER` the remote branch.

```sh
git branch -u ORIGIN/MASTER
```

### Search for string

```sh
git grep 'STRING'
```

### Get commits for a author

```sh
git log --author 'AUTHOR'
```

## License

MIT