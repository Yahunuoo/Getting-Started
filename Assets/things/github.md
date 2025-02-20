# ![github](/Assets/images/github.png)

## Table of Contents
- [Additional Command Line Usage](#additional-command-line-usage)
- [GitHub Configuration](#github-configuration)
- [GitHub Authentication](#github-authentication)
- [GitHub Branch Management](#github-branch-management)
- [GitHub Repository Management](#github-repository-management)
- [GitHub Issue and Pull Request Management](#github-issue-and-pull-request-management)
- [GitHub Repository Cleanup](#github-repository-cleanup)
- [GitHub Tag Management](#github-tag-management)
- [GitHub Alias Configuration](#github-alias-configuration)
- [GitHub Fork Management](#github-fork-management)
- [GitHub Submodule Management](#github-submodule-management)
- [most Command Line Usage](#most-command-line-usage)
- [GitHub Docs](https://docs.github.com/en)

## most Command Line Usage

To use GitHub from the command line, you can use the following commands:

```sh
# Clone a repository
git clone https://github.com/username/repository.git

# Create a new branch
git checkout -b new-branch

# Add changes to staging
git add .

# Commit changes
git commit -m "Your commit message"

# Push changes to remote repository
git push origin new-branch
```

## Additional Command Line Usage

Here are some additional GitHub command line commands:

```sh
# Pull latest changes from remote repository
git pull origin main

# Merge a branch into the current branch
git merge branch-name

# Delete a branch locally
git branch -d branch-name

# Delete a branch remotely
git push origin --delete branch-name

# View the commit history
git log

# View the status of your working directory
git status

# Revert changes in a file to the last commit
git checkout -- file-name

# Stash changes in the working directory
git stash

# Apply stashed changes
git stash apply
```
## GitHub Configuration

Here are some commands to configure GitHub settings:

```sh
# Set your GitHub username
git config --global user.name "Your Name"

# Set your GitHub email
git config --global user.email "your-email@example.com"

# Set the default text editor for Git
git config --global core.editor "code --wait"

# Enable color in Git output
git config --global color.ui true

# Set the default merge tool
git config --global merge.tool vimdiff

# List all Git configurations
git config --list
```
## GitHub Authentication

Here are some commands to manage GitHub authentication:

```sh
# Cache your GitHub credentials in memory
git config --global credential.helper cache

# Store your GitHub credentials permanently
git config --global credential.helper store

# Use a personal access token for authentication
git remote set-url origin https://<TOKEN>@github.com/username/repository.git
```
## GitHub Branch Management

Here are some commands to manage branches in GitHub:

```sh
# List all branches
git branch -a

# Rename a branch
git branch -m old-branch-name new-branch-name

# Switch to a different branch
git checkout branch-name

# Create a new branch and switch to it
git checkout -b new-branch-name

# Push a new branch to remote repository
git push origin new-branch-name

# Set the upstream branch for the current branch
git push --set-upstream origin branch-name
```
## GitHub Repository Management

Here are some commands to manage your GitHub repositories:

```sh
# Initialize a new Git repository
git init

# Add a remote repository
git remote add origin https://github.com/username/repository.git

# Remove a remote repository
git remote remove origin

# Rename a remote repository
git remote rename origin new-origin

# Fetch changes from a remote repository
git fetch origin

# Clone a specific branch from a remote repository
git clone -b branch-name https://github.com/username/repository.git

# View remote repositories
git remote -v
```
## GitHub Issue and Pull Request Management

Here are some commands to manage issues and pull requests on GitHub:

```sh
# List all issues
gh issue list

# View a specific issue
gh issue view ISSUE_NUMBER

# Create a new issue
gh issue create

# List all pull requests
gh pr list

# View a specific pull request
gh pr view PR_NUMBER

# Create a new pull request
gh pr create

# Merge a pull request
gh pr merge PR_NUMBER

# Close a pull request
gh pr close PR_NUMBER
```
## GitHub Repository Cleanup

Here are some commands to clean up your GitHub repository:

```sh
# Remove untracked files from the working directory
git clean -f

# Remove untracked directories from the working directory
git clean -fd

# Remove ignored files from the working directory
git clean -X -f

# Remove both untracked and ignored files from the working directory
git clean -x -f
```
## GitHub Tag Management

Here are some commands to manage tags in GitHub:

```sh
# List all tags
git tag

# Create a new tag
git tag tag-name

# Create a new annotated tag
git tag -a tag-name -m "Tag message"

# Delete a tag locally
git tag -d tag-name

# Push a tag to remote repository
git push origin tag-name

# Delete a tag from remote repository
git push origin --delete tag-name

# View details of a tag
git show tag-name
```
## GitHub Alias Configuration

Here are some commands to create aliases for common Git commands:

```sh
# Create an alias for git status
git config --global alias.st status

# Create an alias for git checkout
git config --global alias.co checkout

# Create an alias for git commit
git config --global alias.ci commit

# Create an alias for git branch
git config --global alias.br branch

# Create an alias for git merge
git config --global alias.mg merge

# Create an alias for git log with a pretty format
git config --global alias.lg "log --oneline --graph --decorate --all"
```
## GitHub Fork Management

Here are some commands to manage forks in GitHub:

```sh
# Add a remote for the original repository
git remote add upstream https://github.com/original-owner/repository.git

# Fetch changes from the original repository
git fetch upstream

# Merge changes from the original repository into your fork
git merge upstream/main

# Push changes to your fork
git push origin main
```
## GitHub Submodule Management

Here are some commands to manage submodules in GitHub:

```sh
# Add a new submodule
git submodule add https://github.com/username/repository.git path/to/submodule

# Initialize submodules
git submodule init

# Update submodules
git submodule update

# Clone a repository with submodules
git clone --recurse-submodules https://github.com/username/repository.git

# Remove a submodule
git submodule deinit -f path/to/submodule
rm -rf .git/modules/path/to/submodule
git rm -f path/to/submodule
```