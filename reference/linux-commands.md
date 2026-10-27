# Linux / WSL Command Reference

![Linux commands](../assets/images/linux-commands-banner.png)

This is a practical reference for Ubuntu running inside WSL. It is intentionally not a full Ubuntu administration guide.

## Navigation

```bash
pwd                 # current directory
ls                  # list files
ls -la              # detailed list including hidden files
cd directory        # enter a directory
cd ..               # go up one level
cd ~                # home directory
```

## Files and directories

```bash
mkdir project
mkdir -p parent/child
touch file.txt
cp source destination
cp -r source-dir destination-dir
mv old-name new-name
rm file.txt
rm -r directory
```

Be especially careful with `rm -r`; deleted Linux files do not go to the Windows Recycle Bin.

## Read and edit files

```bash
cat file.txt
less file.txt
head file.txt
tail file.txt
nano file.txt
```

## Search

```bash
find . -name "*.md"
```

```bash
grep -R "text" .
```

If `ripgrep` is installed:

```bash
rg "text"
```

## Permissions

```bash
chmod +x script.sh
```

```bash
ls -l
```

## Packages

```bash
sudo apt update
sudo apt upgrade
sudo apt install package-name
sudo apt remove package-name
sudo apt autoremove
```

## Processes

```bash
ps aux
top
kill PID
```

## System and storage

```bash
uname -a
df -h
du -sh directory
free -h
```

## Network

```bash
ping example.com
curl https://example.com
wget https://example.com/file
ip addr
ss -tuln
```

## Shell helpers

```bash
clear
history
which git
command -v node
source ~/.zshrc
```

## WSL interoperability

Open the current WSL directory in Windows File Explorer:

```bash
explorer.exe .
```

Open the current directory in VS Code:

```bash
code .
```

Windows drives are mounted below `/mnt`, for example:

```text
/mnt/c
```

For active Linux development projects, prefer a directory inside your WSL home such as `~/code` instead of working directly under `/mnt/c`.
