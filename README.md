# Common Git Commands Summary

My quick summary of my commonly used Git commands.

 - [Git Bash Commands](#Git-Bash-Basic-Commands)
 - [Git Commands](#Git-Commands)

## Git Bash Basic Commands
| Command | Abbreviation | Description | Example(s) |
| ------- | ------------ | ----------- | ------- |
| pwd | Print Working Directory | Prints current directory's path |
| cd | Change Directory | Changes current wokring directory | [cd](#cd) |
| ls | List | Lists file contents of a directory | [ls](#ls) |
| rm | Remove | Removes a file/folder | [rm](#rm) |
| mv | Move | Moves/Renames a file/folder | [mv](#mv) |
| cp | Copy | Copys a file/folder | [cp](#cp) |
| mkdir | Make Directory | Creates a new folder | [mkdir](#mkdir) |
 
### cd
| Example(s) | Description |
| ------- | ----------- |
| cd path/to/folder/potato | The current working directory is potato |
| cd .. | Move one directory upwards (into the current folder's parent folder) |
| cd ~ | "~" sign stands for your user account's home folder |

### ls
| Example(s) | Description |
| ------- | ----------- |
| ls -al | "-l" formats the output list a little more structured and "-a" also lists "hidden" files |

### rm
| Example(s) | Description |
| ------- | ----------- |
| rm potato.txt | Removes potato.txt file |
| rm -r path/to/potato-folder | Removes potato-folder directory and its subfolders recursively, "-r" stands for "recursive" |

### mv
| Example(s) | Description |
| ------- | ----------- |
| mv path/to/file.ext different/path/file.ext | Moving file.ext |
| mv old-filename.ext new-filename.ext | Renaming old-filename.ext to new-filename.ext |

### cp
| Example(s) | Description |
| ------- | ----------- |
| cp filename.ext copy-filename.ext | Copying filename.ext and naming it copy-filename.ext |
| cp -r folder-1 folder-1-copy | Copying folder-1 and its contents recursively |

### mkdir
| Example(s) | Description |
| ------- | ----------- |
| mkdir new-folder | Create a new folder "new-folder" |

___

## Git Commands
   - [Setup and Config](#Setup-and-Config)
   - [Getting and Creating Projects](#Getting-and-Creating-Projects)
   - [Basic Snapshotting](#Basic-Snapshotting)
   - [Branching and Merging](#Branching-and-Merging)
   - [Sharing and Updating Projects](#Sharing-and-Updating-Projects)
   - [Inspection and Comparison](#Inspection-and-Comparison)
   
### Setup and Config
| Command | Description |
| ------- | ----------- |
| git config -–global user.name “[name]” | Sets the author name to be used with your commits |
| git config --global user.email "[email address]" | Sets the author email address to be used with your commits |
| git config --global -e | Opens an editor to modify the config file |
| git config --global --list | Lists all variables set in config file, along with their values. |
| git config --global alias.[user defined alias] "[command]" | Creates custom alias |


### Getting and Creating Projects
| Command | Description |
| ------- | ----------- |
| git init | Initializes a local repository |
| git clone [url] | Creates a local copy of a remote repository |


### Basic Snapshotting
| Command | Description |
| ------- | ----------- |
| git status | Shows the working tree status |
| git add [file/folder] | Adds file/folder contents to the index(staging area) |
| git add -A | Adds all new and changed files to the staging area in the entire working directory |
| git add . | Adds  all new and changed files to the staging area in the current directory |
| git add * | Same as `git add .` excluding files that begin with dot |
| git commit -m "[commit message]" | Commits with inline message |
| git commit -a | Automatically stages tracked files that have been modified and deleted and commit |
| git rm -r [file/folder] | Removes a file/folder |
| git mv [old file name] [new file name] | Renames file |


### Branching and Merging
| Command | Description |
| ------- | ----------- |
| git branch | Lists branches |
| git branch -a | Lists all local and remote branches |
| git branch -d [branch name] | Deletes a branch |
| git branch -m [old branch name] [new branch name] | Renames branch |
| git branch [new branch name] | Creates a new branch |
| git checkout [branch name] | Switch to a branch |
| git checkout -b [branch name] | Creates a new branch and switch to it |
| git checkout -b [branch name] origin/[branch name] | Clones a remote branch and switch to it |
| git checkout - | Switch to the branch last checked out |
| git merge [target branch] | Merges the active branch with a target branch |
| git merge [target branch] --no-ff | Constructs a merge instead of fast-forwarding |
| git merge [branch] [target branch] | Merges a branch with a target branch |
| git stash | Stashes the changes in a dirty working directory away |
| git stash clear | Remove all stashed entries |


### Sharing and Updating Projects
| Command | Description |
| ------- | ----------- |
| git remote add origin [url] | Adds a remote repository |
| git pull | Updates local repository to the newest commit |
| git pull origin [branch name]	| Pulls changes from remote repository |
| git push origin [branch name] | Pushes a branch to your remote repository |
| git push origin --delete [branch name] | 	Deletes a remote branch |

### Inspection and Comparison
| Command | Description |
| ------- | ----------- |
| git log | Shows commit logs |
| git log --abbrev-commit | Shows only a partial prefix of commit object name |
| git log --summary | Shows commit logs in detail |
| git diff | Shows changes between working area and staging area |
| gid diff --staged HEAD | Shows changes between staging area and local Git directory(last commit) |
| git diff [branch] [target branch] | Shows changes between a branch and a target branch |

