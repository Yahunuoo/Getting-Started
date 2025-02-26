# ![install - 2025](/Assets/images/ubuntu(75)-1.png)

## Configuring a development environment Ubuntu desktop

## Table of Contents

- [Install](#a-install)
    - [Updating Ubuntu](#1-the-bgining-updating-ubuntu)
    - [Install VS Code](#2-install-vscode)
    - [Install Git](#3-install-git)
    - [Updating Ubuntu Again](#4-again-updating-ubuntu)
    - [Install Curl](#5-install-curl)
    - [Install Zsh](#6-install-zsh)
    - [Install Oh My Zsh](#7-install-oh-my)

- [Configuring](#b-configuring)
    - [Create Directory Workspace](#1-create-directory-workspace)
    - [Git Config](#2-git-config)
    - [Generate Git Access Token](#3-generate-git-access-token)
    - [Create a .gitignore Global File](#4-create-a-gitignore-global-file-in-the-user-directory)

## A. install:

## 1. the bgining updating ubuntu

```bash
sudo apt update && sudo apt upgrade
```

## 2. install vscode

1. [Download and install the `.deb` package for VS Code](https://code.visualstudio.com/)
2. [Additional extensions](/Assets/things/vscode.md#vscode-extensions)

> 📌 ***open vscod and turn on `Auto Save` setting, is in the File menu***

## 3. install git

access to the most recent stable version of Git with this command

```sh
sudo add-apt-repository ppa:git-core/ppa
```

next

```sh
sudo apt-get update
```

next

```sh
sudo apt-get install git
```

## 4. again updating ubuntu

```bash
sudo apt update && sudo apt upgrade
```

## 5. install curl

Since you already have the terminal open, take the opportunity to install curl, which will let you install applications with just a URL, as you'll see us do soon. Use this command:

```bash
sudo apt install curl
```

## 6. install Zsh

Bash is Ubuntu's default shell (command interpreter), but Z shell is more commonly used in modern systems by default, so that's what we will use. Install it with this command, and accept the changes to be made by entering **`Y`** when prompted to continue:

```bash
sudo apt install zsh
```

Verify the installation with this command:

```bash
zsh --version
```

Make Zsh the default shell with this command:

```bash
chsh -s $(which zsh)
```

End your terminal session by closing the terminal window. Log out of your account, then log back in.

Open a new terminal window. As shown below, you should be prompted to run a configuration setup for new users:

![The terminal after installing `zsh`.](/Assets/images/terminal-u.png)

Enter `2` to accept the default configuration.

Your terminal prompt should look a little different now!

![zsh in action!](/Assets/images/terminal-2.png)

Let's confirm it worked with this command:

```bash
echo $SHELL
```

This should print **`/usr/bin/zsh`**

![zsh in action!](/Assets/images/terminal-3.png)

## 7. install Oh My

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

>[!NOTE]
> 📌 ***Note that your prompt has now changed to simply be `~` This is the desired outcome***

![oh my zsh!](/Assets/images/Oh-My-Zsh.png)

## B. Configuring:

## 1. create directory workspace

Create a directory that will represent the workspace, for example, with the name workstation or any name

```sh
mkdir workstation
```

## 2. Git config

```bash
git config --global user.name "User Name"
```

```bash
git config --global user.email "user@email.com"
```

```bash
git config --global init.defaultBranch main
```

```bash
git config --global core.editor "code --wait"
```

```bash
echo "export GIT_MERGE_AUTOEDIT=no" >> ~/.zshrc
```

```bash
git config --global pull.rebase false
```

## 3. Generate git access token

>[Click here github generate access codes](https://github.com/settings/tokens)

![generate access codes 1](/Assets/images/generate-access-codes-1.png)

>On the Personal access tokens (classic) page, click Generate new token and then Generate new token (classic)

![generate access codes 2](/Assets/images/generate-access-codes-2.png)

>You will be taken back to the Personal access tokens page, and the token you just created will be visible:

![generate access codes 2](/Assets/images/generate-access-codes-3.png)

Click the copy button to copy the newly created token.

You will only see the token on this page ONCE. You MUST copy it now and paste it in a secure and private place where you can easily access it later when you need it. Treat this token as you would a password! The token will be used in place of a password to interact with GitHub on the command line!

Using multiple machines? It is best practice to create a new token for each device requiring command-line access to GitHub. This way, if you need to revoke access to any single device, none of your other devices are impacted.

Place the token in a secure place! The next time you interact with GitHub on the command line, you will be asked to provide a username and password. Use this token in place of a password.

## 4. create a .gitignore global file in the user directory

create a .gitignore_global

```pash
touch ~/.gitignore_global
```

Next, configure Git to use this file

```pash
git config --global core.excludesfile ~/.gitignore_global
```

Open the new .gitignore_global file in VS Code:

```pash
code ~/.gitignore_global
```

>Use the one below

```plaintext
# This is a list of rules for ignoring files in every Git repository on your
# computer. See https://help.github.com/articles/ignoring-files

# GitHub maintains a repository of items that can generally be gitignored
# globally safely at: https://github.com/github/gitignore/tree/main/Global

# GitHub also maintains a repository of language-specific items that should
# typically be ignored on a per-project basis with a .gitignore in that
# project's root directory.
# This repository can be found at: https://github.com/github/gitignore

# This file DOES include items that would typically not be gitignored globally
# for simplicity during the course, but this may cause issues as you further
# your education post-SEI. These items are denoted when used here and are kept
# to a minimum.

###############################################################################
#   The items in this section are generally safe be globally gitignored and   #
#         are very unlikely to cause projects to break if left here.          #
###############################################################################

#================================= Archives ==================================#
#                Unpack these files and commit the raw source.                #
#                git has its own built in compression methods.                #

#----------------------------- Compressed Files ------------------------------#
*.7z
*.jar
*.rar
*.zip
*.gz
*.gzip
*.tgz
*.bzip
*.bzip2
*.bz2
*.xz
*.lzma
*.cab
*.xar

#--------------------------- Packing-only formats ----------------------------#
*.iso
*.tar

#------------------------ Package management formats -------------------------#
*.dmg
*.xpi
*.gem
*.egg
*.deb
*.rpm
*.msi
*.msix
*.msm
*.msp
*.txz

#===================== Operating System Generated Files ======================#
#----------------------------------- Linux -----------------------------------#
# Temporary files created as backups by text editors or similar programs #
*~

# Temporary files created if a process is still accessing a deleted file #
.fuse_hidden*
.nfs*

# KDE directory preferences #
.directory

# Linux trash folder which might appear on any partition or disk #
.Trash-*

#----------------------------------- macOS -----------------------------------#
# General #
.DS_Store
.DS_Store?
.AppleDouble
.LSOverride

# Thumbnails #
._*

# Files that might appear in the root of a volume #
.DocumentRevisions-V100
.fseventsd
.Spotlight-V100
.TemporaryItems
.Trashes
.VolumeIcon.icns
.com.apple.timemachine.donotpresent

# Directories potentially created on remote AFP share #
.AppleDB
.AppleDesktop
Network Trash Folder
Temporary Items
.apdisk

#---------------------------------- Windows ----------------------------------#
# Windows thumbnail cache files #
Thumbs.db
Thumbs.db:encryptable
ehthumbs.db
ehthumbs_vista.db

# Dump file #
*.stackdump

# Folder config file #
[Dd]esktop.ini

# Recycle Bin used on file shares #
$RECYCLE.BIN/

# Windows shortcuts #
*.lnk

#=================================== Tags ====================================#
#---- Ignore tags created by etags, ctags, gtags (GNU global) and cscope -----#
tags

#============================ Visual Studio Code =============================#
#----------------------------- .vscode Directory -----------------------------#
.vscode/

#------------------- Local History for Visual Studio Code --------------------#
.history/

###############################################################################
#   The items in this section may not typically be gitignored globally and    #
#               may cause future projects to break if left here.              #
# ** However, if you remove them from here, you MUST add them back to the **  #
#  ** projects they apply to by placing a .gitignore file containing the **   #
#       ** items to be gitignored in each project's root directory. **        #
###############################################################################

#=========================== Compiled Source Code ============================#
#-------------------------------- Class Files --------------------------------#
*.class

#----------------------------- Dynamic Libraries -----------------------------#
*.so
*.dylib
*.dll

#-------------------------------- Executables --------------------------------#
*.com
*.exe
*.out
*.app

#------------------------------- Object Files --------------------------------#
*.slo
*.lo
*.o
*.obj

#================================== Django ===================================#
#----------------------------------- Logs ------------------------------------#
*.log

#--------------------------- Local django settings ---------------------------#
local_settings.py

#------------------------------- SQL database --------------------------------#
db.sqlite3
db.sqlite3-journal

#============================== Node and Python ==============================#
.env

#=================================== Node ====================================#
node_modules

#================================== Python ===================================#
*.py[cd]
__pycache__/
.python-version

#================================== ESLint ===================================#
.eslintcache

#================================== Testing ==================================#
.rspec
capybara-*.html
coverage
pickle-email-*.html
rerun.txt
spec/reports
spec/tmp
test/tmp
test/version_tmp
```

>[!NOTE]
> 📌 ***all set Done :)***

<!--
## step 5

[Configuring a .gitignore global file](../Assets/gitignore_global.md)

## step 6

[Setting up and preparing the programming language environment](../Programming-Language-Environment/README.md)

>[!NOTE]
> 📌 ***setup to start developing in ubuntu has done***
-->