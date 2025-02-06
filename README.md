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
Set your name for commits (same user name as for GitHub)
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
git branch <new-branch-name>
```
or create a new branch and switch to it in one step
```
git checkout -b <new-branch-name>
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
Delete a branch locally
```
git branch -d <branch-name>
```
If the branch has unmerged changes, to delete it - force delete it
```
git branch -D <branch-name>
```
Delete a branch remotely
```
git push origin --delete <branch-name>
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
or
```
git log --oneline --graph
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
Reapply stashed changes and remove them from the stash list
```
git stash pop
```
**Tagging**
> Used to mark specific points in your repository's history as
> being important, usually for releases or significant milestones.
Create a new tag
```
git tag <tag-name>
```
List all tags
```
git tag
```
Show details of a specific tag
```
git show <tag-name>
```
> Can be used for:
- Versioning Your Releases (e.g., v1.0.0, v2.1.3)
- Marking Important Points in History (launch, of a feature, deployment of a production-ready build, bugfix versions)

**Miscellaneous**
Remove untracked files
```
git clean -f
```
Apply a specific commit to the current branch
```
git cherry-pick <commit>
```
Show who modified each line of a file
```
git blame <file>
```
---
**Steps to Make a File Untraceable Using .gitignore**
1. Create or Edit a .gitignore File
 - If a .gitignore file doesn't exist in your repository, create one at the root of your project:
 ```
 touch .gitignore
 ```
2. Add the File or Pattern to .gitignore
 - For example, if your keys file is named keys.txt, add this line to .gitignore:
 ```
 keys.txt
 ```
 - To ignore all the files in a directory (e.g., config/), use:
 ```
 config/
 ```
 - For more complex patterns, you can use wildcards:
 ```
 *.key      # Ignore all files with .key extension
 secrets/*  # Ignore all files in the secrets folder
 ```
3. Remove the File from Git Tracking
 - If the file is already tracked by Git, you need to untrack it:
 ```
 git rm --cached keys.txt
 ```
 - This removes the file from Git's index but leaves it in your working directory.
4. Commit the Changes
 - After updating .gitignore, commit your changes:
 ```
 git add .gitignore
 git commit -m "Update .gitignore to ignore sensitive files"
 ```
**Example .gitignore for Keys or Sensitive Files**
```
# Ignore API keys and sensitive files
keys.txt
*.key
.env
secrets/

# Ignore system files
.DS_Store
Thumbs.db

# Ignore node modules and build files (for Node.js projects)
node_modules/
dist/
```
---
**Additional Tips**
- Avoid Committing .gitignore with Secrets: _Double-check that your sensitive files were never pushed to the repository before using .gitignore_
- Use Environment Variables: _For added security, store sensitive data in environment variables rather than in files_
---
These practices help maintain the security and integrity of your project while using Git effectively
---
**Git Commands for Team Collaboration**
1. Hadling Code Reviews
Fetch a pull request from GitHub for local testing
```
git fetch origin <branch-name>
```
2. Merging Changes
Merge another branch into the current branch
```
git merge <branch-name>
```
3. Cleaning Up
Delete a branch after merging 
```
git branch -d <branch-name>
```
Remove references to deleted remote branches
```
git remote prune origin
```
**Advice for Working in a Team**
1. Use Descriptive Commit Messages
Write clear and concise messages to describe whaat you changed and why.
2. Pull Before You Push
To avoid conflicts
3. Keep You Branches Small and Focused
