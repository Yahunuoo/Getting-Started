# ![ubuntu command ](/Assets/images/ubuntu-command-line.png)

## Command Line Commands for Ubuntu

## Table of Contents

- [Basic Commands](#basic-commands)
- [File Management](#file-management)
- [System Information](#system-information)
- [Network Commands](#network-commands)
- [Package Management](#package-management)
- [User Management](#user-management)
- [Disk Usage](#disk-usage)
- [Process Management](#process-management)
- [SSH Commands](#ssh-commands)

## Basic Commands

### `pwd`
Prints the current working directory.

```bash
pwd
```

### `ls`
Lists the files and directories in the current directory.

```bash
ls
```

### `cd`
Changes the current directory.

```bash
cd /path/to/directory
```

### `mkdir`
Creates a new directory.

```bash
mkdir directory_name
```

### `rmdir`
Removes an empty directory.

```bash
rmdir directory_name
```

### `rm`
Removes a file or directory.

```bash
rm file_name
```

### `cp`
Copies files or directories.

```bash
cp source destination
```

### `mv`
Moves or renames files or directories.

```bash
mv source destination
```
## File Management

### `touch`
Creates a new empty file.

```bash
touch file_name
```

### `cat`
Concatenates and displays the content of files.

```bash
cat file_name
```

### `nano`
Opens the nano text editor to edit files.

```bash
nano file_name
```

### `vim`
Opens the vim text editor to edit files.

```bash
vim file_name
```

### `head`
Displays the first few lines of a file.

```bash
head file_name
```

### `tail`
Displays the last few lines of a file.

```bash
tail file_name
```

### `chmod`
Changes the file permissions.

```bash
chmod permissions file_name
```

### `chown`
Changes the file owner and group.

```bash
chown owner:group file_name
```
## System Information

### `uname`
Displays system information.

```bash
uname -a
```

### `hostname`
Shows or sets the system's hostname.

```bash
hostname
```

### `top`
Displays real-time system information, including running processes.

```bash
top
```

### `htop`
An interactive process viewer (must be installed separately).

```bash
htop
```

### `df`
Shows disk space usage.

```bash
df -h
```

### `du`
Displays disk usage of files and directories.

```bash
du -sh /path/to/directory
```

### `free`
Shows memory usage.

```bash
free -h
```

### `uptime`
Displays how long the system has been running.

```bash
uptime
```

### `dmesg`
Prints kernel ring buffer messages.

```bash
dmesg
```

### `lshw`
Lists hardware configuration.

```bash
sudo lshw
```

### `lsblk`
Lists information about block devices.

```bash
lsblk
```

### `lscpu`
Displays information about the CPU architecture.

```bash
lscpu
```

### `lsusb`
Lists USB devices.

```bash
lsusb
```

### `lspci`
Lists PCI devices.

```bash
lspci
```
## Network Commands

### `ifconfig`
Displays or configures network interfaces.

```bash
ifconfig
```

### `ip`
Shows/manages IP addresses and routing.

```bash
ip addr
```

### `ping`
Checks the network connection to a server.

```bash
ping hostname_or_ip
```

### `netstat`
Displays network connections, routing tables, and interface statistics.

```bash
netstat -tuln
```

### `ss`
Another utility to investigate sockets.

```bash
ss -tuln
```

### `traceroute`
Shows the path packets take to a network host.

```bash
traceroute hostname_or_ip
```

### `nslookup`
Queries DNS to obtain domain name or IP address mapping.

```bash
nslookup hostname
```

### `dig`
Performs DNS lookups and displays the answers.

```bash
dig hostname
```

### `wget`
Downloads files from the internet.

```bash
wget url
```

### `curl`
Transfers data from or to a server.

```bash
curl url
```
## Package Management

### `apt-get update`
Updates the package lists for upgrades and new package installations.

```bash
sudo apt-get update
```

### `apt-get upgrade`
Upgrades all the installed packages to the latest versions.

```bash
sudo apt-get upgrade
```

### `apt-get install`
Installs a new package.

```bash
sudo apt-get install package_name
```

### `apt-get remove`
Removes an installed package.

```bash
sudo apt-get remove package_name
```

### `apt-get autoremove`
Removes unnecessary packages that were automatically installed to satisfy dependencies for other packages and are no longer needed.

```bash
sudo apt-get autoremove
```

### `apt-get clean`
Cleans up the local repository of retrieved package files.

```bash
sudo apt-get clean
```

### `dpkg -i`
Installs a package from a .deb file.

```bash
sudo dpkg -i package_file.deb
```

### `dpkg -r`
Removes an installed package.

```bash
sudo dpkg -r package_name
```

### `dpkg -l`
Lists all installed packages.

```bash
dpkg -l
```
## User Management

### `adduser`
Adds a new user to the system.

```bash
sudo adduser username
```

### `deluser`
Removes a user from the system.

```bash
sudo deluser username
```

### `usermod`
Modifies a user account.

```bash
sudo usermod options username
```

### `passwd`
Changes a user's password.

```bash
passwd username
```

### `chage`
Changes user password expiry information.

```bash
sudo chage options username
```

### `groups`
Shows the groups a user is a member of.

```bash
groups username
```

### `id`
Displays user and group IDs.

```bash
id username
```

### `who`
Shows who is logged on.

```bash
who
```

### `last`
Shows the last logins of users.

```bash
last
```

### `su`
Switches to another user account.

```bash
su - username
```

### `sudo`
Executes a command as another user, typically root.

```bash
sudo command
```
## Disk Usage

### `df`
Displays the amount of disk space available on the file system.

```bash
df -h
```

### `du`
Estimates file space usage.

```bash
du -sh /path/to/directory
```

### `fdisk`
Manipulates disk partition table.

```bash
sudo fdisk -l
```

### `mkfs`
Builds a Linux file system.

```bash
sudo mkfs -t ext4 /dev/sdX1
```

### `mount`
Mounts a file system.

```bash
sudo mount /dev/sdX1 /mnt
```

### `umount`
Unmounts a file system.

```bash
sudo umount /mnt
```

### `fsck`
Checks and repairs a Linux file system.

```bash
sudo fsck /dev/sdX1
```

## Process Management

### `ps`
Displays information about active processes.

```bash
ps aux
```

### `top`
Displays real-time information about running processes.

```bash
top
```

### `htop`
An interactive process viewer (must be installed separately).

```bash
htop
```

### `kill`
Terminates a process by PID.

```bash
kill PID
```

### `killall`
Terminates all processes by name.

```bash
killall process_name
```

### `pkill`
Terminates processes based on a pattern.

```bash
pkill pattern
```

### `nice`
Starts a process with a specified priority.

```bash
nice -n priority command
```

### `renice`
Changes the priority of an existing process.

```bash
renice priority -p PID
```

### `bg`
Resumes a suspended job in the background.

```bash
bg job_id
```

### `fg`
Brings a background job to the foreground.

```bash
fg job_id
```

### `jobs`
Lists the active jobs.

```bash
jobs
```
## SSH Commands

### `ssh`
Connects to a remote host.

```bash
ssh user@hostname
```

### `ssh-keygen`
Generates an SSH key pair.

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

### `ssh-copy-id`
Copies the SSH key to a remote host.

```bash
ssh-copy-id user@hostname
```

### `scp`
Copies files between hosts over SSH.

```bash
scp source_file user@hostname:/path/to/destination
```

### `sftp`
Transfers files using the SSH File Transfer Protocol.

```bash
sftp user@hostname
```