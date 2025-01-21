# Git Commands Guide

## Basic Commands
- `ls`: List down data of current working directory
- `ls -a`: List down hidden repo also
- `pwd`: Path of current working directory
- `cd`: Change directory to given path
- `clear`: Clear the terminal
- `cd ..`: Go back one step
- `cd /`: Go back to the root directory
- `cd ~`: Go back to home directory
- `touch filename.type`: Create a file
- `touch filename1.type filename2.type`: Create multiple files
- `mkdir`: Create a new folder/repo
- `mkdir foldername1 foldername2`: Create multiple folders at once
- `rm filename.type`: Delete file
- `rmdir foldername`: Delete directory
- `rm -rf foldername`: Delete directory having data

## Advanced Commands (Part 1)
- `vi filename.type`: Edit file in vim (Esc + :q to exit)
- `cat filename.type`: Display file content
- `git init`: Creates a git folder that contains a collection of files of various different versions of a project
- `git status`: Status of working directory and staging area
- `git add`: Adds a change in the working directory to the staging area
- `git add filename.type`: Add a single file to the staging area
- `git commit -m "commit message"`: Saving changes to git
- `git log`: Display changes have been staged and by whom
- `git restore --staged filename.type`: Unstage file
- `git reset`: Unstage all your files at once
- `git rm --cached filename.type/directory`: Remove the version/data history from git repo
- `git rm -f --cached filename.type/directory`: Remove the version/data history from git repo forcefully
- `git stash`: Takes your uncommitted changes (both staged and unstaged), takes and hold them in stack (backstage)
- `git stash pop`: Applies the top stashed element and removes it from stack (backstage)
- `git stash apply`: Applies the top stashed element and keeps it in the stack (backstage)
- `git stash clear`: Clear the stack (backstage)

## Advanced Commands (Part 2)
- `git remote add origin`: Repository url link
- `git remote -v`: To verify remote
- `git add`: Adds a change in the working directory to the staging area
- `git commit -m "commit message"`: Saving changes to git
- `git push origin master`: Push to github repository as master
- `git pull origin master`: Used to fetch and download content from a remote repository
- `git branch`: Create new branch
- `git branch -a`: See all branches created so far
- `git checkout 'branch name'`: Switch to the branch
- `git branch -b 'branch name'`: Create new branch + switch to the branch
- `git merge 'new branch name'`: Merge new branch with your current branch
- `git branch -d 'branch name'`: Delete branch
- `history`: To see all commands used till you will date

## Merging Code
### Way 1
- `git diff <branch name>`: To compare commits, branches, files & more
- `git merge <branch name>`: To merge 2 branches

### Way 2
- Create a PR (Pull Request)

## Init Commands
- `git init`: Used to create a new git repo
- `git remote add origin <link>`: Add remote repository link
- `git remote -v`: To verify remote
- `git branch`: To check branch
- `git branch -M main`: To rename branch
- `git push origin main`

## Push Commands
- `git push origin main`: Upload local repo content to remote repo

## Clone & Status
- Clone: Cloning a repository on our local machine
  - `git clone <some link>`
- Status: Displays the state of the code
  - `git status`

## Configuring Git
- `git config --global user.name "My Name"`
- `git config --global user.email "someone@email.com"`
- `git config --list`
