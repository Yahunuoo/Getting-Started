# Visual Studio Code

![VS Code](../assets/images/vscode-banner.png)

VS Code should be installed on **Windows** and connected to the Linux development environment through the Microsoft **WSL** extension.

## Required

- [Visual Studio Code](https://code.visualstudio.com/)
- [WSL extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)

## Recommended JavaScript extensions

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) — useful for static HTML/CSS/JS projects
- [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons) — optional UI improvement

Install project/language extensions in the **WSL context** when VS Code indicates they need to run inside WSL.

## Useful settings

### Auto Save

Open:

```text
File → Auto Save
```

### Open the current WSL directory

```bash
code .
```

### Command Palette

```text
Ctrl + Shift + P
```

## Verify WSL connection

When working on a WSL project, VS Code should show the WSL remote indicator in the lower-left area of the window.
