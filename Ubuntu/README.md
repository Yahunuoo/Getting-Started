# Configuring a development environment to Ubuntu

## step 1

>**Updating and upgrading packages**

```bash
sudo apt update && sudo apt upgrade
```

![!Updating](../Assets/Updating.png)

>**curl**

Since you already have the terminal open, take the opportunity to install curl, which will let you install applications with just a URL, as you'll see us do soon. Use this command:

```bash
sudo apt install curl
```

>**Zsh**

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

![The terminal after installing `zsh`.](../Assets/terminal.png)

Enter `2` to accept the default configuration.

Your terminal prompt should look a little different now!

![zsh in action!](../Assets/terminal-2.png)

Let's confirm it worked with this command:

```bash
echo $SHELL
```

This should print **`/usr/bin/zsh`**

![zsh in action!](../Assets/terminal-3.png)

## step 2

>**Oh My Zsh**

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

![oh my zsh!](../Assets/Oh-My-Zsh.png)

>[!NOTE]
> 📌 ***Note that your prompt has now changed to simply be `~` This is the desired outcome, end the session `and` go to next step***

## step 3

[install & Configuring VSCode](../VSCode/Ubuntu-Configuring-VSCode.md)

## step 4

[Configuring | Generate access token GitHub](../GitHub)
