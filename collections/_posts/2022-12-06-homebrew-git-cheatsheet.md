---
layout: post
title: "Homebrew Git cheat sheet"
comments: false
description: ""
keywords: "git, cheatsheet"
---

There are a ton of very useful git cheat sheets around (on top of a great documentation).

# Branches
## Permanently remove commits from remote branch
```cmd
git reset --hard <last.working.commit.id>
git push --force
```

## Push local branch to remote
```cmd
git push -u origin <branch.name>
```

## Delete local branches for which remote tracking branches have been pruned
Source: [StackOverflow](https://stackoverflow.com/a/46192689/4186734) 
```cmd
git checkout main
git fetch -p
git branch -vv | grep ': gone]'|  grep -v "\*" | awk '{ print $1; }' | xargs -r git branch -d
```

# Tags
| Goal | Command |
| --- | --- |
| List | `git tag -l` |
| Create annotated tag | `git tag -a <name> -m "<tag.message>"` |
| Push tag to remote (git push doesn't work) | `git push origin --tags` |
| Delete tag local | `git tag -d <name>` |
| Delete tag remote | `git push origin --delete <name>` |

# Commits
## Undo local, unpushed commit(s)
`n` is number of commits to undo. `--soft` keep changes, `--hard` discards commits and doesn't keep changes.
```cmd
git reset --soft HEAD~n
```

## Check out file from remote
```cmd
git checkout origin/<branch.name> -- <path.to.file>
```