# Configuring JavaScript environment

>**1- install nvm**

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

>ompleted installation of nvm

![!ompleted installation of nvm](../Assets/completed-installation-of-nvm.png)

Restart the Terminal application now.

>After starting up the Terminal again, run this command to check the version of nvm

```bash
nvm --version 
```

>**2- install node.js**

syntax = nvm install `Enter the required release`

ask NVM which versions of Node are available

```bash
nvm list-remote
```

It’s a very long list. You can install a version of Node by writing in any of the release versions listed. For instance, to get version v20, then run

```bash
nvm install 
```

> note: command not found: nvm error

Copy this command block and run it in the terminal, which will point to the nvm directory in your ~/.zshrc file

```bash
cat << EOF >> ~/.zshrc

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \\. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \\. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
EOF

```

Restart your terminal. You should now be able to run the nvm --version command and get a version number in response
