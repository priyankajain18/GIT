# GIT (Distributed Version Control System)

### Version Control System
It is a system that records changes to a file or set of files over time.
It allows you to revert files back to a previous state or revert the entire project back to a previous state or compare changes over time etc.

### Distributed Version Control System
In DVCS, you don’t just check out the latest snapshot of the changed files but fully mirror the repository.
Every clone is a full backup of the entire project.

### Installing

```sh
Ubuntu 14.04
------------

sudo apt-get install git-all
```

### Set Identity
Set your name and email address. Every Git commit uses this information.

```sh
git config --global user.name "your_name"
git config --global user.email your_email

```

```sh
git config --list

user.email=your_email
user.name=your_name

or

git config user.name

your_name
```

### Repository
It is a kind of a database where your DVCS stores all the versions of your project.
In Git, the repository is just a simple hidden folder named ".git" in the root directory of your project.

```sh
git init

It creates a new subdirectory named .git in the root directory of your project.
```

### Commit
A commit is a wrapper for a specific set of changes. The author of a commit has to comment what he did in a short "Commit Message".

Everything in Git is check-summed before it is stored and is then referred to by that checksum.
The mechanism that Git uses for this check-summing is called a **SHA-1** hash. This is a 40-character string composed of hexadecimal characters (0–9 and a–f).

```sh
For Example:

24b9da6552252987aa493b52f8696cd6d3b00373
```

Git stores everything in its database not by file name but by this hash value.


> **Note:** Git has three main states:
> - Modified - It means that you have added/changed a file but have not committed it to your database yet.
> - Staged - It means that you have marked a modified file in its current version to go into your next commit.
> - Committed - It means that the data is safely stored in your local database.


> **Note:** Status of a file:
> - untracked - These are the files that are newly created or ignored.
> - tracked


### .gitignore ###
Ignore specific file - Provide the full path to the file, seen from the root folder of your project.
   > path/to/file.py

Ignore all files with a certain name - Anywhere in the project. Just write down the file's name, without giving the path.
   > file.py

Ignore all files of a certain type - Anywhere in the project.
   > *.swp

Ignore all files in a certain folder
   > path/to/folder/*

