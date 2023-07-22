# Common Commands for Linux and Mac OS

This document is a markdown dictionary with copy and paste commands that can be used for Linux Flavors as well as Mac OS

## Table of Contents:

[**File System**](#fileSystem)

- [`cd` | Change Directory](#cd)
- [`pwd` | Print Working Directory](#pwd)
- [`ls` | List files and Directories](#ls)
- [`mkdir` | Make Directories](#mkdir)
- [`rmdir` | Remove Directories](#rmdir)
- [`rm` | Remove Files and Directories](#rm)
- [`cp` | Copy Files and Directories](#cp)
- [`mv` | Move or Rename files and Directories](#mv)
- [`nano` | Easy-to-use text editor](#nano)
- [`touch` | Create an empty file](#touch)
- [`cat` | Concatenate and display the contents of a file ](#cat)
- [`more` | Display file content one screen at a time](#more)
- [`tail` |  Display the last lines of a file](#tail)
- [`ln` | Create a link from a file](#ln)
- [`find` | Search for files and directories](#find)
- [`grep` | Search for a pattern in files](#grep)
- [`wc` | Word, Character, and line Count](#wc)
- [`chmod` | Change Files and Directories Permissions](#chmod)
- [`chown` | Change Owner of Files and Directories](#chown)
- [`chgrp` | Change Group of Files and Directories](#chgrp)
- [`df` | Display disk space usage of the file system](#df)
- [`du` | Estimate file and directory space usage](#du)
- [`mount` | Mount a file system or device](#mount)
- [`umount` | Unmount a file system or device](#umount)
- [`file` | Determine the file type](#file)
- [`stat` | Display file or file system status](#stat)
- [`tar` | Archive files](#tar)
- [`gzip` | Compress files](#gzip)
- [`gunzip` | Decompress files compressed with gzip](#gunzip)
- [`zip` | Package files into a zip archive](#zip)
- [`unzip` | Extract files from a zip archive](#unzip)

[**System and Service manager**](#systemServices)

- [`sudo` | Execute a command with superuser (root) privileges ](#sudo)
- [`su` | Switch to another user account or become the superuser ](#su)
- [`useradd` | Create a new user account ](#useradd)
- [`userdel` | Delete a user account ](#userdel)
- [`passwd` | Change the password of a user account ](#passwd)
- [`groupadd` | Create a new group ](#groupadd)
- [`groupdel` | Delete a group ](#groupdel)
- [`ps` | Process Status ](#ps)
- [`top` | Display real-time information about the system's current processes. ](#top)
- [`systemctl` | System and service manager for a Modern Linux OS](#systemctl)
- [`journalctl` | View logs for a service on a Modern Linux OS](#journalctl)
- [`kill` | : Terminate processes using their process IDs (PIDs)](#kill)
- [`shutdown` | Shutdown or restart the system](#shutdown)
- [`reboot` | Reboot the system](#reboot)
- [`uname` | Print System Operating System Information](#uname)
- [`hostname` | Display or set the system's hostname](#hostname)
- [`date` | Display or set the system date and time](#date)
- [`uptime` | Show how long the system has been running](#uptime)
- [`free` | Display the system's memory usage](#free)
- [`fdisk` | Partition table manipulator for creating, deleting, and managing disk partitions](#fdisk)
- [`lsusb` | List USB devices](#lsusb)
- [`lsdev` | List devices](#lsdev)
- [`iptables` | Configure firewall rules (IPv4)](#iptables)
- [`ufw` | Uncomplicated Firewall - a user-friendly interface for managing iptables (Ubuntu and Debian-based systems)](#ufw)

[**Remote Connectivity**](#remoteConnectivity)

- [`ssh` | Secure Shell command for remote login and executing commands on a remote machine securely](#ssh)
- [`sshuttle` | Create a secure VPN tunnel using SSH](#sshuttle)
- [`scp` | Securely copy files between local and remote machines](#scp)
- [`sftp` | Secure File Transfer Protocol for interactive file transfers between local and remote machines](#sftp)
- [`rsync` | Synchronize files and directories between local and remote systems](#rsync)

[**Networking**](#networkingCommands)

- [`ping` |  Send ICMP echo request packets to test network connectivity](#ping)
- [`ifconfig` | Display or configure network interfaces](#ifconfig)
- [`netstat` | Display network statistics](#netstat)
- [`wget` | Non-interactive network downloader](#wget)
- [`curl` | Command line tool and library for transferring data with URLs](#curl)
- [`nc` | Netcat, a versatile networking utility that can act as a simple TCP/UDP client and server](#nc)
- [`nmap` | Network exploration tool and security / port scanner](#nmap)
- [`ip` | A versatile command for network interface configuration and management](#ip)
- [`dig` | DNS lookup tool for querying DNS servers and retrieving DNS records](#dig)
- [`arp` | Display and modify the ARP (Address Resolution Protocol) cache](#dig)

[**Package Management**](#packageManagement)

- [`apt-get` | Command-line tool for handling packages in Debian-based systems](#apt-get)
- [`yum` | Package manager for systems based on Fedora/RHEL](#yum)
- [`pacman` | Package manager for Arch Linux](#pacman)

[**Other**](#otherCommands)

- [`man` | Display manual information on a command](#man)
- [`history` | Display history of commands performed by a user](#history)
- [`alias` | Create an alias of a command](#alias)

## <a name="fileSystem"></a> File System

### <a name="cd"></a> `cd` *also known as* **Change Directory**

Description:

> This command, stands for "Change Directory" in Linux. This command is essential for navigating through different directories within a Linux file system. This command allows users to move swiftly and efficiently within the file hierarchy.

Examples:

`cd` or `cd ~`

> Takes you to your users home directory

`cd /`

> Takes you to the root of the File System

`cd ..`

> Takes you back one directory

`cd ../../`

> Takes you back two directories

`cd /etc/systemd/system`

> This will take you to the directory *System* that is within *Systemd*, within *etc*

---

### <a name="pwd"></a> `pwd` *also known as* **Print Working Directory** 

Description:

> This command is used to display the full path of the current directory in which the user is working. This command is beneficial for keeping track of the user's location within the complex file hierarchy of Linux.


Examples:

`pwd`

> Displays to the Command Line Interface the current directory in which the user is working

---

### <a name="ls"></a> `ls` *also known as* **List**

Description:

> This command stands for "List" in Linux. This command is used to display the contents of the current directory, including files and subdirectories. This command provides a clear and concise overview of the items within the current location in the file system.

**Available Flags:**

`-l` ***(long format)***
>This option displays detailed information about files and directories, including permissions, owner, group, size, modification date, and more.

`-a` ***(all)***
> This option shows all files, including hidden files (files starting with a dot "."), which are not normally displayed.

`-h` ***(human-readable)***
>With this option, file sizes are displayed in a human-readable format, such as KB, MB, or GB.

`-R` ***(recursive)***
>This flag is used to list the contents of directories recursively, including subdirectories.

`-t` ***(time sorting)***
>The -t option sorts files by their modification time, with the most recently modified files shown first.

`-r` ***(reverse sorting)***
>This option reverses the order of the output, showing files in reverse order.

`-S` ***(size sorting)***
>This flag sorts files by their sizes, with the largest files listed first.

`-G` ***(colorized output)***
>With this option, the output is colorized to make it easier to distinguish file types and attributes.


Examples:

`ls`

> Basic list of all files and directories in the current users directory

`ls -la`

> list of all files and directories in the current users directory in long format and all files (including hidden ones)

`ls -lahS`

> list of all files and directories in the current users directory in long format, all files, file size in human readable format, and files sorted by there size.

---

### <a name="mkdir"></a> `mkdir` *also known as* **Make Directory**

Description:

> This command is used to create a new directory within the file system. This command offers users the ability to organize their files by creating separate directories for different purposes.

**Available Flags:**

`-m` or `--mode` ***(permissions mode)***
>Allows you to specify the permissions (mode) of the new directory in octal notation.

`-p` or `--parents` ***(Parent Directories)***
> This flag enables the creation of parent directories if they do not exist. It prevents an error from being displayed if the parent directory is missing.


Examples:

`mkdir New\ Folder`

> Create a directory in the Users Current Working Directory called "New Folder"

`mkdir data`

> Create a directory in the Users Current Working Directory called "data"

`mkdir -p data/examples`

> Create a directory in the Users Current Working Directory then proceeding down. If the Directory does exist it will continue down, otherwise it'll make it. This command example will create a Directory called "data", then within it a Directory called "examples"

`mkdir -p /data/New\ Folder/example`

> Creates the full directory starting from the root of the filesystem. If the Directory does exist it will continue down, otherwise it'll make it. This command example will create a Directory called "data", then within it a Directory called "New Folder" then another inside called "Example"

---

### <a name="rmdir"></a> `rmdir` *also known as* **Remove Directory** 

Description:

> The `rmdir` command is used to remove empty directories within the file system in Linux. Note that this command will only delete empty directories. If a directory contains files or subdirectories, `rmdir` will fail.

**Available Flags:**

`-p` or `--parents` ***(Remove Directory and its Parents)***
>This flag will attempt to remove the directory hierarchy. If a specified directory is successfully removed, `rmdir` will then attempt to remove the parent directory, and so on, until it encounters a directory it cannot remove or until all specified directories and their parents have been removed.

Examples:

`rmdir FolderName`

>Attempts to remove the directory named "FolderName" in the current working directory. This will succeed if the directory is empty.

`rmdir -p FolderName/SubFolder`

>Attempts to remove "SubFolder" and its parent directory "FolderName" in the current working directory. Both directories must be empty for this to succeed.

---
### <a name="rm"></a> `rm` *also known as* **Remove Files or Directories** 

Description:

> The `rm` command is used to remove files or directories within the file system in Linux. Unlike `rmdir`, `rm` can remove non-empty directories, particularly when used with the `-r` or `-R` flag.

**Available Flags:**

`-r` or `-R` or `--recursive` ***(Remove Directories and their Contents Recursively)***
> This flag tells `rm` to remove the directory and its contents recursively. When used, `rm` will delete the directory and its contents.

`-f` or `--force` ***(Ignore Nonexistent Files and Arguments, Never Prompt)***
> This flag forces deletion of files without prompting for confirmation. This can be dangerous, so use with caution.

`-i` ***(Prompt Before Every Removal)***
> This flag will prompt you for confirmation before attempting to remove each file.

`-v` or `--verbose` ***(Explain What is Being Done)***
> This option makes `rm` more talkative. It will provide additional detail on what is being done.

Examples:

`rm FileName`
> Removes the file named "FileName" in the current working directory.

`rm .`
> Removes *ALL* files and the *CURRENT* working directory.

`rm *`
> Removes *ALL* files in the current working directory.

`rm -r FolderName`
> Removes the directory named "FolderName" and its contents from the current working directory.

`rm -rf FolderName`
> Removes the directory named "FolderName" and its contents from the current working directory without prompting for confirmation.

`rm -i FileName`
> Prompts for confirmation before attempting to remove the file named "FileName".

---
### <a name="cp"></a> `cp` *also known as* **Copy Files and Directories** 

Description:

> The `cp` command is used to copy files and directories. The items to be copied are specified as the source and the destination where the copy should be placed is specified as the target.

**Available Flags:**

`-r` or `-R` or `--recursive` ***(Copy Directories Recursively)***
> This flag tells `cp` to copy directories recursively. If the source is a directory, this option will cause `cp` to copy the entire directory and its contents to the destination.

`-f` or `--force` ***(Force Copy by Removing the Destination File)***
> This flag forces `cp` to remove the destination file if it cannot be opened for write operations.

`-i` or `--interactive` ***(Prompt Before Overwrite)***
> With this option, `cp` will prompt you for confirmation before overwriting any existing files.

`-v` or `--verbose` ***(Explain What is Being Done)***
> This option makes `cp` more talkative. It will provide additional detail on what is being done.

Examples:

`cp source.txt destination.txt`
> Copies the file named "source.txt" to "destination.txt". If "destination.txt" exists, it is overwritten.


`cp -r source_directory destination_directory`
> Copies the directory named "source_directory" and its contents to the "destination_directory". If "destination_directory" exists, its contents are updated with the contents of "source_directory". If "destination_directory" doesn't exist, it's created.

`cp -rf source_directory destination_directory`
> This command forcefully copies the directory named "source_directory" and its contents recursively to the "destination_directory". If "destination_directory" exists, its contents are updated with the contents of "source_directory". If "destination_directory" does not exist, it's created. Existing files in the destination directory are overwritten without prompting.


`cp -i source.txt destination.txt`
> Copies "source.txt" to "destination.txt", but prompts for confirmation before overwriting "destination.txt" if it exists.


`cp -v source.txt destination.txt`
> Copies "source.txt" to "destination.txt" and explains what is being done.

---

### <a name="mv"></a> `mv` *also known as* **Move or Rename Files**

Description:

> The `mv` command is used to move or rename files and directories within the file system in Linux. You can move items from one location to another, or simply rename an item in its current location.

**Available Flags:**

`-f` or `--force` ***(Do Not Prompt Before Overwriting)***
> This flag forces `mv` to not prompt for confirmation before overwriting an existing target file.

`-i` or `--interactive` ***(Prompt Before Overwrite)***
> With this option, `mv` will prompt you for confirmation before overwriting any existing files.

`-u` or `--update` ***(Move Only Newer Files)***
> This option makes `mv` move only when the source file is newer than the destination file or when the destination file is missing.

`-v` or `--verbose` ***(Explain What is Being Done)***
> This option makes `mv` more talkative. It will provide additional detail on what is being done.

Examples:

`mv source.txt destination.txt`
> Moves the file named "source.txt" to "destination.txt". If "destination.txt" exists, it is overwritten.

`mv -i source.txt destination.txt`
> Moves "source.txt" to "destination.txt", but prompts for confirmation before overwriting "destination.txt" if it exists.

`mv -v source.txt destination.txt`
> Moves "source.txt" to "destination.txt" and explains what is being done.

`mv -u source.txt destination.txt`
> Moves "source.txt" to "destination.txt" only if "source.txt" is newer than "destination.txt" or if "destination.txt" is missing.

## <a name="systemServices"></a> System and Service manager

## <a name="remoteConnectivity"></a> Remote Connectivity

## <a name="networkingCommands"></a> Networking

## <a name="packageManagement"></a> Package Management

## <a name="otherCommands"></a> Other Commands
