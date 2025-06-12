# SVN

## Install

```
sudo apt install subversion
```

## SVN checkout

```
sudo svn checkout --username <name> <url>
```

## SVN update

Update your local working copy with any changes from the repository.
This will automatically merge changes with your local changes if possible.

```
sudo svn update
```

## SVN status

Get status of files, i.e. how your working copy compares to the last time you
checked the repository.

```
sudo svn status
```

## SVN add

Add new files or directories to version control.

```
svn add <file>
```

## SVN revert

Undo local edits, revert to last image of repository.

```
sudo svn revert <file>
```

## SVN commit

Commit changes in your local working copy into the repository.
Use the “-m” option to write a message about what you changed.

```
svn commit -m "your message"
```
