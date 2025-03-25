# GitHub Guide for Programming Students

## Introduction

GitHub is an essential platform for modern software development that allows developers to collaborate on code, track changes, and manage projects effectively. This guide will help you get started with GitHub and master the fundamental operations you need for submitting your assignments and collaborating with others.

## Table of Contents

1. [Registering and Creating a Repository](#1-registering-and-creating-a-repository)
2. [Cloning a Repository](#2-cloning-a-repository)
3. [Pulling Repository Changes](#3-pulling-repository-changes)
4. [Committing Changes Locally](#4-committing-changes-locally)
5. [Staging Changes](#5-staging-changes)
6. [Pushing Changes to Server](#6-pushing-changes-to-server)
7. [Creating Pull Requests](#7-creating-pull-requests)
8. [Creating Branches](#8-creating-branches)
9. [Merging Branches](#9-merging-branches)
10. [Stashing Changes](#10-stashing-changes)
11. [Resolving Conflicts](#11-resolving-conflicts)

## 1. Registering and Creating a Repository

### Registration

1. Go to [GitHub.com](https://github.com)
2. Click on "Sign up" and follow the instructions to create your account
3. Verify your email address when prompted

### Creating a Repository via Web Interface

1. After logging in, click the "+" icon in the top-right corner
2. Select "New repository"
3. Fill in the repository details:
   - Repository name (use a descriptive name, e.g., "cs101-assignment1")
   - Description (optional but recommended)
   - Choose "Public" or "Private" (for assignments, private is often preferred)
   - Select "Initialize this repository with a README"
   - Add a .gitignore file appropriate for your programming language
   - Choose a license if applicable
4. Click "Create repository"

## 2. Cloning a Repository

Cloning creates a local copy of a repository on your computer.

```bash
# Clone a repository using HTTPS
git clone https://github.com/username/repository-name.git

# Clone a repository using SSH (requires SSH key setup)
git clone git@github.com:username/repository-name.git

# Clone to a specific folder
git clone https://github.com/username/repository-name.git my-folder-name
```

After cloning, a new directory with your repository name will be created. Navigate to it:

```bash
cd repository-name
```

## 3. Pulling Repository Changes

Pulling updates your local repository with changes from the remote repository.

```bash
# Make sure you're in the repository directory first
# Pull changes from the remote repository
git pull

# Pull from a specific remote and branch
git pull origin main
```

It's a good practice to pull changes before starting work each day to ensure you have the latest code.

## 4. Committing Changes Locally

Committing records changes to the repository. Each commit should represent a logical unit of work.

```bash
# Check which files have been modified
git status

# Commit all tracked and modified files with a message
git commit -am "Description of changes made"

# Alternative two-step approach:
# 1. Stage files (covered in the next section)
# 2. Commit staged files
git commit -m "Description of changes made"
```

Write clear, concise commit messages that describe what changes were made and why.

## 5. Staging Changes

Staging allows you to select which changes will be included in the next commit.

```bash
# Stage a specific file
git add filename.py

# Stage multiple files
git add file1.py file2.py

# Stage all changes in the current directory
git add .

# Stage all changes in the repository
git add -A

# Remove a file from staging
git reset filename.py
```

Staging gives you fine-grained control over what goes into each commit, allowing you to create clean, logical commit history.

## 6. Pushing Changes to Server

Pushing uploads your local commits to the remote repository.

```bash
# Push changes to the default remote repository (origin) and branch
git push

# Push to a specific remote and branch
git push origin main

# Force push (use with caution - can overwrite remote changes)
git push -f origin main
```

Remember to pull changes before pushing to avoid conflicts.

## 7. Creating Pull Requests

Pull Requests (PRs) are a way to propose changes to a repository. They're central to collaborative development.

Creating a PR via command line involves:

1. Push your branch to GitHub:
```bash
git push origin your-branch-name
```

2. GitHub will display a URL in the output. Visit that URL or go to the repository page on GitHub.

3. Click on "Compare & pull request" button.

4. Fill in:
   - Title: Clear summary of what the PR does
   - Description: Detailed explanation of changes
   - Reviewers: Select team members to review (if applicable)

5. Click "Create pull request"

## 8. Creating Branches

Branches allow you to develop features, fix bugs, or experiment without affecting the main codebase.

```bash
# List all branches (* indicates current branch)
git branch

# Create a new branch
git branch branch-name

# Create and switch to a new branch
git checkout -b branch-name

# Switch to an existing branch
git checkout branch-name

# Using the newer git switch command (Git 2.23+)
git switch branch-name

# Create and switch to a new branch (Git 2.23+)
git switch -c branch-name
```

Naming convention for branches:
- feature/feature-name
- bugfix/issue-description
- hotfix/urgent-fix
- release/version-number

## 9. Merging Branches

Merging combines changes from different branches.

```bash
# First, switch to the target branch (e.g., main)
git checkout main

# Merge a branch into the current branch
git merge branch-name

# Merge with no fast-forward to preserve branch history
git merge --no-ff branch-name
```

After merging, you may want to delete the branch if it's no longer needed:

```bash
# Delete a branch locally
git branch -d branch-name

# Force delete an unmerged branch
git branch -D branch-name

# Delete a branch on the remote
git push origin --delete branch-name
```

## 10. Stashing Changes

Stashing temporarily saves changes that you don't want to commit immediately.

```bash
# Stash current changes
git stash

# Stash with a descriptive message
git stash save "Working on feature X"

# List all stashes
git stash list

# Apply the most recent stash and keep it in the stash list
git stash apply

# Apply a specific stash
git stash apply stash@{2}

# Apply the most recent stash and remove it from the stash list
git stash pop

# Remove a specific stash
git stash drop stash@{1}

# Clear all stashes
git stash clear
```

Stashing is useful when you need to switch branches but aren't ready to commit your changes.

## 11. Resolving Conflicts

Conflicts occur when Git can't automatically merge changes. You'll need to resolve them manually.

When a conflict occurs, Git will mark the conflicted files. Opening them will show something like:

```
<<<<<<< HEAD
current change
=======
incoming change
>>>>>>> branch-name
```

Steps to resolve conflicts:

1. Run `git status` to see which files have conflicts
2. Open the conflicted files and look for the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
3. Edit the files to resolve the conflicts (choose one version or merge them manually)
4. Remove the conflict markers
5. Stage the resolved files:
```bash
git add filename
```
6. Complete the merge:
```bash
git commit -m "Merge branch 'branch-name' with conflict resolution"
```

## Best Practices

1. **Pull before you push**: Always pull the latest changes before pushing to avoid conflicts
2. **Commit often**: Make small, focused commits with clear messages
3. **Use branches**: Don't work directly on the main branch
4. **Write meaningful commit messages**: Explain what and why, not how
5. **Review your changes**: Use `git diff` and `git status` before committing
6. **Keep your repository clean**: Use `.gitignore` to exclude unnecessary files

## Common Git Commands Summary

```bash
# Setup & Configuration
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Repository Operations
git init                    # Initialize a new repository
git clone [url]             # Clone a repository
git remote -v               # List remotes
git remote add [name] [url] # Add a remote

# Basic Workflow
git status                  # Check status
git add [file]              # Stage changes
git commit -m "[message]"   # Commit changes
git pull                    # Pull changes
git push                    # Push changes

# Branching & Merging
git branch                  # List branches
git branch [name]           # Create branch
git checkout [branch]       # Switch branch
git merge [branch]          # Merge branch
git branch -d [branch]      # Delete branch

# History & Comparison
git log                     # View commit history
git log --oneline           # Compact view
git diff                    # View changes
git blame [file]            # See who changed what
```

## Troubleshooting Common Issues

### Authentication Failed
- Check your credentials
- For HTTPS: Update your credentials in the credential manager
- For SSH: Verify your SSH key is added to your GitHub account

### Cannot Push
- Pull first to incorporate remote changes
- Check if you have proper permissions

### Merge Conflicts
- Follow the conflict resolution steps above
- Use a visual merge tool if available

### Accidentally Committed to Wrong Branch
- Use `git reset` to undo the commit
- Switch to the correct branch
- Re-commit the changes

---

Remember that Git is a powerful tool with a steep learning curve. Don't worry if you make mistakes—they're part of the learning process. Use this guide as a reference, and don't hesitate to ask for help when needed.

For more advanced Git features, refer to the [official Git documentation](https://git-scm.com/doc).
