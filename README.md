# Cheatsheet Git commands
Git is a version control tool that is essential for working with DS/CS in the real world. It helps you to track your work, exeriment with changes and collaborate with others easily. So, here's the ***list of terminal commands*** that are often used in the projects.

**Installing Git**
Navigate to the latest [Git installer](https://git-scm.com/downloads) and download *the latest* version.

***Check if installation is successful***
```
git --version
```
To create a folder
```
mkdir 'folder name'
```

**Setup and Configuration**
Set your name for commits
```
git config --global user.name "Your Name"
```
Set your email for commits (same email as you used for GitHub)
```
git config --global user.email "youremail@example.com"
```
Show all Git configurations
```
git config --list
```
**Starting a Repository**
Initialize a new Git repository
```
git init
```
Clone an existing repository
```
git clone <repository-url>
```
**Basic Workflow**
Check the status of your repository
```
git status
```
Stage all changes in the currect directory
```
git add .
```
Or stage a specific file
```
git add <file>
```
Commit changes with a message
```
git commit -m "Commit messsage"
```
Push changes to the remote repository
```
git push origin <branch name>
```
Fetch and merge changes from the remote repository
```
git pull origin <branch name>
```
**Branching and Merging** (working in a team)
List all branches
```
git branch
```
Create a new branch
```
git branch <bramch-name>
```
Switch to a specific branch
```
git checkout <branch-name>
```
Create and switch to a new branch
```
git checkout -b <branch-name>
```
Merge a branch into the current branch
```
git merge <branch-name>
```
**Viewing Changes**
Show the commit history
```
git log
```
Show a concise commit history
```
git log --oneline
```
View unstaged changes
```
git diff
```
View changes staged for the next commit 
```
git diff --staged
```
**Undoing Changes**
Unstage a file without discarding changes
```
git reset <file>
```
Reset to a specific commit and discard all changes
```
git reset --hard <commit>
```
Discard changes to a file
```
git checkout -- <file>
```
Create a new commit that undoes a specific commit 
```
git revert <commit>
```
**Remote Repositories**
Show remote repository URLs
```
git remote -v
```
Add a new remote repository
```
git remote add <name> <url>
```
Fetch changes from a remote repository
```
git fetch
```
**Stashing Changes**
Save changes temporarily and clean the working directory
```
git stash
```
Reapply the stashed changes
```
git stash apply
```
Remove a specific stash entry
```
git stash drop
```
