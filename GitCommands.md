# Useful Commands

Here are some useful git commands that I use, and these notes help me to always have access to them and I hope they can help anyone in need.

## Init and Configure

Command | Description
:---: | ---
`git init` | Start the Git folder
`git remote add <name> <url>` | Create a connection between local repository and online repository and name it
`git remote rename <old> <new>` | Rename connection between local repository and online repository
` git remote remove <name>` | Remove connection between local repository and online repository

## Git Add
Command | Description
:---: | ---
`git add -A` | Stage all files (new, modified and deleted)
`git add *` | Stage all files (except beginning with a dot)
`git add .` | Stage new and modified files only
`git add -u` | Stage modified and deleted files only

All respect .gitignore, but * throws an error.

## Git Commit
Command | Description
:---: | ---
`git commit` | Open the commit area and save staged files
`git commit -m "comentários das alterações"` | save comments and all staged files
`git commit -am "comentários das alterações"` | Stage modified and deleted files and save comments and all staged files

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

## Git Branches
Command | Description
:---: | ---
`git branch` | List local branches and which one is active
`git branch -a` | List local and remote branches and which one is active
`git switch <branch>` | Switch to the specified branch
`git checkout -b <branch name>` | Create a new branch
`git branch -d <branch>` | Delete branch
`git branch -M main` | Move/rename the active branch