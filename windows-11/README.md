# Windows 11 + WSL Development Setup

![Windows 11](../assets/images/windows-11.jpg)

This is the main workstation setup guide. The goal is to use **Windows 11** as the desktop operating system and **Ubuntu in WSL 2** as the development environment.

## Contents

- [1. Update Windows](#1-update-windows)
- [2. Open Windows Terminal as Administrator](#2-open-windows-terminal-as-administrator)
- [3. Install WSL 2 and Ubuntu](#3-install-wsl-2-and-ubuntu)
- [4. Create the Ubuntu user](#4-create-the-ubuntu-user)
- [5. Check WSL](#5-check-wsl)
- [6. Configure Windows Terminal](#6-configure-windows-terminal)
- [7. Update Ubuntu inside WSL](#7-update-ubuntu-inside-wsl)
- [8. Install Zsh](#8-install-zsh)
- [9. Install Oh My Zsh](#9-install-oh-my-zsh)
- [10. Install Visual Studio Code](#10-install-visual-studio-code)
- [11. Install Git for Windows](#11-install-git-for-windows)
- [12. Configure Git inside WSL](#12-configure-git-inside-wsl)
- [13. Use Windows Git Credential Manager from WSL](#13-use-windows-git-credential-manager-from-wsl)
- [14. Create the development workspace](#14-create-the-development-workspace)
- [15. Optional: PowerToys](#15-optional-powertoys)
- [16. Final checks](#16-final-checks)

## 1. Update Windows

Before installing development tools:

1. Open **Settings → Windows Update**.
2. Install available Windows updates.
3. Open **Microsoft Store → Library** and update installed Store apps.
4. Restart Windows if required.

## 2. Open Windows Terminal as Administrator

Search for **Terminal**, right-click **Windows Terminal**, and choose **Run as administrator**.

Commands in this section that require elevated privileges should be run from this administrator terminal.

## 3. Install WSL 2 and Ubuntu

Run:

```powershell
wsl --install -d Ubuntu
```

Restart Windows when requested.

If WSL is already installed and the command only shows help, list available distributions:

```powershell
wsl --list --online
```

Then install Ubuntu explicitly:

```powershell
wsl --install -d Ubuntu
```

To update WSL itself later:

```powershell
wsl --update
```

## 4. Create the Ubuntu user

The first Ubuntu launch will ask for:

- a Linux username
- a Linux password

The password is not displayed while typing. This is normal in Linux terminals.

Use a simple username without spaces and keep the password in a secure password manager.

## 5. Check WSL

From PowerShell:

```powershell
wsl --status
```

```powershell
wsl --version
```

```powershell
wsl --list --verbose
```

Ubuntu should be using WSL version `2`.

## 6. Configure Windows Terminal

Open **Windows Terminal → Settings → Startup** and set the default profile to **Ubuntu** if you want the terminal to open directly in WSL.

The Windows desktop applications and the WSL Linux environment are separate environments. Install desktop applications on Windows, and install command-line development tools inside WSL when appropriate.

## 7. Update Ubuntu inside WSL

Inside the Ubuntu/WSL terminal:

```bash
sudo apt update && sudo apt upgrade -y
```

Install the basic utilities used by this guide:

```bash
sudo apt install -y curl git zsh
```

Check Git:

```bash
git --version
```

## 8. Install Zsh

Check the installed version:

```bash
zsh --version
```

Set Zsh as the default shell:

```bash
chsh -s "$(which zsh)"
```

Close the WSL terminal and open it again.

On the first Zsh run, select the option to create the default configuration if prompted.

![Zsh first run](../assets/images/zsh-first-run.png)

Confirm the shell:

```bash
echo $SHELL
```

Expected result:

```text
/usr/bin/zsh
```

![Zsh terminal](../assets/images/zsh-terminal.png)

## 9. Install Oh My Zsh

Run:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

![Oh My Zsh](../assets/images/oh-my-zsh.png)

After installation, restart the terminal if necessary.

## 10. Install Visual Studio Code

Install **Visual Studio Code on Windows**, not as a Linux desktop application inside WSL.

Official download:

https://code.visualstudio.com/

Then install the Microsoft **WSL** extension in VS Code.

See the separate [VS Code reference](../tools/vscode.md) for recommended settings and extensions.

### Open a WSL project in VS Code

From inside a project directory in WSL:

```bash
code .
```

The lower-left area of VS Code should indicate that the window is connected to WSL.

## 11. Install Git for Windows

Install the current **Git for Windows** release:

https://git-scm.com/download/win

Keep **Git Credential Manager** enabled during installation. It is included with Git for Windows and provides secure authentication for Git hosting services such as GitHub.

Git for Windows is installed mainly so its credential manager can be shared with Git running inside WSL.

## 12. Configure Git inside WSL

Run these commands inside Ubuntu/WSL and replace the example name and email:

```bash
git config --global user.name "User Name"
```

```bash
git config --global user.email "user@example.com"
```

```bash
git config --global init.defaultBranch main
```

```bash
git config --global core.editor "code --wait"
```

```bash
git config --global pull.rebase false
```

Review the configuration:

```bash
git config --global --list
```

## 13. Use Windows Git Credential Manager from WSL

Inside WSL, configure Git to use the Git Credential Manager installed by Git for Windows:

```bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager.exe"
```

Confirm it:

```bash
git config --global --get credential.helper
```

The first HTTPS operation against GitHub may open a Windows authentication flow. After authentication, credentials can be stored by Windows Credential Manager rather than placing a token directly in Git configuration.

### Personal Access Token fallback

A GitHub Personal Access Token is useful when a tool or workflow explicitly requires one, but it is not the primary authentication method in this setup.

GitHub token settings:

https://github.com/settings/tokens

Treat a token like a password. Do not commit it to a repository or place it in a Markdown guide.

## 14. Create the development workspace

Create a directory inside the Linux filesystem:

```bash
mkdir -p ~/code
```

Move into it:

```bash
cd ~/code
```

Avoid storing active development repositories under `/mnt/c/...` unless there is a specific reason to do so. Keeping Linux development files in the WSL filesystem generally gives the cleanest Linux toolchain behavior.

You can open the current WSL directory in Windows File Explorer with:

```bash
explorer.exe .
```

## 15. Optional: PowerToys

Microsoft PowerToys adds useful Windows productivity utilities such as **FancyZones**.

Official documentation:

https://learn.microsoft.com/windows/powertoys/

For a development workstation, this is optional rather than a requirement.

## 16. Final checks

Run these checks inside WSL:

```bash
git --version
```

```bash
echo $SHELL
```

```bash
code --version
```

From PowerShell:

```powershell
wsl --list --verbose
```

