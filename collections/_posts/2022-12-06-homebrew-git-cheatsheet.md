---
layout: post
title: "Homebrew Git cheat sheet"
comments: false
description: "Possibly useful git commands."
keywords: "git, cheatsheet"
---

There are a ton of very useful git cheat sheets around, on top of a great documentation (which is where alongside StackOverflow I find myself when things get fun). I started putting together this list ~3 years ago and finally decided to move from my notepad to here. I'll be updating this over time.

# Branches
## Permanently remove commits from remote branch
```shell
git reset --hard <last.working.commit.id>
git push --force
```

## Push local branch to remote
```shell
git push -u origin <branch.name>
```

## Delete local branches for which remote tracking branches have been pruned
Source: [StackOverflow](https://stackoverflow.com/a/46192689/4186734) 
```shell
git checkout main
git fetch -p
git branch -vv | grep ': gone]'|  grep -v "\*" | awk '{ print $1; }' | xargs -r git branch -d
```

# Tags

| Goal | Command |
| :--- | :--- |
| List | `git tag -l` |
| Create annotated tag | `git tag -a <name> -m "<tag.message>"` |
| Push tag to remote (git push doesn't work) | `git push origin --tags` |
| Delete tag local | `git tag -d <name>` |
| Delete tag remote | `git push origin --delete <name>` |

# Commits
## Undo local, unpushed commit(s)
`n` is number of commits to undo. `--soft` keep changes, `--hard` discards commits and doesn't keep changes.
```shell
git reset --soft HEAD~n
```

## Check out file from remote
```shell
git checkout origin/<branch.name> -- <path.to.file>
```

# Rebase
**NOTE:** I'm not a rebase expert, create backup tag before forcing any changes & proceed with caution.

## Rebase
1. `git checkout <rebase-target-branch>`
1. `git checkout -b <intermediate-branch>`
1. Cherry-pick from `<work-branch>` into `<intermediate-branch>`
1. `git checkout <work-branch>`  
1. `git reset --hard <intermediate-branch>`
1. `git push --force`

## Rebase in squash-commit repo
There might be an easier approach, but this has worked quite well. In a repo where PR/MRs follow squash-commit policy, merges from `main` to `feature` branches aren't desired, and `feature` branch is `n` merges behind `main`. To perform a rebase closer to what one would expect (i.e., only `feature` branch changes on top of `main`, without existing commits re-hashed):
- Rebase `feature` onto updated `main`
- Run `git reflog`, find commit with most recent `feature` branch commit, note ref (i.e., `HEAD@{25}`)
- Type `q` to exit `reflog`
- Run `git reset --hard HEAD@{n}` to discard duplicate changes
- Run `git push --force` to update remote and discard duplicate changes in remote

# Submodules
## Import submodules recursively
`git submodule update --init --remote --recursive`

## Undo submodule updates locally
`git restore . --recurse-submodules`

Source: [StackOverflow](https://stackoverflow.com/questions/134882/undoing-a-git-rebase).