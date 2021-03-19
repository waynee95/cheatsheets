# Git Cheatsheet

## Create a repository

```bash
$ mkdir <name>
$ cd <name>
$ git init
```

## How to commit changes

```bash
$ git status              # too see which files changed
$ git diff <file>          # to see the changes
$ git add <files>
$ git commit -m <message>
```

`git commit -a` will automatically add all modified files, but not new ones.

## Reset local repo to remote master

```bash
$ git fetch origin
$ git reset --hard origin/master
```

## Delete local branch

```bash
$ git branch -d <branch_name>
```

## Add file to last commit

```bash
$ git add <left_out_file>
$ git commit --amend
```

## Unstage file

```bash
$ git reset <filename>
```

## Revert local commit

```bash
$ git reset HEAD~1
```

## Remove untracked files

```bash
# Print out which files would be removed
$ git clean -n -d <path>
# Actually remove the files!
$ git clean -f <path>
```
## List number of LOC changed 

```bash
$ git diff --shortstat
```
