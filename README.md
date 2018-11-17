# DVCS (distrubute version control system)

Before git store, git do checksume, by called a SHA-1 hash.

Git only add data

## Three states

- Commited, modified, and staged.
```
Committed means that the data is safely stored in your local database. 
Modified means that you have changed the file but have not committed it to your database yet. 
Staged means that you have marked a modified file in its current version to go into your next commit snapshot.
```

- Git config: (local, global, system)
Simple config

```
[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
[user]
	name = tranlehaiquan@gmail.com
```

1. Local
In folder ./git/config

2. Global
~/.git in linux
$HOME/.gitconfig in window

3. System

Setting a user name with 

Global `git config --global user.name "John Doe"`
Local `git config --local user.name "John Doe"`

To check setting user `git config --list`

- Git status
Untrack, modified, deleted

## Operation

- `git init` for create and git folder
- `git status` for status files (untrack, modified, staged)
- `git add <file>` for add files to staged
- `git reset HEAD -- <file>` which effectively reverts git add and prevents the changes to this file from participating in the next commit.
- `git log`
```
git log -p
git log --stat
git log --pretty
``` 
- `git commit --amend` edit the last commit with the new one
- `git checkout -- <file>` to checkout (revert file want)
- `git remote`

`git remote` To see which remote servers you have configured,
`git remote -v` To shows you the URLs
`git remote add [shortname] [url]` to add new remote git repository

- `git fetch [remote-name]` to get data from remote project
- `git push [remote-name] [branch-name]` to push
- `git remote rename [remote-name] [remote-newname]`
- `git remote rm [remote-name]` 

Make git tag:
Git uses two main types of tags: lightweight and annotated. A lightweight tag is very much like a branch that doesn’t change — it’s just a pointer to a specific commit. Annotated tags, however, are stored as full objects in the Git database. 

`git tag` to show tag
`git tag -a v0.1 -m [message]` to create an annotated
After that we can use `git show v0.1`

## Branch

- `git branch` to list all branch
- `git checkout <name-brand>` to switch to that branch
