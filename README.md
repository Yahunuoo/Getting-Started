# Getting Started

![Getting Started](./assets/images/home-banner.png)

A personal setup guide for preparing a **Windows 11 development workstation** with **WSL 2 + Ubuntu**, placing each development tool in the right environment for a clean and reliable Windows/WSL workflow.

> Last reviewed: 2026-10-26

## Setup path

Use these pages in order when setting up a new computer:

1. [Windows 11 + WSL development setup](./windows-11/README.md)

After the initial setup, use the following pages as references:

- [VS Code](./tools/vscode.md)
- [Git & GitHub](./tools/git-github.md)
- [Linux / WSL commands](./reference/linux-commands.md)
- [Windows / WSL commands](./reference/windows-commands.md)
- [Programming resources](./resources.md)

## Environment model

This guide follows the model below:

```text
Windows 11
├── Windows Terminal
├── Visual Studio Code
├── Git for Windows
│   └── Git Credential Manager
│
└── WSL 2
    └── Ubuntu
        ├── Git
        ├── Zsh / Oh My Zsh
        ├── project files
        └── language runtimes such as Node.js
```

### Important rule

Keep active development projects inside the Linux filesystem, for example:

```text
~/code
```

Use Windows for desktop applications such as VS Code and Windows Terminal. Use WSL/Ubuntu for the development command line, runtime tools, and project files.

![Getting Started](./assets/images/all-set.webp)
