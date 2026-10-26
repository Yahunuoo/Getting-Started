# Getting Started

![Getting Started](./assets/images/home-banner.png)

Personal setup guide for preparing a **Windows 11 development workstation** using **WSL 2 + Ubuntu**, with the development tools installed in the correct place for a Windows/WSL workflow.

> Last reviewed: 2026-10-26

## Setup path

Follow these pages in order when preparing a new computer:

1. [Windows 11 + WSL development setup](./windows-11/README.md)

After the initial setup, use these as references:

- [VS Code](./tools/vscode.md)
- [Git & GitHub](./tools/git-github.md)
- [Linux / WSL commands](./reference/linux-commands.md)
- [Windows / WSL commands](./reference/windows-commands.md)
- [Programming resources](./resources.md)

## Environment model

This guide uses the following model:

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

Keep development projects inside the Linux filesystem, for example:

```text
~/code
```

Use Windows for desktop applications such as VS Code and Windows Terminal, and use WSL/Ubuntu for the development command line and project files.
