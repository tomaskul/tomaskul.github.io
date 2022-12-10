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
```powershell
git reset --hard <last.working.commit.id>
git push --force
```

## Push local branch to remote
```powershell
git push -u origin <branch.name>
```

## Delete local branches for which remote tracking branches have been pruned
Source: [StackOverflow](https://stackoverflow.com/a/46192689/4186734) 
```powershell
git checkout main
git fetch -p
git branch -vv | grep ': gone]'|  grep -v "\*" | awk '{ print $1; }' | xargs -r git branch -d
```

# Tags
| Goal | Command |
| ----- | ----- |
| List | `git tag -l` |
| Create annotated tag | `git tag -a <name> -m "<tag.message>"` |
| Push tag to remote (git push doesn't work) | `git push origin --tags` |
| Delete tag local | `git tag -d <name>` |
| Delete tag remote | `git push origin --delete <name>` |

# Commits
## Undo local, unpushed commit(s)
`n` is number of commits to undo. `--soft` keep changes, `--hard` discards commits and doesn't keep changes.
```powershell
git reset --soft HEAD~n
```

## Check out file from remote
```powershell
git checkout origin/<branch.name> -- <path.to.file>
```