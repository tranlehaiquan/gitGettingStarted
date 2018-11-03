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

## Operation

`git init` for create and git folder
`git status` for status files (untrack, modified, staged)
`git add <file>` for add files to staged