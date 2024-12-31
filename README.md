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
