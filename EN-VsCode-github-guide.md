# GitHub Guide for VS Code Users

## Introduction

This guide is designed to help programming students effectively use GitHub with Visual Studio Code (VS Code). VS Code provides excellent GitHub integration through its built-in source control features and extensions, making it easy to manage your code repositories without having to use the command line extensively.

## Table of Contents

1. [Setting Up GitHub in VS Code](#1-setting-up-github-in-vs-code)
2. [Creating a Repository](#2-creating-a-repository)
3. [Cloning a Repository](#3-cloning-a-repository)
4. [Pulling Repository Changes](#4-pulling-repository-changes)
5. [Committing Changes](#5-committing-changes)
6. [Staging Changes](#6-staging-changes)
7. [Pushing Changes](#7-pushing-changes)
8. [Creating Pull Requests](#8-creating-pull-requests)
9. [Creating and Managing Branches](#9-creating-and-managing-branches)
10. [Merging Branches](#10-merging-branches)
11. [Stashing Changes](#11-stashing-changes)
12. [Resolving Conflicts](#12-resolving-conflicts)

## 1. Setting Up GitHub in VS Code

### Installing Git

Before you start, ensure Git is installed on your system:
1. Download and install Git from [git-scm.com](https://git-scm.com/)
2. Verify installation by opening a terminal and typing `git --version`

### Installing VS Code Extensions

For the best GitHub experience in VS Code, install these extensions:
1. Open VS Code
2. Go to Extensions view (click the Extensions icon in the Activity Bar or press `Ctrl+Shift+X`)
3. Search for and install:
   - **GitHub Pull Requests and Issues** - For managing PRs and issues
   - **GitLens** - For additional Git features and visualizations

### Configuring GitHub Authentication

1. Open VS Code
2. Click on the Source Control icon in the Activity Bar (or press `Ctrl+Shift+G`)
3. If you haven't connected to GitHub yet, you'll see options to clone a repository or open a folder
4. When you perform your first Git operation, VS Code will prompt you to authenticate with GitHub
5. Follow the authentication flow, which will typically open a browser for you to sign in to GitHub

### Configuring Git Identity

Set your Git user information in VS Code:
1. Open the terminal in VS Code (`Ctrl+`` or View > Terminal)
2. Configure your Git username and email:
```
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## 2. Creating a Repository

### Creating a New Repository on GitHub

1. Go to [GitHub.com](https://github.com) and sign in
2. Click on the "+" icon in the top-right corner and select "New repository"
3. Fill in:
   - Repository name
   - Description (optional)
   - Choose public or private
   - Select "Add a README file" if desired
   - Choose a .gitignore template appropriate for your project
   - Select a license if needed
4. Click "Create repository"

### Initializing a Local Repository in VS Code

1. Open the folder you want to initialize as a Git repository in VS Code
2. Click on the Source Control icon in the Activity Bar
3. Click on "Initialize Repository"
4. To connect this local repository to GitHub:
   - Click on "Publish to GitHub" in the Source Control view
   - Select whether to publish publicly or privately
   - Choose a repository name
   - Click "OK" to publish

## 3. Cloning a Repository

### Cloning from GitHub in VS Code

1. Click on the Source Control icon in the Activity Bar
2. Click on "Clone Repository"
3. Choose from the following options:
   - "Clone from GitHub" (if you've authenticated with GitHub)
   - "Clone from URL" (if you have a specific repository URL)
4. If selecting "Clone from GitHub":
   - Search for a repository from your GitHub account
   - Select the repository you want to clone
5. If selecting "Clone from URL":
   - Paste the GitHub repository URL
6. Choose a local folder to clone into
7. Click "Select Repository Location"
8. VS Code will clone the repository and prompt you to open it

## 4. Pulling Repository Changes

### Pulling Changes in VS Code

1. Open your repository in VS Code
2. Click on the Source Control icon in the Activity Bar
3. In the Source Control view, look for the "..." (More Actions) menu
4. Click "Pull" to fetch and merge changes from the remote repository

Alternatively, you can:
1. Look at the status bar at the bottom of VS Code
2. Find the sync indicator showing incoming and outgoing commits (↓↑)
3. Click on it and select "Pull"

You can also use the keyboard shortcut: Press `Ctrl+Shift+P`, type "Git: Pull" and press Enter.

## 5. Committing Changes

### Creating Commits in VS Code

1. Make changes to your files in the editor
2. Click on the Source Control icon to see all modified files
3. Hover over the "Changes" section to see the "+" icon to stage all changes, or:
   - Hover over individual files and click the "+" icon to stage specific files
4. Once changes are staged, enter a commit message in the text field at the top of the Source Control panel
5. Click the checkmark (✓) icon to commit the staged changes
   - Alternatively, press `Ctrl+Enter` while in the commit message field

For more detailed commit messages:
1. Click "..." in the Source Control view
2. Select "Commit Staged" to open a more detailed commit message editor

## 6. Staging Changes

### Staging Files and Changes in VS Code

1. In the Source Control view, you'll see all modified files under "Changes"
2. To stage individual files:
   - Hover over the file and click the "+" icon
   - Or right-click the file and select "Stage Changes"
3. To stage specific parts of a file (partial staging):
   - Open the file in the editor
   - In the editor's gutter, click the "+" icon next to the lines you want to stage
   - Or right-click the selected lines and choose "Stage Selected Ranges"
4. To stage all changes at once:
   - Click the "+" icon next to the "Changes" header

### Unstaging Changes

1. In the Source Control view, look for staged files under "Staged Changes"
2. To unstage a file:
   - Hover over the file and click the "-" icon
   - Or right-click the file and select "Unstage Changes"

## 7. Pushing Changes

### Pushing Commits to GitHub

1. After committing changes, click the "..." in the Source Control view
2. Select "Push"
3. If this is your first push to a new repository, you might be prompted to select a remote repository

Alternatively:
1. Look for the sync indicator in the status bar (showing ↑ with a number)
2. Click on it and select "Push"

You can also use the keyboard shortcut: Press `Ctrl+Shift+P`, type "Git: Push" and press Enter.

### Publishing a Branch

If you've created a new branch locally:
1. When you're ready to push it to GitHub, look for the cloud icon with an arrow in the status bar
2. Click it and select "Publish Branch"
3. Or use the "..." menu in the Source Control view and select "Push" or "Publish Branch"

## 8. Creating Pull Requests

### Creating Pull Requests from VS Code

With the GitHub Pull Requests and Issues extension installed:

1. Make your changes and push them to a branch on GitHub
2. Click on the GitHub icon in the Activity Bar
3. In the GitHub view, click on the "+" icon next to "Pull Requests"
4. Select the source branch (your changes) and the target branch (usually main or master)
5. Add a title and description for your Pull Request
6. Click "Create" to submit the Pull Request

Alternatively:
1. After pushing a branch, VS Code often shows a notification with a "Create Pull Request" button
2. Click this button to open the Pull Request creation interface

### Managing Pull Requests

1. Click on the GitHub icon in the Activity Bar
2. Expand the "Pull Requests" section to see all open PRs
3. Click on a PR to:
   - Review the changes
   - Add comments
   - Approve or request changes
   - Merge the PR (if you have permission)

## 9. Creating and Managing Branches

### Creating Branches in VS Code

1. Look at the status bar at the bottom of VS Code to see your current branch
2. Click on the branch name in the status bar
3. From the dropdown, select "Create new branch..."
4. Enter a name for your new branch
5. Press Enter to create and switch to the new branch

Alternatively, use the Command Palette:
1. Press `Ctrl+Shift+P`
2. Type "Git: Create Branch" and press Enter
3. Enter a branch name and press Enter

### Switching Between Branches

1. Click on the current branch name in the status bar
2. Select a branch from the dropdown list to switch to it

Or:
1. Press `Ctrl+Shift+P`
2. Type "Git: Checkout to" and press Enter
3. Select the branch you want to switch to

### Viewing Branch History

With GitLens extension installed:
1. Click on the GitLens icon in the Activity Bar
2. Navigate to the "Repositories" view
3. Expand your repository and the "Branches" section
4. Click on a branch to see its commit history

## 10. Merging Branches

### Merging Branches in VS Code

1. First, switch to the target branch (the branch you want to merge into):
   - Click the branch name in the status bar
   - Select the target branch (e.g., main)
2. Open the Command Palette with `Ctrl+Shift+P`
3. Type "Git: Merge Branch..." and press Enter
4. Select the source branch (the branch you want to merge from)

VS Code will perform the merge operation:
- If there are no conflicts, the merge will complete automatically
- If there are conflicts, VS Code will guide you through the conflict resolution process

## 11. Stashing Changes

### Stashing Changes in VS Code

When you need to switch branches but aren't ready to commit your changes:

1. Click the "..." menu in the Source Control view
2. Select "Stash" or "Stash (Include Untracked)"
3. Enter an optional message to identify your stash
4. Press Enter to create the stash

### Applying Stashed Changes

1. Click the "..." menu in the Source Control view
2. Select "Stash" > "Apply Stash..."
3. Select the stash you want to apply
4. Choose one of the options:
   - "Apply Stash" (keeps the stash for future use)
   - "Apply Stash and Delete" (removes the stash after applying)
   - "Delete Stash" (removes the stash without applying)

## 12. Resolving Conflicts

### Handling Merge Conflicts in VS Code

When a conflict occurs during merging or pulling:

1. VS Code will show the conflicted files in the Source Control view
2. Click on a conflicted file to open it in the editor
3. VS Code displays an inline conflict editor with three sections:
   - "Current Change" (your local changes)
   - "Incoming Change" (changes from the branch you're merging)
   - The editor combining both changes with conflict markers
4. For each conflict, VS Code offers action buttons:
   - "Accept Current Change"
   - "Accept Incoming Change"
   - "Accept Both Changes"
   - "Compare Changes"
5. Select the appropriate action for each conflict
6. After resolving all conflicts in a file, save the file
7. Stage the resolved file by clicking the "+" icon next to it
8. Once all conflicts are resolved and staged, complete the merge by committing

For a more visual approach to conflict resolution:
1. When encountering conflicts, right-click on a conflicted file
2. Select "Resolve in Merge Editor"
3. Use the three-way merge editor to visually resolve conflicts

## VS Code GitHub Features and Tips

### Source Control View Navigation

The Source Control view provides a comprehensive interface for Git operations:
- **Changes**: Files you've modified but not staged
- **Staged Changes**: Files ready to be committed
- **Merge Changes**: Files with conflicts during a merge
- **Commits**: Shows recent commits when expanded

### Useful VS Code Keyboard Shortcuts for Git

- `Ctrl+Shift+G`: Open Source Control view
- `Ctrl+Enter`: Commit staged changes (when focus is in the commit message field)
- `Alt+C`: Stage selected changes in a file
- `Alt+R`: Restore (discard) selected changes in a file
- `Ctrl+Shift+P`: Command Palette for Git commands

### VS Code Settings for Git

Customize your Git experience in VS Code:
1. Go to File > Preferences > Settings (or press `Ctrl+,`)
2. Search for "git" to find Git-related settings
3. Useful settings to consider:
   - `git.enableSmartCommit`: Automatically stage all changes when committing
   - `git.confirmSync`: Confirm before synchronizing Git repositories
   - `git.autofetch`: Periodically fetch from remotes
   - `git.decorations.enabled`: Show Git status in the Explorer

### GitHub Workflow Recommendations

For effective use of GitHub with VS Code:
1. **Branch for Features**: Create a new branch for each feature or bug fix
2. **Commit Often**: Make small, focused commits with clear messages
3. **Pull Before Pushing**: Always pull changes before pushing to avoid conflicts
4. **Use Pull Requests**: Create PRs for code review before merging into main branches
5. **Leverage Extensions**: Use GitHub and GitLens extensions for enhanced workflow

## Additional Resources

- [VS Code Git Documentation](https://code.visualstudio.com/docs/sourcecontrol/overview)
- [GitHub Documentation](https://docs.github.com/en)
- [GitHub Pull Requests and Issues Extension](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
- [GitLens Extension](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

---

This guide covers the essential GitHub operations using VS Code's graphical interface. As you become more familiar with these tools, you'll find that VS Code's Git integration makes version control and collaboration through GitHub more intuitive and efficient.
