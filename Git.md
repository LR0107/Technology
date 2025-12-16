# Git Quick Start Guide

## 1. Download and Install Git

Download: https://git-scm.com/  
Verify installation:

`git --version`

## 2. Configure User Information

`git config --global user.name "Your Name" `

`git config --global user.email "your_email@example.com"`

View configuration:

`git config --list`

## 3. Create a Project Directory and Initialize a Git Repository

`git init`

Successful output example:

`Initialized empty Git repository in /Users/yourname/`

## 4. Create Files and Commit

Create a file:

`echo "# My First Project" > README.md`

Add to staging area:

`git add README.md`

Commit changes:

`git commit -m "Initial commit: add README file"`

## 5. Common Operations

View commit history:

`git log`

### Branch Management

`git branch                 # List local branches git branch feature/login   # Create a new branch git checkout feature/login # Switch to a branch git checkout -b dev        # Create and switch to dev branch`

## 6. Remote Repositories

Add a remote repository:

`git remote add reponame https://github.com/username/repo.git`

Notes:

- The repository URL is available after creating the repo on GitHub.

- `reponame` is a custom alias for the remote repository.

Push to remote (specific branch):

`git push -u reponame main`

Pull remote updates:

`git pull reponame main`

Clone a repository:

`git clone https://github.com/team/project.git`
