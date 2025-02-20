# ![github](/Assets/images/github.png)

## Table of Contents

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