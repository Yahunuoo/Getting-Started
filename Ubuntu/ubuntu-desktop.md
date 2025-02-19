# ![install - 2025](/Assets/images/ubuntu-desktop.png)

## Configuring a development environment Ubuntu desktop

## [the bgining updating ubuntu](ubuntu-desktop.md)

```bash
sudo apt update && sudo apt upgrade
```

## [install vscode](ubuntu-desktop.md)

1. [Download and install the `.deb` package for VS Code](https://code.visualstudio.com/)
2. [Additional extensions](Extensions.md)

> 📌 ***open vscod and turn on `Auto Save` setting, is in the File menu***

## [install git](/Ubuntu/README.md)

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

## [again updating ubuntu](ubuntu-desktop.md)

```bash
sudo apt update && sudo apt upgrade
```

## install curl

Since you already have the terminal open, take the opportunity to install curl, which will let you install applications with just a URL, as you'll see us do soon. Use this command:

```bash
sudo apt install curl
```

## install Zsh

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

## install Oh My Zsh**

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

>[!NOTE]
> 📌 ***Note that your prompt has now changed to simply be `~` This is the desired outcome***

![oh my zsh!](/Assets/images/Oh-My-Zsh.png)

> ***end the session `and` go to next step***

## step 5

[Configuring a .gitignore global file](../Assets/gitignore_global.md)

## step 6

[Setting up and preparing the programming language environment](../Programming-Language-Environment/README.md)

>[!NOTE]
> 📌 ***setup to start developing in ubuntu has done***
