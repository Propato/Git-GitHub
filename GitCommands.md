# Useful Commands

Here are some useful git commands that I use, and these notes help me to always have access to them and I hope they can help anyone in need.

## Table of contents

* [Dictionary](#Dictionary)
* [Init and Configure](#Init-and-Configure)
* [Git Add](#Git-Add)
* [Git Commit](#Git-Commit)
* [Git Push](#Git-Push)
* [Git Pull](#Git-Pull)
* [Git Diff](#Git-Diff)
* [Git Log](#Git-Log)
* [Git Checkout](#Git-Checkout)
* [Git Revert](#Git-Revert)
* [Git Reset](#Git-Reset)
* [Git Clean](#Git-Clean)
* [Git Branches](#Git-Branches)
* [Git Fetch](#Git-Fetch)
* [Git Merge](#Git-Merge)
* [Git Rebase](#Git-Rebase)

## Dictionary

Keywords | Description
:---: | ---
HEAD | pointer for the last commit
HEAD^ | HEAD's previous commit, the more "^" further we go back in the sequence of commits

## Init and Configure

Command | Description
:---: | ---
`git init` | Start the Git folder
`git remote add <name> <url>` | Create a connection between local repository and online repository and name it
`git remote rename <old> <new>` | Rename connection between local repository and online repository
`git remote remove <name>` | Remove connection between local repository and online repository

## Git Add

Command | Description
:---: | ---
`git add -A` | Stage all files (new, modified and deleted)
`git add *` | Stage all files (except beginning with a dot)
`git add .` | Stage new and modified files only
`git add -u` | Stage modified and deleted files only
`git reset` | Reset staged files/Undo add

All respect .gitignore, but * throws an error.

## Git Commit

Command | Description
:---: | ---
`git commit` | Open the commit area and save staged files
`git commit -m "comentários das alterações"` | save comments and all staged files
`git commit -a` | Stage modified and deleted files and save all staged files
`git commit --amend` | Save all staged files in the last commit

## Git Push

Command | Description
:---: | ---
`git push origin <remote branch>` | Update the remote branch with the saved current local branch
`git push -f origin <remote branch>` | -f Allow to update the remote branch that is not an ancestor of the local branch
`git push -u origin <remote branch>` | Update the remote branch with the saved current local branch and sets the local branch to "track" the remote branch
`git push` | Using the "track" from the local branch to remote branch, update all remote branches with saved local branches

## Git Pull

Command | Description
:---: | ---
`git pull origin <remote branch>` | Update the current local branch with the remote branch
`git pull --allow-unrelated-histories origin <remote branch>` | Update the current local branch with the remote branch, this option allow to merge branches that do not share a common ancestor
`git pull --commit origin <remote branch>` | Perform the merge and commit the result
`git pull` | Update all local branches with corresponding remote branch

## Git Diff

Command | Description
:---: | ---
`git diff [<options>] <commit> <commit>` | Show changes between the commits

## Git Log

Command | Description
:---: | ---
`git log` | shows commit history, press q to quit
`git log --oneline` | shows simplefy commit history, press q to quit

## Git Checkout

Command | Description
:---: | ---
`git checkout <commit id>` | Access the commit by modifying the working tree and the history
`git checkout <branch>` | Access last commit of the branch

## Git Revert

Command | Description
:---: | ---
`git revert <commit id>` | Reverts the working tree to the commit and make a new commit with this working tree, dont deleted history

## Git Reset

Command | Description
:---: | ---
`git reset` | Reset staged files/Undo add (resets the indexes but not the file changes)
`git reset -- <file name>` | Reset the staged file/Undo add in the file
`git reset <commit id>` | Undo commits and add up to the given commit (resets the indexes but not the working tree)
`git reset --soft <commit id>` | Undo commits up to the given commit (dont resets the indexes and the working tree)
`git reset --hard <commit id>` | Undo commits and add up to the given commit (resets the indexes and the working tree)

> reset working tree == remove changes in the tracked files
> reset index == reset adds

## Git Clean

Command | Description
:---: | ---
`git clean` | Remove untracked files from the working tree
`git clean -n` | Show what will be removed
`git clean -i` | Show what will be removed and clean files interactively from the working tree
`git clean -f` | Remove untracked files from the working tree by force
`git clean -d` | Recursively remove untracked directories from the working tree

## Git Branches

Command | Description
:---: | ---
`git branch` | List local branches and which one is active
`git branch -a` | List local and remote branches and which one is active
`git switch <branch>` | Switch to the specified branch
`git checkout -b <branch name>` | Create a new branch
`git branch -d <branch>` | Delete branch
`git branch -M main` | Move/rename the active branch

## Git Fetch

Command | Description
:---: | ---
`git fetch` | updates the local repository with the latest information from the remote repository, but without modifying the local files

## Git Merge

Command | Description
:---: | ---
`git merge` | Join two or more development histories together

## Git Rebase

Command | Description
:---: | ---
`git Rebase` | Reapply commits on top of another base tip