# Overall Commands and more for Linux and Mac OS

This document is a markdown dictionary with copy and paste commands that can be used for most Linux Flavors as well as Mac OS. Some commands are operating system specific and will mark as such.

## <a name="tableOfContents"></a> Table of Contents:

### [**File System**](#fileSystem)

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

### [**System and Service manager**](#systemServices)

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

### [**Remote Connectivity**](#remoteConnectivity)

- [`ssh` | Secure Shell command for remote login and executing commands on a remote machine securely](#ssh)
- [`sshuttle` | Create a secure VPN tunnel using SSH](#sshuttle)
- [`scp` | Securely copy files between local and remote machines](#scp)
- [`sftp` | Secure File Transfer Protocol for interactive file transfers between local and remote machines](#sftp)
- [`rsync` | Synchronize files and directories between local and remote systems](#rsync)

### [**Networking**](#networkingCommands)

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

### [**Web Hosting and Services**](#webServices)

- [`certbot` | A Command to issue self signing Certicates (SSL)](#certbot)
- [`nginx` | A Servicing Application that serves Proxies and Web Services](#nginx)

#### **- NGINX configs**

- [`http_redirect_https` | Config for All Traffic to Server Redirecting from HTTP to HTTPS](#http_redirect_https)
- [`single_view_application`  | Serving a Single Page Web Application](#vue_service)
- [`proxy_service`  | Proxying a Webservice through NGINX](#nginx_proxy_service)

### [**Package Management**](#packageManagement)

- [`apt-get` | Command-line tool for handling packages in Debian-based systems](#apt-get)
- [`yum` | Package manager for systems based on Fedora/RHEL](#yum)
- [`pacman` | Package manager for Arch Linux](#pacman)
- [`brew` | Missing Package manager for Mac OS](#brew)
- [`pip` | Package Installer for Python](#pip)


### [**Other**](#otherCommands)

- [`man` | Display manual information on a command](#man)
- [`history` | Display history of commands performed by a user](#history)
- [`alias` | Create an alias of a command](#alias)

### [**Symbols**](#symbols)

- [` ~ ` | Tilde | Users Home Directory](#tilde)
- [` | ` | Vertical Line | Pipe ](#pipe)
- [` * ` | Asterisk | Wildcard](#asterisk)
- [` ? ` | Question Mark | Wildcard](#questionMark)
- [` ! ` | Exclamation Mark | Bang ](#exclamationMark)
- [` $ ` | Dollar Sign | Variable ](#dollarSign)
- [` ' ` | Quotation | Text Literal ](#quotation)
- [` " ` | Double Quotation | Text Literal with Expansions ](#doubleQuotation)
- [` . ` | Dot | Current Directory ](#dot)
- [` .. ` | Double Dot | Parent Directory ](#doubleDot)
- [` ../ ` | Double Dot Slash | Relative Path ](#doubleDotSlash)
- [` / ` | Forward Slash | Directory Seperation ](#forwardSlash)
- [` > ` | Greater Than | Output Direction ](#greaterThan)
- [` < ` | Less Than | Input Direction ](#lessThan)
- [` >> ` | Double Greater Than | Append Output ](#doubleGreaterThan)
- [` \ ` | Backslash | Escape Character ](#backslash)

### [**Command Line Shortcuts**](#shortcuts)

- Navigation:

    - `Ctrl + A` : Move cursor to the beginning of the line.
    - `Ctrl + E`: Move cursor to the end of the line.
    - `Ctrl + B` or` Left Arrow`: Move cursor one character backward.
    - `Ctrl + F` or `Right Arrow`: Move cursor one character forward.
    - `Alt + B`: Move cursor one word backward.
    - `Alt + F`: Move cursor one word forward.
- Editing:

    - `Ctrl + U`: Clear the line before the cursor.
    - `Ctrl + K`: Clear the line after the cursor.
    - `Ctrl + W`: Delete the word before the cursor.
    - `Alt + D`: Delete the word after the cursor.
    - `Ctrl + Y`: Paste the last item deleted or cut *(after using Ctrl + U/K/W)*.
- History:

    - `Ctrl + R`: Search command history interactively (reverse search).
    - `Ctrl + G`: Exit history search mode without running a command.
    - `Up Arrow` or `Ctrl + P`: Go to the previous command in history.
    - `Down Arrow` or `Ctrl + N`: Go to the next command in history.
    - `!!`: Repeat the last command.
    - `!n`: Repeat the nth command from history *(replace `n` with the command number)*.
- Tab Completion:

    - `Tab`: Auto-complete file and directory names.
    - `Tab + Tab`: Display a list of possible completions (double tap Tab).
    - `Alt + /`: Auto-complete a command using Bash's "word-based" completion.
- Job Control:

    - `Ctrl + C`: Terminate the current foreground process.
    - `Ctrl + Z`: Suspend the current foreground process and put it in the background.
    - `jobs`: List the background jobs.
    - `bg`: Resume a suspended background job.
    - `fg`: Bring a background job to the foreground.
- Miscellaneous:

    - `Ctrl + L`: Clear the screen (equivalent to the `clear` command).
    - `Ctrl + D`: Exit the current shell (equivalent to typing `exit`).

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

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="pwd"></a> `pwd` *also known as* **Print Working Directory** 

Description:

> This command is used to display the full path of the current directory in which the user is working. This command is beneficial for keeping track of the user's location within the complex file hierarchy of Linux.


Examples:

`pwd`

> Displays to the Command Line Interface the current directory in which the user is working

###### [ ← Back to table of contents ](#tableOfContents)
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

###### [ ← Back to table of contents ](#tableOfContents)
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

###### [ ← Back to table of contents ](#tableOfContents)
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

###### [ ← Back to table of contents ](#tableOfContents)
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

###### [ ← Back to table of contents ](#tableOfContents)
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

###### [ ← Back to table of contents ](#tableOfContents)
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

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="nano"></a> `nano` *also known as* **Nano's ANOther editor**

Description:

> The `nano` command is used to open the Nano text editor in a Linux terminal. This editor is a simple, user-friendly, and lightweight text editor used for creating and editing files. It offers basic features like syntax coloring, search and replace, indentation, and tab completion.

**Available Flags:**

`-B` or `--backup` ***(Backup Mode)***
> Makes a backup of the existing file before saving the changes.

`-I` or `--ignorercfiles` ***(Ignore nano's rc files)***
> Does not look at the nanorc files for configuration settings.

`-m` or `--mouse` ***(Enable Mouse Support)***
> Enables mouse support, if available for your system.

`-R` or `--restricted` ***(Restricted Mode)***
> Enables restricted mode. This means that it won't allow the user to write a new file or to read an existing one.

`-Y` ***(Syntax Highlighting Group)***
> Uses this group for syntax highlighting.

Examples:

`nano`

> Opens a new blank buffer in Nano

`nano filename`

> Opens 'filename' in Nano for editing. If 'filename' does not exist, it creates a new file with that name

`nano -B filename`

> Opens 'filename' in Nano with backup mode, which creates a backup file with a tilde '~' appended to the file name

`nano -l filename`

> Opens 'filename' in Nano with line numbers displayed

`nano +10 filename`

> Opens 'filename' in Nano and positions the cursor at line 10

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="touch"></a> `touch` *also known as* **Change File Timestamps**

Description:

> The `touch` command in Linux is used to create new, empty files. It can also be used to update the timestamps on existing files and directories, without modifying their content. This command is helpful when you need to quickly create a file or update the access or modification times.

**Available Flags:**

`-a` ***(Change Access Time)***
> Changes only the access time of the file.

`-m` ***(Change Modification Time)***
> Changes only the modification time of the file.

`-r` ***(Use Reference File's Timestamps)***
> Uses the timestamp of the reference file instead of the current time.

`-t` ***(Specify Timestamps)***
> Uses the specified time as the timestamp, instead of the current time.


Examples:

`touch filename`

> Creates a new file named 'filename' if it does not already exist. If the file exists, it updates the access and modification timestamps

`touch -a filename`

> Changes the access time of the file 'filename'. The file's modification time is not changed

`touch -m filename`

> Changes the modification time of the file 'filename'. The file's access time is not changed

`touch -c filename`

> Does not create a new file if 'filename' does not exist, only updates the timestamps on existing files

`touch -t 202307221530 filename`

> Sets the access and modification times of 'filename' to 15:30 (3:30 PM), July 22, 2023

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="cat"></a> `cat` *also known as* **Concatenate**

Description:

> The `cat` command in Linux is used for creating, viewing, and concatenating files. `cat` stands for "concatenate", which means to combine. This command is most often used to display the contents of one or more files in the terminal.

**Available Flags:**

`-b` ***(Number Non-blank Output Lines)***
> Numbers all non-blank output lines.

`-n` ***(Number All Output Lines)***
> Numbers all output lines.

`-s` ***(Squeeze Blank Lines)***
> Squeezes multiple adjacent blank lines.

`-E` ***(Display End-of-line Markers)***
> Displays a dollar sign (`$`) at the end of each line.

`-T` ***(Display Tab Characters)***
> Displays tab characters as `^I`.


Examples:

`cat filename`

> Displays the contents of 'filename' on the screen

`cat file1 file2`

> Concatenates (joins) 'file1' and 'file2' and displays the result on the screen

`cat file1 file2 > file3`

> Concatenates 'file1' and 'file2', and redirects the result to 'file3'. If 'file3' already exists, it is overwritten. If 'file3' does not exist, it is created

`cat > filename`

> Creates a new file named 'filename' and allows you to start typing content for that file directly in the terminal. Press `CTRL+D` to finish and return to the terminal prompt

`cat >> filename`

> Appends standard input or another file's contents to the end of 'filename'

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="more"></a> `more` *also known as* **Pager**

Description:

> The `more` command in Linux is used to view the contents of a file in a terminal one screen at a time. The `more` command pauses after displaying a screenful of text and provides a prompt at the bottom of the screen. It is helpful when you want to read the contents of a large file without scrolling.

**Available Flags:**

`-d` ***(Provide more Information)***
> Provide more information and prompts.

`-l` ***(Do not Pause after Form Feed)***
> Does not pause after form feed.

`-f` ***(Count Logical Lines)***
> Counts logical, rather than screen lines (i.e., long lines are not folded).

`-p` ***(Clean Screen)***
> Cleans the screen before displaying the page.

`-c` ***(Clean Screen per File)***
> Cleans the screen before displaying the page for each file.

Examples:

`more filename`

> Displays the contents of 'filename' on the screen, one page at a time. Press `space` to go to the next page or `enter` to go to the next line

`more -n 5 filename`

> Displays 'filename' 5 lines at a time

`more +10 filename`

> Starts displaying 'filename' from line 10

`ls | more`

> Lists files and directories in the current directory and pipes the output to `more` to make it easier to read

`more file1 file2`

> Displays the contents of 'file1' and 'file2', one after the other, using the `more` paging system

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="tail"></a> `tail` *also known as* **Output the Last Part of Files**

Description:

> The `tail` command in Linux is used to display the end of a file. By default, it prints the last 10 lines of the specified files. If more than one file is specified, it precedes each set of output with a header giving the file name. The `tail` command is particularly useful for viewing the newest entries in log files.

**Available Flags:**

`-n` ***(Number of Lines)***
> Outputs the last number of lines, instead of the last 10; or use -n +NUM to output starting with line NUM.

`-f` ***(Follow)***
> Outputs appended data as the file grows.

`-r` ***(Reverse)***
> Outputs the lines in reverse order.

`-v` ***(Always Output Headers)***
> Always outputs headers giving file names.


Examples:

`tail filename`

> Displays the last 10 lines of 'filename'

`tail -n 5 filename`

> Displays the last 5 lines of 'filename'

`tail -f filename`

> Displays the last 10 lines of 'filename' and then outputs appended data as the file grows. This is particularly useful for monitoring log files

`tail -n +5 filename`

> Displays lines starting with line 5 of 'filename'

`tail -q -n 5 file1 file2`

> Quiet mode, displays last 5 lines from 'file1' and 'file2' without showing the file headers

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="ln"></a> `ln` *also known as* **Link**

Description:

> The `ln` command in Linux is used to create links between files and directories. There are two types of links that can be created: hard links and symbolic, or soft, links. Hard links are pointers to the file data itself, whereas symbolic links are pointers to other file paths.

**Available Flags:**

`-s` or `--symbolic` ***(Create a Symbolic Link)***
> Makes a symbolic link instead of a hard link.

`-f` or `--force` ***(Remove Existing Destination Files)***
> Removes existing destination files.

`-n` or `--no-dereference` ***(Treat Link Destination as a Normal File)***
> Treats the link destination as a normal file if it is a symbolic link to a directory.

`-v` or `--verbose` ***(Show What is Being Done)***
> Shows what is being done.


Examples:

`ln file1 file2`

> Creates a hard link named 'file2' that points to the file 'file1'. Both 'file1' and 'file2' share the same data but are named differently

`ln -s file1 file2`

> Creates a symbolic link named 'file2' that points to the file 'file1'. 'file2' is just a pointer to 'file1', not a copy of the data

`ln -s /path/to/directory linkname`

> Creates a symbolic link to a directory. 'linkname' will now point to '/path/to/directory'

`ln -s /path/to/file`

> Creates a symbolic link in the current directory that points to '/path/to/file'. The link will have the same name as the original file

`ln -sf file1 file2`

> Forces the creation of a symbolic link by removing 'file2' if it exists, before creating the link

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="find"></a> `find` *also known as* **Find Files and Directories**

Description:

> The `find` command in Linux is a very powerful tool used to search and locate files and directories based on different criteria such as file name, file type, size, and more. It traverses the file system hierarchy from the file paths specified in the command line.

**Available Flags:**

`-name` ***(File Name)***
> Searches for files by name.

`-iname` ***(Case-insensitive Name)***
> Searches for files by name, ignoring case.

`-type` ***(File Type)***
> Searches for files of a specific type (f for regular files, d for directories, l for symbolic links, etc).

`-mtime` ***(Modification Time)***
> Searches for files modified within a certain number of days.

`-size` ***(File Size)***
> Searches for files of a specific size.


Examples:

`find /home -name test.txt`

> Searches for a file named 'test.txt' in the '/home' directory and all of its subdirectories

`find / -type d -name "mydir"`

> Searches for a directory named 'mydir' in the root directory '/' and all of its subdirectories

`find / -type f -empty`

> Finds all empty files in the root directory '/' and all of its subdirectories

`find /home/user -mtime 0`

> Finds all files in '/home/user' that have been modified within the last day

`find /home/user -size +100M`

> Finds all files in '/home/user' that are larger than 100 Megabytes

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="grep"></a> `grep` *also known as* **Global Regular Expression Print**

Description:

> The `grep` command in Linux stands for "global regular expression print". It's used to search text for lines that match a certain pattern. `grep` is highly versatile and can be used with regular expressions for complex pattern matching.

**Available Flags:**

`-i` or `--ignore-case` ***(Ignore Case Distinctions)***
> Ignore case distinctions in patterns and data.

`-v` or `--invert-match` ***(Invert Match)***
> Select non-matching lines.

`-r` or `-R` or `--recursive` ***(Read all Files under each Directory, Recursively)***
> Recursively search subdirectories listed.

`-l` or `--files-with-matches` ***(Print File Names)***
> Print only names of FILEs containing matches.

`-w` or `--word-regexp` ***(Match Whole Words)***
> Force PATTERN to match only whole words.

Examples:

`grep "pattern" filename`

> Searches for the word 'pattern' within 'filename'

`grep -i "pattern" filename`

> Searches for 'pattern' in 'filename', ignoring case

`grep -r "pattern" .`

> Searches recursively for 'pattern' in the current directory and its subdirectories

`grep -E "[a-z]{3}" filename`

> Uses extended regular expressions to search for any three lowercase letters in a row in 'filename'

`grep -v "pattern" filename`

> Inverts the search, returning all lines in 'filename' that do not contain 'pattern'

`grep "^start" filename`

> Searches 'filename' for lines that start with 'start'

`grep "end$" filename`

> Searches 'filename' for lines that end with 'end'

`grep -E "^.{10}$" filename`

> Uses a regular expression to find lines in 'filename' that are exactly 10 characters long

`echo -e "cat\nbat\nrat\nmat" | grep ".at"`

> Creates a list of words and uses `grep` to print words ending with 'at'

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="wc"></a> `wc` *also known as* **Word, Line, Character, and Byte Count**

Description:

> The `wc` command in Linux is used to find out the number of lines, words, characters, and bytes in a file. `wc` stands for "word count", but it can count more than just words. It can be a handy tool when you need to know the size or length of a file.

**Available Flags:**

`-l` or `--lines` ***(Print the Newline Counts)***
> Counts and prints the number of newline characters in a file.

`-w` or `--words` ***(Print the Word Counts)***
> Counts and prints the number of words in a file.

`-c` or `--bytes` ***(Print the Byte Counts)***
> Counts and prints the number of bytes in a file.

`-m` or `--chars` ***(Print the Character Counts)***
> Counts and prints the number of characters in a file.

Examples:

`wc filename`

> Returns the number of lines, words, characters, and bytes in 'filename', in that order

`wc -l filename`

> Returns only the number of lines in 'filename'

`wc -w filename`

> Returns only the number of words in 'filename'

`wc -m filename`

> Returns only the number of characters in 'filename'

`wc -c filename`

> Returns only the number of bytes in 'filename'

`ls | wc -l`

> Lists the files and directories in the current directory and pipes the output to `wc -l` to count the number of items

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="chmod"></a> `chmod` *also known as* **Change Mode**

Description:

> The `chmod` command in Linux is used to change the access permissions of files and directories. It allows you to define who can read, write, and execute a file or directory. Permissions can be set using symbolic modes (using letters) or octal modes (using numbers).

**Available Flags:**

`-R` or `--recursive` ***(Change Files and Directories Recursively)***
> Change files and directories recursively.

`-f` or `--silent` or `--quiet` ***(Suppress Most Error Messages)***
> Suppresses most error messages.

`-v` or `--verbose` ***(Output a Diagnostic for Every File Processed)***
> Outputs a diagnostic for every file processed.


Examples:

`chmod u+x filename`

> Gives the user (u) execute (x) permission on 'filename'

`chmod g-w filename`

> Removes write (w) permission for the group (g) on 'filename'

`chmod o=r filename`

> Sets the other (o) permissions to read (r) only on 'filename'

`chmod a+w filename`

> Gives all users (a) write (w) permission on 'filename'

`chmod 755 filename`

> Sets permissions for 'filename' to read, write, execute for the owner, and read, execute for the group and others (equivalent to `u=rwx,g=rx,o=rx`)

`chmod -R 644 directory`

> Recursively (-R) sets read and write permissions for the owner and read permission for the group and others for all files in 'directory' 

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="chown"></a> `chown` *also known as* **Change Owner**

Description:

> The `chown` command in Linux is used to change the owner and group of a file or directory. It allows you to specify who the new owner and group should be. This command is generally used by administrators to change the ownership of files/directories.

**Available Flags:**

`-R` or `--recursive` ***(Operate on Files and Directories Recursively)***
> Operates on files and directories recursively.

`-f` or `--silent` or `--quiet` ***(Suppress Most Error Messages)***
> Suppresses most error messages.

`-v` or `--verbose` ***(Output a Diagnostic for Every File Processed)***
> Outputs a diagnostic for every file processed.


Examples:

`chown newowner filename`

> Changes the owner of 'filename' to 'newowner'

`chown newowner:newgroup filename`

> Changes the owner of 'filename' to 'newowner' and the group to 'newgroup'

`chown -R newowner directory`

> Changes the owner of 'directory' and its contents to 'newowner' recursively

`chown :newgroup filename`

> Changes the group of 'filename' to 'newgroup'. If the owner is not specified, it remains the same

`chown --reference=ref_file target_file`

> Changes the owner and group of 'target_file' to be the same as those of 'ref_file'

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="chgrp"></a> `chgrp` *also known as* **Change Group**

Description:

> The `chgrp` command in Linux is used to change the group ownership of a file or directory. It allows you to specify the new group. This command is often used when a file needs to be accessed by different users, all of whom are members of the same group.

**Available Flags:**

`-R` or `--recursive` ***(Operate on Files and Directories Recursively)***
> Operates on files and directories recursively.

`-f` or `--silent` or `--quiet` ***(Suppress Most Error Messages)***
> Suppresses most error messages.

`-v` or `--verbose` ***(Output a Diagnostic for Every File Processed)***
> Outputs a diagnostic for every file processed.

Examples:

`chgrp newgroup filename`

> Changes the group of 'filename' to 'newgroup'

`chgrp -R newgroup directory`

> Changes the group of 'directory' and its contents to 'newgroup' recursively

`chgrp --reference=ref_file target_file`

> Changes the group of 'target_file' to be the same as that of 'ref_file'

`chgrp newgroup file1 file2 file3`

> Changes the group of 'file1', 'file2', and 'file3' to 'newgroup'

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="df"></a> `df` *also known as* **Disk Free**

Description:

> The `df` command in Linux is used to display the amount of disk space used and available on the file system. By default, the space is shown in 1K blocks, but this can be adjusted to a more human-readable format.

**Available Flags:**

`-h` or `--human-readable` ***(Print Sizes in Human Readable Format)***
> Prints sizes in human readable format (e.g., 1K, 234M, 2G).

`-a` or `--all` ***(Include Dummy File Systems)***
> Includes filesystems having 0 blocks.

`-T` or `--print-type` ***(Print File System Type)***
> Prints the file system type.


Examples:

`df`

> Displays the disk space usage of all mounted filesystems

`df -h`

> Displays the disk space usage in human-readable format (e.g., KB, MB, GB)

`df /home`

> Displays the disk space usage of the '/home' file system

`df -T`

> Displays the disk space usage along with the filesystem type

`df -a`

> Shows the disk space usage of all filesystems, even those with 0 blocks

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="du"></a> `du` *also known as* **Disk Usage**

Description:

> The `du` command in Linux is used to estimate the space usage of files and directories. This command can be used to track down files and directories that are using large amounts of disk space.

**Available Flags:**

`-h` or `--human-readable` ***(Print Sizes in Human Readable Format)***
> Prints sizes in human readable format (e.g., 1K, 234M, 2G).

`-a` or `--all` ***(Write Counts for all Files)***
> Writes counts for all files, not just directories.

`-s` or `--summarize` ***(Display only a Total for each Argument)***
> Displays only a total for each argument.

`-c` or `--total` ***(Produce a Grand Total)***
> Produces a grand total.


Examples:

`du`

> Shows disk usage of the current directory and its subdirectories in kilobytes

`du -h`

> Shows disk usage in a human-readable format (KB, MB, GB)

`du -sh directory`

> Shows a summary (-s) of the total disk usage of 'directory' in human-readable format (-h)

`du -a`

> Shows the disk usage of all files, not just directories

`du -ch directory`

> Displays a grand total usage at the end (-c) and in a human-readable format (-h) for the specified 'directory'

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="mount"></a> `mount` *also known as* **Mount File Systems**

Description:

> The `mount` command in Linux is used to mount file systems. The command attaches a file system (which could be a device, partition, or network share) to a certain point in the directory tree. This is crucial when you want to access the content of the device or partition.

**Available Flags:**

`-a` or `--all` ***(Mount all Filesystems)***
> Mounts all filesystems mentioned in fstab.

`-r` or `--read-only` ***(Mount the Filesystem Read-only)***
> Mounts the filesystem read-only.

`-w` or `--rw` or `--read-write` ***(Mount the Filesystem Read-write)***
> Mounts the filesystem read-write.

`-t` or `--types` ***(Indicate Filesystem Type)***
> Indicates the filesystem type.

Examples:

`mount`

> Displays all file systems that are currently mounted

`mount /dev/sda1 /mnt`

> Mounts the first partition of the first hard disk (sda1) to the /mnt directory

`mount -t type device directory`

> Mounts the 'device' of a specific 'type' (e.g., ext4, nfs, etc.) to a 'directory'

`mount -o options device directory`

> Mounts 'device' to 'directory' with specific 'options' (e.g., read-only, etc.)

`mount -a`

> Mounts all filesystems mentioned in /etc/fstab (useful at boot)

`mount -t iso9660 -o ro /dev/cdrom /mnt/cdrom`

> Mounts a CD-ROM in read-only mode

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="umount"></a> `umount` *also known as* **Unmount File Systems**

Description:

> The `umount` command in Linux is used to unmount mounted file systems. Unmounting is the process of detaching the file system from the directory tree, making it no longer accessible until it is mounted again. It is an important step before physically removing portable storage devices to prevent data corruption.

**Available Flags:**

`-a` or `--all` ***(Umount all Filesystems)***
> Umounts all filesystems mentioned in fstab.

`-f` or `--force` ***(Force Umount)***
> Forces umount in case of unresponsive NFS system.

`-l` or `--lazy` ***(Lazy Umount)***
> Detaches the filesystem now, and cleanup continues in the background.

`-r` or `--read-only` ***(Try to Remount Read-only)***
> Tries to remount unmountable filesystems read-only.


Examples:

`umount /mnt`

> Unmounts the file system that is mounted at /mnt

`umount -a`

> Unmounts all mounted file systems

`umount -t type`

> Unmounts all file systems of a specific 'type' (e.g., nfs, ext4, etc.)

`umount -l /mnt`

> Performs a lazy unmount, detaching the file system immediately, but cleaning up references later

`umount -f /mnt`

> Forces unmount (use with caution as it can cause data loss)

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="file"></a> `file` *also known as* **File Type**

Description:

> The `file` command in Linux is used to determine the type of a file. It's a handy command when you're not sure what a particular file is, as it will try to classify the file's contents according to various tests, including filesystem tests, magic number tests, and language tests.

**Available Flags:**

`-b` or `--brief` ***(Do not Prepend Filenames to Output Lines)***
> Do not prepend filenames to output lines.

`-f` or `--files-from FILE` ***(Read Input from FILE)***
> Reads file names from file.

`-i` or `--mime` ***(Output MIME type Strings)***
> Outputs MIME type strings.

`-z` or `--uncompress` ***(Try to Look Inside Compressed Files)***
> Tries to look inside compressed files.


Examples:

`file filename`

> Determines the type of 'filename'

`file -i filename`

> Gives mime type of 'filename', which can be useful for scripting

`file *`

> Determines the type of all files in the current directory

`file -s /dev/sda1`

> Attempts to determine the filesystem type on the partition sda1

`file -b filename`

> Outputs the information minus the filename (brief mode)

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="stat"></a> `stat` *also known as* **File or File System Status**

Description:

> The `stat` command in Linux is used to display detailed status of a particular file or file system. It provides information like size, permissions, creation time, access time, inode number, and more.

**Available Flags:**

`-c` or `--format=FORMAT` ***(Use the Specified FORMAT instead of the Default)***
> Use the specified FORMAT instead of the default.

`-f` or `--file-system` ***(Display File System Status instead of File Status)***
> Display file system status instead of file status.

`-L` or `--dereference` ***(Follow Links)***
> Follow links.

`-t` or `--terse` ***(Print the Information in Terse Form)***
> Print the information in terse form.


Examples:

`stat filename`

> Displays the status of 'filename'

`stat -c %s filename`

> Displays the size of 'filename' in bytes using the format option -c

`stat -f /`

> Displays the status of the file system where root (/) is located

`stat -L symlink`

> Shows status of the file the symbolic link points to (-L follows symlinks)

`stat --printf="%n %s bytes\n" filename`

> Customizes output using printf formatting. This example shows the name and size of 'filename'

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="tar"></a> `tar` *also known as* **Tape Archive**

Description:

> The `tar` command in Linux is used to create, maintain, modify, and extract files that are archived in the tar format. It's a widely used command for packaging a set of files for distribution or for backup purposes.

**Available Flags:**

`-c` or `--create` ***(Create a New Archive)***
> Create a new archive.

`-x` or `--extract` or `--get` ***(Extract Files from an Archive)***
> Extract files from an archive.

`-f` or `--file=ARCHIVE` ***(Use Archive File or Device ARCHIVE)***
> Use archive file or device ARCHIVE.

`-v` or `--verbose` ***(Verbosely List Files Processed)***
> Verbosely list files processed.

`-z` or `--gzip` or `--gunzip` or `--ungzip` ***(Filter the Archive through Gzip)***
> Filter the archive through gzip.

Examples:

`tar -cvf archive.tar directory/`

> Creates (-c) a new tar archive named 'archive.tar' containing 'directory/', with verbose (-v) output to show what's being included and using file (-f) operation mode

`tar -xvf archive.tar`

> Extracts (-x) the contents of 'archive.tar' with verbose (-v) output to show what's being extracted and using file (-f) operation mode

`tar -tvf archive.tar`

> Lists (-t) the contents of 'archive.tar' with verbose (-v) output and using file (-f) operation mode

`tar -czvf archive.tar.gz directory/`

> Creates a gzipped (-z) tar archive. This is useful for compressing the archive

`tar -xjvf archive.tar.bz2`

> Extracts a bzipped (-j) tar archive. This is for decompressing and extracting the archive

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="gzip"></a> `gzip` *also known as* **GNU zip**

Description:

> The `gzip` command in Linux is used to compress files. Each file is replaced by a gzipped compressed version of itself, with the name original_name.gz. It's widely used for its speed and simplicity, especially for network file transfers and backup operations.

**Available Flags:**

`-k` or `--keep` ***(Keep Input Files)***
> Keep (don't delete) input files.

`-f` or `--force` ***(Force Compression)***
> Force compression or decompression even if the file has multiple links or the corresponding file already exists.

`-d` or `--decompress` or `--uncompress` ***(Decompress)***
> Decompress the compressed file.

`-v` or `--verbose` ***(Verbose Mode)***
> Verbose mode. Display the name and percentage reduction for each file compressed or decompressed.

Examples:

`gzip filename`

> Compresses 'filename' into 'filename.gz' and deletes the original file

`gzip -k filename`

> Compresses 'filename' into 'filename.gz' but keeps (-k) the original file

`gzip -d filename.gz`

> Decompresses 'filename.gz' back to 'filename' (-d stands for decompress)

`gzip -r directory/`

> Recursively (-r) compresses all files in 'directory/' and its subdirectories

`gzip -l filename.gz`

> Lists (-l) information about the gzipped 'filename.gz' file, such as compression ratio

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="gunzip"></a> `gunzip` *also known as* **GNU unzip**

Description:

> The `gunzip` command in Linux is used to decompress files compressed by `gzip`. The compressed file is replaced by an uncompressed file with the original name.

**Available Flags:**

`-k` or `--keep` ***(Keep Input Files)***
> Keep (don't delete) input files.

`-f` or `--force` ***(Force Compression)***
> Force decompression even if the file has multiple links or the corresponding file already exists.

`-c` or `--stdout` or `--to-stdout` ***(Write Output on Standard Output)***
> Write output on standard output; keep original files unchanged.

`-v` or `--verbose` ***(Verbose Mode)***
> Verbose mode. Display the name and percentage reduction for each file compressed or decompressed.


Examples:

`gunzip filename.gz`

> Decompresses 'filename.gz' back to 'filename'

`gunzip -k filename.gz`

> Decompresses 'filename.gz' back to 'filename', but keeps (-k) the original compressed file

`gunzip -c filename.gz > filename`

> Decompresses 'filename.gz' to 'filename' without deleting the compressed file. The -c option writes the output to the standard output

`gunzip -r directory/`

> Recursively (-r) decompresses all gzipped files in 'directory/' and its subdirectories

`gunzip -l filename.gz`

> Lists (-l) information about the gzipped 'filename.gz' file, such as compression ratio

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="zip"></a> `zip` *also known as* **Package and Compress (Zip) Files**

Description:

> The `zip` command in Linux is used to package and compress (archive) files. `zip` is useful for packaging a set of files for distribution, for archiving files, and for saving disk space by temporarily compressing unused files or directories.

**Available Flags:**

`-r` or `--recurse-paths` ***(Travel the Directory Structure Recursively)***
> Travel the directory structure recursively; for example: `zip -r foo.zip foo` or `zip -r foo.zip foo -x \*.o`.

`-m` or `--move` ***(Move Specified Files into the Zip Archive)***
> Move specified files into the zip archive; actually, this deletes the target directories/files after making the specified zip archive.

`-d` or `--delete` ***(Delete Entries from a Zip Archive)***
> For example: `zip -d foo foo/tom/junk foo/harry/\* \*.o`.

`-f` or `--freshen` ***(Freshen: Only Changed Files)***
> Freshen: only changed files. Update entries of the specified files to reflect the disk versions.


Examples:

`zip archive.zip filename`

> Compresses 'filename' into 'archive.zip'

`zip -r archive.zip directory/`

> Recursively (-r) compresses the directory 'directory/' into 'archive.zip'

`zip -m archive.zip filename`

> Compresses 'filename' into 'archive.zip' and then deletes the original file (-m stands for move)

`zip -s 1m archive.zip filename`

> Splits (-s) the compressed file into multiple parts of specified size, in this case, 1 megabyte

`zip -e archive.zip filename`

> Creates a password protected zip file (-e stands for encrypt)

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="unzip"></a> `unzip` *also known as* **Extract Compressed Files in a ZIP Archive**

Description:

> The `unzip` command in Linux is used to extract the contents from the zip archives. It supports password-protected archives. It's handy for extracting files and directories efficiently.

**Available Flags:**

`-l` or `--list` ***(List Archive File Contents)***
> List archive file contents.

`-n` or `--never-overwrite` ***(Never Overwrite Existing Files)***
> Never overwrite existing files; default mode.

`-o` or `--overwrite` ***(Overwrite Existing Files Without Prompting)***
> Overwrite existing files without prompting.

`-d` or `--directory` ***(Extract Files into Dir)***
> Extract files into DIR.

`-x` or `--exclude` ***(Exclude Specified Files)***
> Exclude specified files.


Examples:

`unzip archive.zip`

> Extracts all files from 'archive.zip'

`unzip -l archive.zip`

> Lists (-l) the contents of 'archive.zip' without extracting them

`unzip -d directory/ archive.zip`

> Extracts all files from 'archive.zip' into 'directory/'

`unzip -p archive.zip filename > filename`

> Extracts 'filename' from 'archive.zip' and writes it to standard output

`unzip archive.zip filename`

> Extracts specific 'filename' from 'archive.zip'

###### [ ← Back to table of contents ](#tableOfContents)
---

## <a name="systemServices"></a> System and Service manager

### <a name="sudo"></a> `sudo` *also known as* **Superuser Do**

Description:

> The `sudo` command in Linux allows users to run programs with the security privileges of another user (normally the superuser, or root). Its name is a concatenation of "su" (switch user) and "do" (execute a command). 

**Available Flags:**

`-u` or `--user=USER` ***(Run Command as User USER)***
> Run command as user USER instead of default root.

`-i` or `--login` ***(Simulate Initial Login)***
> Simulates an initial login shell environment.

`-k` or `--reset-timestamp` ***(Reset the Timestamp)***
> Invalidates the user's timestamp by setting the time on it to the epoch.

`-l` or `--list` ***(List User's Privileges or Check a Specific Command)***
> Lists the commands allowed (and forbidden) to a user by the security policy.

Examples:

`sudo command`

> Executes 'command' as the superuser

`sudo -u username command`

> Executes 'command' as 'username'

`sudo -i`

> Opens a new shell as the superuser

`sudo visudo`

> Edits the sudoers file, which defines who can use sudo and how

`sudo !!`

> Executes the previous command as the superuser. '!!' is a shortcut for the previous command in the Bash shell.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="su"></a> `su` *also known as* **Switch User**

Description:

> The `su` command in Linux allows you to run a shell with substitute user and group IDs. By default, without any other arguments, it switches to the root user of the system, requiring the root password.

**Available Flags:**

`-` or `-l` or `--login` ***(Provide an Environment Similar to What the User Would Expect had the User Logged in Directly)***
> Starts the shell as a login shell with an environment similar to a real login.

`-c` or `--command=COMMAND` ***(Pass COMMAND to the Shell with the `-c' Option)***
> Passes a single COMMAND to the shell with the `-c' option.

`-s` or `--shell=SHELL` ***(Run SHELL if /etc/shells Allows it)***
> Runs SHELL if it's allowed by the system's security policy.

Examples:

`su`

> Switches to the root user (will prompt for the root password)

`su -`

> Switches to the root user and changes the environment to root's

`su username`

> Switches to 'username' (will prompt for 'username's password)

`su - username`

> Switches to 'username' and changes the environment to 'username's

`su -c 'command'`

> Runs 'command' as root

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="useradd"></a> `useradd` *also known as* **User Add**

Description:

> The `useradd` command in Linux is used to create new user accounts. It updates the system files with information provided from the command line and with default values from the system.

**Available Flags:**

`-m` or `--create-home` ***(Create the User's Home Directory)***
> Creates the user's home directory as /home/username.

`-d` or `--home-dir HOME_DIR` ***(Specify the User's Home Directory)***
> Specifies the user's home directory.

`-s` or `--shell SHELL` ***(Specify the User's Login Shell)***
> Specifies the user's login shell.

`-u` or `--uid UID` ***(Specify the User's UID)***
> Specifies the user's UID.

`-g` or `--gid GROUP` ***(Specify the User's Initial Login Group)***
> Specifies the user's initial login group.

Examples:

`useradd username`

> Creates a new user named 'username' with default settings

`useradd -m username`

> Creates a new user named 'username' and makes a home directory for them (-m stands for create home directory)

`useradd -g groupname username`

> Creates a new user named 'username' and adds them to 'groupname'

`useradd -s /bin/bash username`

> Creates a new user named 'username' and sets their login shell to Bash

`useradd -d /custom/home/dir username`

> Creates a new user named 'username' with a specified home directory

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="userdel"></a> `userdel` *also known as* **User Delete**

Description:

> The `userdel` command in Linux is used to delete user accounts and related files. It updates the system account files, deleting all entries that refer to the user name 'username'.

**Available Flags:**

`-r` or `--remove` ***(Remove User's Home Directory and Mail Spool)***
> Removes the user's home directory and mail spool as specified in the `passwd` file.

`-f` or `--force` ***(Force Removal of Files, Even if Not Owned by User)***
> Forces removal of the user account, even if the user is still logged in. It also forces `userdel` to remove the user's home directory and mail spool, even if another user uses the same home directory or if the mail spool is not owned by the specified user.

Examples:

`userdel username`

> Deletes the user named 'username'

`userdel -r username`

> Deletes the user named 'username' and their home directory and mail spool (-r stands for remove home directory)

`userdel -f username`

> Force deletes the user 'username' even if they are still logged in (-f stands for force)

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="passwd"></a> `passwd` *also known as* **Password**

Description:

> The `passwd` command in Linux is used to change the user's password. The root user can change the password for any account or specific account.

**Available Flags:**

`-l` or `--lock` ***(Lock the Password of the Named Account)***
> Locks the password of the named account. This option disables a password by changing it to a value which matches no possible encrypted value.

`-u` or `--unlock` ***(Unlock the Password of the Named Account)***
> Unlocks the password of the named account.

`-d` or `--delete` ***(Delete the Password for the Named Account)***
> Deletes the password for the named account.

`-S` or `--status` ***(Display Password Status for the Named Account)***
> Displays password status for the named account.

Examples:

`passwd`

> Changes the password for the current user (prompts for the old and new password)

`passwd username`

> Changes the password for the user 'username' (requires root privileges)

`passwd -l username`

> Locks 'username's account, disabling their password (-l stands for lock)

`passwd -u username`

> Unlocks 'username's account, re-enabling their password (-u stands for unlock)

`passwd -d username`

> Deletes 'username's password, making their account password-less (-d stands for delete)

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="groupadd"></a> `groupadd` *also known as* **Group Add**

Description:

> The `groupadd` command in Linux is used to create a new group definition on the system. It's a low-level utility that is used when creating a new user.

**Available Flags:**

`-g` or `--gid GID` ***(Specify the Numeric GID for the New Group)***
> Specifies the numeric GID for the new group.

`-r` or `--system` ***(Create a System Group)***
> Creates a system group. The numeric identifiers of new system groups are chosen in the SYS_GID_MIN-SYS_GID_MAX range, defined in login.defs, instead of GID_MIN-GID_MAX.


Examples:

`groupadd groupname`

> Creates a new group named 'groupname'

`groupadd -g gid groupname`

> Creates a new group with a specific group ID (gid)

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="groupdel"></a> `groupdel` *also known as* **Group Delete**

Description:

> The `groupdel` command in Linux is used to delete a group definition from the system. The group should be removed from the passwd file and the group file.

**Available Flags:**

(No applicable or commonly used flags for this command)

Examples:

`groupdel groupname`

> Deletes the group named 'groupname'

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="ps"></a> `ps` *also known as* **Process Status**

Description:

> The `ps` command in Linux is used to provide information about the currently running processes, including their process identification numbers (PIDs). You can use this PID to kill a process, etc.

**Available Flags:**

`-e` or `-A` or `--all` ***(Select All Processes)***
> Selects all processes.

`-f` ***(Full Format Listing)***
> Does a full-format listing. This option can be combined with many other UNIX-style options to add additional columns.

`-u` ***(User-oriented Format)***
> Displays the process's user/owner.

`-x` ***(Include Processes Without a Controlling Terminal)***
> Includes processes without controlling terminals.


Examples:

`ps`

> Displays currently running processes for the current shell

`ps -e`

> Displays all the currently running processes

`ps -f`

> Provides a full-format listing, including command lines used to start a process

`ps -u username`

> Shows processes owned by 'username'

`ps -aux`

> Provides detailed information about all processes, system and user ones.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="top"></a> `top` *also known as* **Table of Processes**

Description:

> The `top` command in Linux is used to provide a dynamic real-time view of the running system. It can display system summary information as well as a list of tasks currently being managed by the kernel.

**Available Flags:**

`-d` or `--delay=SECONDS` ***(Specify Delay Between Screen Updates)***
> You can specify the delay between screen updates.

`-u` or `--user=USER` ***(Monitor Only Processes of a Certain User)***
> Monitor only processes of a certain user.

`-p` or `--pid=PID` ***(Monitor Only Certain PIDs)***
> Monitor only certain PIDs. This option can be specified multiple times.

`-b` or `--batch` ***(Batch Mode)***
> Operates in "batch" mode, useful for sending output from `top` to other programs or to a file. In this mode, `top` will not accept command-line input and runs until the iterations limit set by the `-n`/`--iterations` option is reached or until killed.


Examples:

`top`

> Displays real-time view of the running system

`top -u username`

> Shows processes run by 'username'

`top -n 1`

> Displays 'top' output once and exits

`top -b`

> Runs 'top' in batch mode, useful for sending output from 'top' to other programs or to a file

`top -p PID`

> Monitors a specific process by its process ID (PID)

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="systemctl"></a> `systemctl` *also known as* **System Control**

Description:

> The `systemctl` command in Linux is used to manage and control 'systemd' system and service manager. It's a useful command to manage system services, units, and more.

**Available Flags:**

`start` ***(Start One or More Units)***
> Starts one or more units (services, sockets, etc.).

`stop` ***(Stop One or More Units)***
> Stops one or more units.

`restart` ***(Restart One or More Units)***
> Restarts one or more units.

`status` ***(Show Runtime Status of One or More Units)***
> Shows runtime status information about one or more units.

`enable` ***(Enable One or More Unit Files)***
> Enables one or more unit files, as specified on the command line.

`disable` ***(Disable One or More Unit Files)***
> Disables one or more unit files, as specified on the command line.

`-h` or `--help` ***(Print a Short Help Text and Exit)***
> Prints a short help text and exits.

`-a` or `--all` ***(Show All Units, Including Inactive Ones)***
> Show status of all units, including inactive ones.

`-r` or `--recursive` ***(Recursively Start Units in Directories or Dropped in by *.wants/ Symlinks)***
> When operating on units located on the file system, systemctl will recursively descend into directories and follow unit file symlinks specified on the command line.


Examples:

`systemctl`

> Displays the status of all active units

`systemctl start service`

> Starts a service (replace 'service' with the name of the service)

`systemctl stop service`

> Stops a service

`systemctl restart service`

> Restarts a service

`systemctl reload service`

> Reloads the configuration of a service

`systemctl status service`

> Shows the status of a service

`systemctl enable service`

> Enables a service to start at boot

`systemctl disable service`

> Disables a service from starting at boot

`systemctl is-enabled service`

> Checks if a service is enabled to start at boot

`systemctl is-active service`

> Checks if a service is currently active

`systemctl list-units`

> Lists all units that systemd knows about

`systemctl list-unit-files`

> Lists all unit files and their enablement state (enabled, disabled, static, etc.)

`systemctl reboot`

> Reboots the system

`systemctl poweroff`

> Powers off the system

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="journalctl"></a> `journalctl` *also known as* **Journal Control**

Description:

> The `journalctl` command in Linux is used to query the contents of the systemd journal. It's an essential tool for system troubleshooting, enabling administrators to access and filter system log messages.

**Available Flags:**

`-f` or `--follow` ***(Follow the Journal Logs)***
> Shows the real-time updates that are being written to the journal.

`-u` or `--unit=UNIT` ***(Display Logs for a Specific Unit)***
> Shows logs for a specific unit.

`-b` or `--boot` ***(Display Logs from the Current Boot)***
> Shows all messages from the current boot.

`-p` or `--priority=PRIORITY` ***(Filter Output by Priority)***
> Shows messages with a specific priority level (emerg, alert, crit, err, warning, notice, info, debug).

`-r` or `--reverse` ***(Reverse Output Order)***
> Displays newest entries first.

`-k` or `--dmesg` ***(Display Kernel Messages)***
> Displays only kernel messages.


Examples:

`journalctl`

> Shows all logs collected by the journal, presented in a less-like interface

`journalctl -b`

> Shows all logs collected since the last boot

`journalctl -f`

> Follows the journal, similar to 'tail -f'

`journalctl -k`

> Shows all kernel messages

`journalctl -u service`

> Shows logs for a specific service (replace 'service' with the name of the service)

`journalctl --since="2023-07-22 00:00:00"`

> Shows logs since a specified date and time

`journalctl --until="2023-07-22 12:00:00"`

> Shows logs until a specified date and time

`journalctl -p err`

> Filters logs by priority; in this case, showing only errors

`journalctl _PID=1`

> Shows logs for a specific process ID (PID)

`journalctl /usr/sbin/apache2`

> Shows logs for a specific binary

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="kill"></a> `kill` *also known as* **Kill Process**

Description:

> The `kill` command in Linux is used to send a signal to a process. By default, it sends a TERM signal, which requests a process to terminate.

**Available Flags:**

`-s` or `--signal=SIGNAL` ***(Specify the Signal to be Sent)***
> Specifies the signal to be sent. The signal can be specified by using name or number. The default signal is TERM.

`-l` or `--list[=TABLE]` ***(List Signals)***
> Lists the signal names. If an argument is given, it is interpreted as a signal number or a signal name and the corresponding signal name or signal number will be shown.

`-L` or `--table` ***(List Signal Names in a Table)***
> Same as `-l`, but it will print signal names and their corresponding numbers in a table.


Examples:

`kill PID`

> Sends the TERM signal to the process with the specified PID

`kill -9 PID`

> Sends the KILL signal to the process, forcing it to terminate immediately

`killall processname`

> Sends the TERM signal to all processes with the given name

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="shutdown"></a> `shutdown` *also known as* **Shutdown System**

Description:

> The `shutdown` command in Linux is used to shutdown, restart, or halt the system in a safe manner.

**Available Flags:**

`-h` or `--halt` ***(Halt the Machine)***
> Halts the machine.

`-r` or `--reboot` ***(Reboot the Machine)***
> Reboots the machine.

`-P` or `--poweroff` ***(Power-off the Machine)***
> Powers off the machine.

`-c` or `--cancel` ***(Cancel a Pending Shutdown)***
> Cancels a pending shutdown.

Examples:

`shutdown now`

> Shuts down the system immediately

`shutdown -h now`

> Halts the system immediately

`shutdown -r now`

> Reboots the system immediately

`shutdown +10`

> Shuts down the system in 10 minutes

`shutdown 22:00`

> Shuts down the system at 10:00 PM

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="reboot"></a> `reboot` *also known as* **Reboot System**

Description:

> The `reboot` command in Linux is used to reboot the system.

**Available Flags:**

`-f` or `--force` ***(Force Immediate Reboot)***
> Forces immediate reboot, without unmounting or syncing filesystems.

`-n` or `--no-sync` ***(Don't Sync Before Reboot)***
> Doesn't sync before reboot.

Examples:

`reboot`

> Reboots the system immediately

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="uname"></a> `uname` *also known as* **Unix Name**

Description:

> The `uname` command in Linux is used to print system information.

**Available Flags:**

`-a` or `--all` ***(Print All Information)***
> Prints all system information.

`-s` or `--kernel-name` ***(Print the Kernel Name)***
> Prints the kernel name.

`-r` or `--kernel-release` ***(Print the Kernel Release)***
> Prints the kernel release.

`-v` or `--kernel-version` ***(Print the Kernel Version)***
> Prints the kernel version.

`-m` or `--machine` ***(Print the Machine Hardware Name)***
> Prints the machine hardware name.


Examples:

`uname -a`

> Prints all system information, including kernel version and system architecture

`uname -r`

> Prints the kernel version

`uname -m`

> Prints the system architecture

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="hostname"></a> `hostname` *also known as* **Host Name**

Description:

> The `hostname` command in Linux is used to show or set the system's host name.

**Available Flags:**

`-a` or `--alias` ***(Display the Alias Name)***
> Displays the alias name of the host.

`-i` or `--ip-address` ***(Display the IP Address)***
> Displays the network address of the host.

`-s` or `--short` ***(Display the Short Hostname)***
> Displays the short hostname. This is the hostname up to the first `.`.

`-d` or `--domain` ***(Display the DNS Domain)***
> Displays the name of the DNS domain.

`-f` or `--fqdn` or `--long` ***(Display the FQDN Name)***
> Displays the fully qualified domain name (FQDN) for the host.


Examples:

`hostname`

> Shows the system's host name

`hostname newname`

> Sets the system's host name to 'newname' (requires root privileges)

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="date"></a> `date` *also known as* **Date**

Description:

> The `date` command in Linux is used to display or set the system's date and time.

**Available Flags:**

`-d` or `--date=STRING` ***(Display Time Described by STRING, Not `Now`)***
> Displays time described by STRING, instead of `now`.

`-u` or `--utc` or `--universal` ***(Print or Set Coordinated Universal Time)***
> Prints or sets Coordinated Universal Time (UTC).

`-R` or `--rfc-email` ***(Output Date and Time in RFC 5322 Format)***
> Outputs date and time in RFC 5322 format.

`-I[TIMESPEC]` or `--iso-8601[=TIMESPEC]` ***(Output Date or Time in ISO 8601 Format)***
> Outputs date or time in ISO 8601 format. TIMESPEC can be `date`, `hours`, `minutes`, `seconds`, or `ns` for date only, hours, minutes, seconds, or nanoseconds precision.

`-r` or `--reference=FILE` ***(Display the Last Modification Time of FILE)***
> Displays the last modification time of FILE.


Examples:

`date`

> Displays the current date and time

`date +%Y-%m-%d`

> Displays the current date in 'Year-Month-Day' format

`date -s "2023-07-22 12:34:56"`

> Sets the system's date and time to 'July 22, 2023 12:34:56' (requires root privileges)

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="uptime"></a> `uptime` *also known as* **Uptime**

Description:

> The `uptime` command in Linux gives a one-line display of the following information: The current time, how long the system has been running, how many users are currently logged on, and the system load averages for the past 1, 5, and 15 minutes.

**Available Flags:**

`-p` or `--pretty` ***(Show Uptime in Pretty Format)***
> Show uptime in pretty format, like `up 2 days, 4 hours, 42 minutes`.

`-h` or `--help` ***(Display Help Information)***
> Displays help information and exit.

`-s` or `--since` ***(System Up Since)***
> Shows the date and time the system has been up since.


Examples:

`uptime`

> Displays the current system uptime

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="free"></a> `free` *also known as* **Free**

Description:

> The `free` command in Linux is used to display the amount of free and used memory in the system.

**Available Flags:**

`-b` or `--bytes` ***(Display Amount of Memory in Bytes)***
> Display the amount of memory in bytes.

`-k` or `--kilo` ***(Display Amount of Memory in Kilobytes)***
> Display the amount of memory in kilobytes. This is the default.

`-m` or `--mega` ***(Display Amount of Memory in Megabytes)***
> Display the amount of memory in megabytes.

`-g` or `--giga` ***(Display Amount of Memory in Gigabytes)***
> Display the amount of memory in gigabytes.

`-t` or `--total` ***(Display a Line Containing the Totals)***
> Display a line containing the totals.


Examples:

`free -m`

> Displays the amount of free and used memory in megabytes

`free -g`

> Displays the amount of free and used memory in gigabytes

`free -h`

> Displays the amount of free and used memory in a human-readable format

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="fdisk"></a> `fdisk` *also known as* **Fixed Disk**

Description:

> The `fdisk` command in Linux is used to create, manage, and delete partition tables on hard disks.

**Available Flags:**

`-l` or `--list` ***(List the Partition Tables for the Specified Devices)***
> List the partition tables for the specified devices and then exit. If no devices are given, those mentioned in `/proc/partitions` (if that exists) are used.

`-s` or `--size` ***(Print the Size in Blocks of the Partition)***
> Print the size in blocks of the partition specified by the device and then exit.

`-b` or `--sector-size` ***(Specify the Sector Size of the Disk)***
> Specify the sector size of the disk. Valid values are 512, 1024, 2048, and 4096.

`-u` or `--units` ***(Change Display/Entry Units)***
> Change display/entry units. By default, sectors are used as units.


Examples:

`fdisk -l`

> Lists the partition tables for all disk drives

`fdisk /dev/sda`

> Starts an interactive menu for managing the partition table on the /dev/sda disk

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="lsusb"></a> `lsusb` *also known as* **List USB**

Description:

> The `lsusb` command in Linux is used to display information about USB buses in the system and the devices connected to them.

**Available Flags:**

`-v` or `--verbose` ***(Increase Verbosity)***
> Tells lsusb to be verbose and display detailed information about the devices shown. This includes configuration descriptors for the device's current speed. Class descriptors will be shown, when available, for USB device classes including hub, audio, HID, communications, and chipcard.

`-s` or `--bus` ***(Show Only Devices on this Bus)***
> Show only devices in specified bus and/or device number.

`-d` or `--device` ***(Show Only Devices with this Vendor and Product ID)***
> Show only devices with the specified vendor and product ID.

`-t` or `--tree` ***(Show Device Tree)***
> Tells lsusb to dump the physical USB device hierarchy as a tree.


Examples:

`lsusb`

> Lists all USB devices connected to the system

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="lsdev"></a> `lsdev` *also known as* **List Devices**

Description:

> The `lsdev` command in Linux is used to display information about installed hardware.

**Available Flags:**

`lsdev` does not have any flags.

Examples:

`lsdev`

> Lists all devices and their properties

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="iptables"></a> `iptables` *also known as* **IP Tables**

Description:

> The `iptables` command in Linux is used to set up, maintain, and inspect the tables of IP packet filter rules in the Linux kernel.

**Available Flags:**

`-A` or `--append` ***(Append to Chain)***
> Append to chain. Adds one or more rules to the end of the selected chain.

`-D` or `--delete` ***(Delete Matching Rule from Chain)***
> Delete one or more rules from the selected chain.

`-I` or `--insert` ***(Insert in Chain)***
> Insert one or more rules in the selected chain as the given rule number.

`-F` or `--flush` ***(Flush Chain)***
> Flush the selected chain (all the chains in the table if none is given). This is equivalent to deleting all the rules one by one.

`-L` or `--list` ***(List the Rules in a Chain or All Chains)***
> List all rules in the selected chain. If no chain is selected, all chains are listed.


Examples:

`iptables -L`

> Lists all current firewall rules

`iptables -F`

> Flushes all firewall rules

`iptables -A INPUT -p tcp --dport 80 -j ACCEPT`

> Appends a rule to the INPUT chain to accept TCP packets on port 80

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="ufw"></a> `ufw` *also known as* **Uncomplicated Firewall**

Description:

> The `ufw` command in Linux is used as a frontend for iptables for managing a Netfilter firewall. It provides a user-friendly way to create an IPv4 or IPv6 host-based firewall.

**Available Flags:**

`enable` ***(Enable UFW)***
> Enables the firewall, this has the same effect as running `ufw start`.

`disable` ***(Disable UFW)***
> Disables the firewall, this has the same effect as running `ufw stop`.

`default` ***(Set Default Policy)***
> Sets the default policy. This can either be `allow`, `deny`, `reject` or `limit`.

`allow` ***(Allow Traffic)***
> Allows traffic from a specified service or port.

`deny` ***(Deny Traffic)***
> Denies traffic from a specified service or port.

`status` ***(Show Firewall Status)***
> Shows the status of ufw, whether it's active and what rules are set.

Examples:

`ufw status`

> Shows the current status and rules of UFW

`ufw enable`

> Enables UFW

`ufw disable`

> Disables UFW

`ufw allow 22`

> Allows incoming traffic on port 22

`ufw deny 22`

> Denies incoming traffic on port 22

`ufw default deny incoming`

> Sets the default to deny all incoming connections

`ufw default allow outgoing`

> Sets the default to allow all outgoing connections

###### [ ← Back to table of contents ](#tableOfContents)
---

## <a name="remoteConnectivity"></a> Remote Connectivity

### <a name="ssh"></a> `ssh` *also known as* **Secure Shell**

Description:

> `ssh` (Secure Shell) is a cryptographic network protocol used to securely access and manage remote systems over an unsecured network. It provides encrypted communication between the client and the server.

**Available Flags:**

`<user>@<host>` ***(Connect to Remote Host)*** 
> `ssh <user>@<host>` establishes a secure shell connection to the specified remote host.

`-p` or `--port` ***(Specify Port Number)***
> `ssh -p <port> <user>@<host>` connects to the remote host on the specified port number.

`-i` or `--identity` ***(Select Identity File)***
> `ssh -i <private_key> <user>@<host>` uses the specified private key file for authentication.

Examples:

`ssh user@example.com`

> Connects to the remote host `example.com` using the default port 22.

`ssh -p 2222 user@example.com`

> Connects to the remote host `example.com` on port 2222.

`ssh -i ~/.ssh/private_key user@example.com`

> Connects to the remote host `example.com` using the specified private key file.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="sshuttle"></a> `sshuttle`

Description:

> `sshuttle` is a tool used to create a VPN-like connection over SSH. It allows you to route your internet traffic through an SSH tunnel, providing secure access to remote networks. This command requires installation and is available on most Linux Systems as well as Mac OS. [Install sshuttle](https://github.com/sshuttle/sshuttle#obtaining-sshuttle)

**Available Flags:**

`<server>` ***(Create VPN-Like Connection)***
> `sshuttle -r <user>@<server> <subnet>` creates a VPN-like connection through SSH to the specified server and subnet.

`-D` or `--dns` ***(Use Remote DNS)***
> `sshuttle -r <user>@<server> <subnet> -D` routes DNS queries through the remote DNS server.

`--exclude` ***(Exclude Subnet from VPN)***
> `sshuttle --exclude <subnet>` excludes the specified subnet from the VPN.

Examples:

`sshuttle -r user@example.com 0/0`

> Routes all internet traffic through the VPN-like connection to `example.com`.

`sshuttle -r user@example.com 10.0.0.0/24`

> Routes only traffic for the subnet `10.0.0.0/24` through the VPN-like connection to `example.com`.

`sshuttle -r user@example.com 0/0 -D`

> Routes all internet traffic and DNS queries through the VPN-like connection to `example.com`.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="scp"></a> `scp` *also known as* **Secure Copy**

Description:

> `scp` (Secure Copy) is a command-line tool used to securely transfer files between local and remote hosts. It uses SSH for data transfer and provides encryption and authentication.

**Available Flags:**

`<source>` ***(Source File or Directory)***
> `scp <source> <user>@<host>:<destination>` copies the specified file or directory from the local machine to the remote host.

`<user>@<host>:<source>` ***(Source File or Directory on Remote Host)***
> `scp <user>@<host>:<source> <destination>` copies the specified file or directory from the remote host to the local machine.

Examples:

`scp file.txt user@example.com:/home/user/`

> Copies `file.txt` from the local machine to the remote host `example.com` in the user's home directory.

`scp user@example.com:/var/log/access.log .`

> Copies `access.log` from the remote host `example.com` to the current directory on the local machine.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="sftp"></a> `sftp` *also known as* **Secure File Transfer Protocol**

Description:

> `sftp` (Secure File Transfer Protocol) is an interactive command-line tool used for secure file transfer between local and remote hosts. It operates over an encrypted SSH session.

**Available Flags:**

`<user>@<host>` ***(Connect to Remote Host)***
> `sftp <user>@<host>` establishes an SFTP connection to the specified remote host.

Examples:

`sftp user@example.com`

> Connects to the remote host `example.com` via SFTP.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="rsync"></a> `rsync`

Description:

> `rsync` is a powerful and versatile command-line utility used for synchronizing files and directories between local and remote systems. It efficiently transfers only the differences between source and destination files.

**Available Flags:**

`<source>` ***(Source File or Directory)***
> `rsync <source> <user>@<host>:<destination>` copies the specified file or directory from the local machine to the remote host.

`<user>@<host>:<source>` ***(Source File or Directory on Remote Host)***
> `rsync <user>@<host>:<source> <destination>` copies the specified file or directory from the remote host to the local machine.

`-a` or `--archive` ***(Archive Mode)***
> `rsync -a <source> <destination>` enables archive mode, preserving permissions, ownership, and timestamps.

`-v` or `--verbose` ***(Verbose Output)***
> `rsync -v <source> <destination>` provides verbose output, showing detailed progress during the transfer.

`-z` or `--compress` ***(Compress Files During Transfer)***
> `rsync -z <source> <destination>` compresses files during the transfer to reduce bandwidth usage.

Examples:

`rsync -avz /path/to/local/file.txt user@example.com:/path/to/remote/`

> Synchronizes `file.txt` from the local machine to the remote host `example.com`.

`rsync -avz user@example.com:/path/to/remote/file.txt /path/to/local/`

> Synchronizes `file.txt` from the remote host `example.com` to the local machine.

###### [ ← Back to table of contents ](#tableOfContents)
---

## <a name="networkingCommands"></a> Networking

### <a name="ping"></a> `ping`

Description:

> `ping` is a command-line utility used to test the reachability of a host on an Internet Protocol (IP) network. It sends ICMP echo request packets to the target host and waits for ICMP echo reply packets.

**Available Flags:**

`<host>` ***(Target Host)***
> `ping <host>` sends ICMP echo requests to the specified host.

Examples:

`ping example.com`

> Pings the host `example.com` to check its reachability.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="ifconfig"></a> `ifconfig` *also known as* **Interface Configuration**

Description:

> `ifconfig` is a command-line tool used to configure network interfaces on Unix-like operating systems. It provides information about the current network configuration of the system.

**Available Flags:**

`-a` or `--all` ***(Display All Interfaces)***
> `ifconfig -a` displays information about all network interfaces, including those that are down.

`<interface>` ***(Display Specific Interface)***
> `ifconfig <interface>` displays information about the specified network interface.

Examples:

`ifconfig`

> Displays information about all active network interfaces.

`ifconfig -a`

> Displays information about all network interfaces, including those that are down.

`ifconfig eth0`

> Displays information about the `eth0` network interface.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="netstat"></a> `netstat` *also known as* **Network Statistics**

Description:

> `netstat` is a command-line tool used to display various network-related information, such as active network connections, routing tables, and network interface statistics.

**Available Flags:**

`-t` or `--tcp` ***(Show TCP Connections)***
> `netstat -t` displays all TCP connections.

`-u` or `--udp` ***(Show UDP Connections)***
> `netstat -u` displays all UDP connections.

`-r` or `--route` ***(Show Routing Table)***
> `netstat -r` displays the kernel routing table.

`-i` or `--interfaces` ***(Show Interface Statistics)***
> `netstat -i` displays a table of network interfaces and their statistics.

Examples:

`netstat`

> Displays all active network connections.

`netstat -t`

> Displays all TCP connections.

`netstat -u`

> Displays all UDP connections.

`netstat -r`

> Displays the kernel routing table.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="wget"></a> `wget`

Description:

> `wget` is a command-line utility used to download files from the web. It supports downloading via HTTP, HTTPS, and FTP protocols.

**Available Flags:**

`<URL>` ***(Download File)***
> `wget <URL>` downloads the file from the specified URL.

`-O` or `--output-document` ***(Save to Specific File)***
> `wget -O <filename> <URL>` downloads the file from the specified URL and saves it with the given filename.

Examples:

`wget https://example.com/file.txt`

> Downloads the `file.txt` from `example.com`.

`wget -O myfile.txt https://example.com/file.txt`

> Downloads the `file.txt` from `example.com` and saves it as `myfile.txt`.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="curl"></a> `curl`

Description:

> `curl` is a command-line tool used to transfer data to or from a server using various protocols, including HTTP, HTTPS, FTP, and more.

**Available Flags:**

`<URL>` ***(Download File or Perform HTTP Request)***
> `curl <URL>` downloads the file or performs an HTTP request to the specified URL.

`-o` or `--output` ***(Save to Specific File)***
> `curl -o <filename> <URL>` downloads the file from the specified URL and saves it with the given filename.

`-I` or `--head` ***(Show Headers Only)***
> `curl -I <URL>` fetches and displays the headers only, not the whole document.

Examples:

`curl https://example.com/file.txt`

> Downloads the `file.txt` from `example.com`.

`curl -o myfile.txt https://example.com/file.txt`

> Downloads the `file.txt` from `example.com` and saves it as `myfile.txt`.

`curl -I https://example.com`

> Fetches and displays the headers of the `example.com` website.

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="nc"></a> `nc` *also known as* **Netcat**

Description:

> `nc` (Netcat) is a versatile networking utility often referred to as the "Swiss Army knife" for TCP/IP. It can be used for port scanning, transferring data, creating listening sockets, and more.

**Available Flags:**

`-l` or `--listen` ***(Listen Mode)***
> `nc -l <port>` creates a listening socket and waits for incoming connections on the specified port.

`-p` or `--port` ***(Specify Port)***
> `nc -l -p <port>` specifies the port number to listen on.

`-v` or `--verbose` ***(Verbose Output)***
> `nc -v <host> <port>` enables verbose output, providing more details about the connection.

Examples:

`nc -l 1234`

> Creates a listening socket on port 1234.

`nc -l -p 2222`

> Creates a listening socket on port 2222.

`nc -v example.com 80`

> Connects to `example.com` on port 80 with verbose output.

###### [ ← Back to table of contents ](#tableOfContents)
---


### <a name="nmap"></a> `nmap` *also known as* **Network Mapper**

Description:

> `nmap` (Network Mapper) is a powerful and flexible open-source network scanning tool used for network exploration and security auditing. It discovers hosts and services on a computer network, thus creating a "map" of the network.

**Available Flags:**

`<target>` ***(Specify Target Host or IP Range)***
> `nmap <target>` scans the target host or IP range to discover active hosts and open ports.

`-p` or `--port` ***(Specify Port(s) to Scan)***
> `nmap -p <port(s)> <target>` specifies the port(s) to scan for each target.

`-sS` or `--syn` ***(TCP SYN Scan)***
> `nmap -sS <target>` performs a TCP SYN scan, the most common and stealthy scan type.

`-sU` or `--udp` ***(UDP Scan)***
> `nmap -sU <target>` performs a UDP scan to identify open UDP ports.

`-O` or `--osscan` ***(OS Detection)***
> `nmap -O <target>` tries to identify the operating system of the target hosts.

Examples:

`nmap example.com`

> Scans the `example.com` host for open ports using the default scan.

`nmap -p 80,443 example.com`

> Scans the `example.com` host for open ports 80 and 443.

`nmap -sS example.com`

> Performs a TCP SYN scan on the `example.com` host.

`nmap -sU example.com`

> Performs a UDP scan on the `example.com` host.

`nmap -O example.com`

> Tries to identify the operating system of the `example.com` host.

###### [ ← Back to table of contents ](#tableOfContents)
---


### <a name="ip"></a> `ip` *also known as* **ip Command**

Description:

> The `ip` command is used to manage network interfaces and routing tables in Linux. It provides a more extensive set of features than the traditional `ifconfig` command.

**Available Flags:**

`link` ***(Manage Network Interfaces)***
> `ip link` displays and manages network interfaces.

`addr` ***(Manage IP Addresses)***
> `ip addr` displays and manages IP addresses associated with network interfaces.

`route` ***(Manage Routing Table)***
> `ip route` displays and manages the kernel routing table.

Examples:

`ip link`

> Displays information about all network interfaces.

`ip addr show eth0`

> Shows IP addresses assigned to the `eth0` interface.

`ip route show`

> Shows the kernel routing table.

###### [ ← Back to table of contents ](#tableOfContents)
---


### <a name="dig"></a> `dig` *also known as* **Domain Information Groper**

Description:

> `dig` (Domain Information Groper) is a command-line tool used to query DNS servers and retrieve DNS information for a domain name.

**Available Flags:**

`<domain>` ***(Domain Name)***
> `dig <domain>` queries DNS servers to retrieve DNS information for the specified domain name.

`-t` or `--type` ***(Query Type)***
> `dig -t <query_type> <domain>` specifies the query type, such as A, AAAA, MX, CNAME, etc.

Examples:

`dig example.com`

> Queries DNS servers for information about `example.com`.

`dig -t MX example.com`

> Queries DNS servers for Mail Exchange (MX) records of `example.com`.

###### [ ← Back to table of contents ](#tableOfContents)
---


### <a name="arp"></a> `arp` *also known as* **Address Resolution Protocol**

Description:

> `arp` (Address Resolution Protocol) is a command-line tool used to display and manage the ARP cache, which translates IP addresses to MAC addresses on a local network.

**Available Flags:**

`-a` or `--all` ***(Display All Entries)***
> `arp -a` displays all entries in the ARP cache.

Examples:

`arp -a`

> Displays all entries in the ARP cache.

###### [ ← Back to table of contents ](#tableOfContents)
---


## <a name="webServices"></a> Web Hosting and Services

---
## <a name="sslCertManagement"></a> SSL Certificate Management

### <a name="certbot"></a> `certbot` *also known as* **Let's Encrypt Certificate Bot**

Description:

> `certbot` is a command-line tool provided by EFF (Electronic Frontier Foundation) to automatically obtain and install SSL/TLS certificates from Let's Encrypt Certificate Authority. It makes HTTPS adoption easier by automating both the certificate issuance and renewal processes.

**Available Flags:**

`certonly` ***(Only Obtain a Certificate)***
> `certbot certonly` is used when you want to obtain a certificate but not install it. Typically combined with `--webroot`, `--standalone`, `--nginx` or other plugins.

`renew` ***(Renew Certificates)***
> `certbot renew` will renew all of the certificates that certbot manages which are near expiry.

`run` ***(Obtain and Install a Certificate)***
> `certbot run` obtains a certificate and installs it, potentially replacing an existing certificate with the same name.

`delete` ***(Delete a Certificate)***
> `certbot delete` will delete a specified certificate that is no longer in use.

`revoke` ***(Revoke a Certificate)***
> `certbot revoke` is used to revoke a specific certificate by its certificate path.

Examples:

`sudo certbot certonly --webroot -w /var/www/html -d example.com`

> Obtains a certificate for `example.com` using the webroot plugin.

`sudo certbot certonly --nginx -d example.com -d www.example.com`

> Obtains a certificate for `example.com` using the webroot plugin.

`sudo certbot renew`

> Renews all near-expiry certificates managed by certbot.

`sudo certbot run --standalone -d example.com`

> Obtains and installs a certificate for `example.com` using the standalone plugin.

`sudo certbot delete --cert-name example.com`

> Deletes the certificate for `example.com`.

`sudo certbot revoke --cert-path /etc/letsencrypt/live/example.com/cert.pem`

> Revokes the certificate for `example.com` using its certificate path.

###### [ ← Back to table of contents ](#tableOfContents)
---


### <a name="nginx"></a> `nginx` *also known as* **Nginx Web Server**

Description:

> `nginx` is a high-performance HTTP and reverse proxy server, a mail proxy server, and a generic TCP/UDP proxy server. It's known for its high performance, stability, feature set, simple configuration, and low resource consumption.

**Available Flags:**

`-s` ***(Signal to a Master Process)***
> `nginx -s` allows you to send signals to the master process: stop, quit, reopen, reload.

Examples:

`nginx -s stop`
> Stops the `nginx` master process immediately.

`nginx -s quit`
> Gracefully shuts down the `nginx` master process.

`nginx -s reopen`
> Reopens the log files.

`nginx -s reload`
> Reloads the configuration file.

`-t` or `--test` ***(Test Configuration File)***
> `nginx -t` checks the syntax of the configuration file and tests it.

Examples:

`nginx -t`
> Checks the syntax of the configuration file and tests it.

`-v` ***(Show Version)***
> `nginx -v` displays the nginx version.

Examples:

`nginx -v`
> Displays the nginx version.

`-V` ***(Show Version and Configure Options)***
> `nginx -V` displays the nginx version, compiler version, and configure parameters.

Examples:

`nginx -V`
> Displays the nginx version, compiler version, and configure parameters.

###### [ ← Back to table of contents ](#tableOfContents)
---


---

### <a name="http_redirect_https"></a> `http_redirect_http` *also known as* **Config for All Traffic to Server Redirecting from HTTP to HTTPS**

Description:

> The configuration below is used to redirect all HTTP traffic coming to the server to its HTTPS counterpart. This is essential for ensuring encrypted and secure communication.

**Configuration:**

```
server {
    listen 80 default_server;

    server_name _;

    return 301 https://$host$request_uri;
}
```

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="vue_service"></a> `Serve a Single View Application` *also known as* **Serving a Single Page Web Application**

Description:

> This configuration is ideal for serving a Vue 2/3 production website. Additionally, it includes proxy passes for specific routes, ensuring seamless routing for essential paths like sitemap and robots.txt.

**Use Cases:**

> Serving a Vue 2/3 Production Website.

**Configuration:**

```
server {
        root /data/EXAMPLE.COM/front-dist/;

        index index.html index.htm index.nginx-debian.html;

        server_name EXAMPLE.COM WWW.EXAMPLE.COM;

        gzip_static on;

        location / {
          try_files $uri $uri/ /index.html;
          etag off;
        }

        # THIS IS A PROXY PASS FOR /sitemap.xml
        location /sitemap.xml {
          proxy_pass http://localhost:8080/sitemap.xml;
          proxy_set_header Host $host;
        }

        # THIS IS A PROXY PASS FOR /robots.txt
        location /robots.txt {
          proxy_pass http://localhost:8080/robots.txt;
          proxy_set_header Host $host;
        }

    listen [::]:443 ssl; # managed by Certbot
    listen 443 ssl; # managed by Certbot
    ssl_certificate /etc/letsencrypt/live/EXAMPLE.COM/fullchain.pem; # managed by Certbot
    ssl_certificate_key /etc/letsencrypt/live/EXAMPLE.COM/privkey.pem; # managed by Certbot
    include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot
}
```


###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="nginx_proxy_service"></a> `Proxy Service` *also known as* **Proxying a Webservice through NGINX**

Description:

> The configuration below enables you to route traffic through an NGINX proxy. This is useful for serving web services that don't support SSL (HTTPS) directly, for running web frameworks like Nuxt 3 through a proxy, or for accessing sites on local networks without direct port forwarding.

**Use Cases:**

> - Serving a web service that is not supported for SSL (HTTPS).
> - Running a Nuxt 3 Web app through a proxy.
> - Accessing a site on a local network that can't be port forwarded directly.

**Configuration:**

```
server {
    server_name API.EXAMPLE.COM;
	
    location / {
       proxy_pass http://localhost:8080;
    }

    listen [::]:443 ssl; # managed by Certbot
    listen 443 ssl; # managed by Certbot
    ssl_certificate /etc/letsencrypt/live/API.EXAMPLE.COM/fullchain.pem; # managed by Certbot
    ssl_certificate_key /etc/letsencrypt/live/API.EXAMPLE.COM/privkey.pem; # managed by Certbot
    include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot
}
```


###### [ ← Back to table of contents ](#tableOfContents)

---
## <a name="packageManagement"></a> Package Management

### <a name="apt-get"></a> `apt-get` *also known as* **APT Package Handling Utility**

Description:

> `apt-get` is the command-line tool for handling packages in Debian-based Linux distributions. It provides a way to install, upgrade, or remove software packages on a system.

**Available Flags:**

`update` ***(Retrieve New Lists of Packages)***
> `apt-get update` downloads the package lists from the repositories and "updates" them to get information on the newest versions of packages and their dependencies.

`upgrade` ***(Perform an Upgrade)***
> `apt-get upgrade` will fetch new versions of packages existing on the machine if APT knows about these new versions by way of `apt-get update`.

`install` ***(Install New Packages)***
> `apt-get install` is followed by one or more packages desired for installation or upgrading.

`remove` ***(Remove Packages)***
> `apt-get remove` is used to remove an installed package, leaving configuration files intact.

`autoremove` ***(Remove Unused Packages)***
> `apt-get autoremove` is used to remove packages that were automatically installed to satisfy dependencies for other packages and are now no longer needed.

`dist-upgrade` ***(Distribution Upgrade)***
> `apt-get dist-upgrade` in addition to performing the function of upgrade, this option also intelligently handles changing dependencies with new versions of packages.

`purge` ***(Remove Packages and Configuration Files)***
> `apt-get purge` is identical to remove except that packages are removed and purged. Any configuration files are also deleted.

Examples:

`sudo apt-get update`

> Updates package lists

`sudo apt-get upgrade`

> Upgrades all upgradable packages

`sudo apt-get install git`

> Installs git

`sudo apt-get remove git`

> Removes git

`sudo apt-get autoremove`

> Removes all unused packages

`sudo apt-get dist-upgrade`

> Upgrades packages and intelligently handles changing dependencies

`sudo apt-get purge git`

> Removes git and its configuration files

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="yum"></a> `yum` *also known as* **Yellowdog Updater Modified**

Description:

> `yum` is the default package manager for Red Hat based distributions such as CentOS, Fedora or RHEL. It is used to install, uninstall, update, list available packages, update all or a specific package, etc.

**Available Flags:**

`install` ***(Install a Package)***
> `yum install` is used to install the latest version of a package or group of packages while ensuring that all dependencies are resolved.

`update` ***(Update a Package)***
> `yum update` is used to update all the installed packages to the latest available versions.

`remove` ***(Remove a Package)***
> `yum remove` is used to remove any specified packages from the system along with any packages dependent on the package being removed.

`list` ***(List a Package)***
> `yum list` is used to list various information about available packages; it can list all available and installed packages in the system.

`check-update` ***(Check for Updates)***
> `yum check-update` checks the server for any updates that are applicable to your system.

`info` ***(Provide Information about a Package)***
> `yum info` is used to display detailed information about a package.

`clean` ***(Clean Yum Cache)***
> `yum clean` is used to clean up various things which accumulate in the yum cache over time.

Examples:

`sudo yum install git`

> Installs the git package

`sudo yum update`

> Updates all packages

`sudo yum remove git`

> Removes the git package

`yum list installed`

> Lists all installed packages

`sudo yum check-update`

> Checks for package updates

`yum info git`

> Provides information about the git package

`sudo yum clean all`

> Cleans up the yum cache

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="pacman"></a> `pacman` *also known as* **Package Manager**

Description:

> `pacman` is the package manager for Arch-based distributions. It is used to install, remove, and update packages. `pacman` also tracks the dependencies of each package to ensure that all software is working as expected.

**Available Flags:**

`-S` ***(Synchronize Packages)***
> `pacman -S` is used to install a package.

`-Sy` ***(Refresh Package Lists)***
> `pacman -Sy` refreshes the package lists from the repositories.

`-Su` ***(Upgrade All Packages)***
> `pacman -Su` upgrades all packages that are out-of-date.

`-R` ***(Remove Packages)***
> `pacman -R` is used to remove a package.

`-Rs` ***(Remove Unused Packages)***
> `pacman -Rs` removes a package and its unused dependencies.

`-Ss` ***(Search Package Database)***
> `pacman -Ss` is used to search the package database.

`-Q` ***(Query the Package Database)***
> `pacman -Q` queries the local package database.

Examples:

`sudo pacman -Sy`

> Updates the package list

`sudo pacman -S firefox`

> Installs the firefox package

`sudo pacman -Su`

> Upgrades all packages

`sudo pacman -R firefox`

> Removes the firefox package

`sudo pacman -Rs firefox`

> Removes the firefox package and its unused dependencies

`pacman -Ss firefox`

> Searches the package database for the firefox package

`pacman -Q firefox`

> Queries the local package database for the firefox package

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="pip"></a> `pip` *also known as* **Package Installer for Python**

Description:

> `pip` is the package installer for Python. It provides a way to install, upgrade, or remove Python libraries and tools from the Python Package Index (PyPI) and other repositories.

**Available Flags:**

`install` ***(Install Packages)***
> `pip install` is used to install one or more Python packages.

`uninstall` ***(Uninstall Packages)***
> `pip uninstall` is used to remove one or more installed Python packages.

`list` ***(List Installed Packages)***
> `pip list` displays a list of all installed Python packages.

`freeze` ***(Output Installed Packages in Requirements Format)***
> `pip freeze` outputs the versions of all installed packages, making it easy to reproduce an environment.

`download` ***(Download Packages)***
> `pip download` is used to download Python packages without installing them.

`search` ***(Search for Packages on PyPI)***
> `pip search` is used to search for Python packages available on PyPI.

`upgrade` ***(Upgrade Packages)***
> `pip install --upgrade` is used to upgrade one or more installed Python packages to the latest version.

Examples:

`pip install requests`

> Installs the requests package

`pip uninstall requests`

> Uninstalls the requests package

`pip list`

> Lists all installed Python packages

`pip freeze > requirements.txt`

> Saves the list of all installed packages with their versions to `requirements.txt`

`pip download requests`

> Downloads the requests package without installing it

`pip search "web framework"`

> Searches PyPI for Python packages related to "web framework"

`pip install --upgrade requests`

> Upgrades the requests package to the latest version

###### [ ← Back to table of contents ](#tableOfContents)
---


### <a name="brew"></a> `brew` *also known as* **Homebrew**

Description:

> `brew` (Homebrew) is a package manager for macOS that allows you to easily install, update, and manage various software packages, libraries, and tools. This command requires an installation from [ Homebrew ](https://brew.sh)

**Available Flags:**

`install` ***(Install a Package or Formula)***
> `brew install` is used to install a package or formula from the Homebrew repository.

`uninstall` ***(Uninstall a Package or Formula)***
> `brew uninstall` is used to uninstall a previously installed package or formula.

`search` ***(Search for Packages)***
> `brew search` allows you to search for packages available in the Homebrew repository.

`update` ***(Update Homebrew and Upgrade Packages)***
> `brew update` updates the Homebrew itself and `brew upgrade` upgrades the installed packages.

`list` ***(List Installed Packages or Formulas)***
> `brew list` shows a list of all installed packages or formulas.

`info` ***(Display Information About a Package or Formula)***
> `brew info` displays detailed information about a package or formula.

Examples:

`brew install wget`

> Installs the wget package

`brew uninstall wget`

> Uninstalls the wget package

`brew search python`

> Searches for packages related to Python

`brew update`

> Updates Homebrew itself

`brew upgrade`

> Upgrades all installed packages

`brew list`

> Lists all installed packages

`brew info wget`

> Displays information about the wget package

###### [ ← Back to table of contents ](#tableOfContents)
---


## <a name="otherCommands"></a> Other Commands

### <a name="man"></a> `man` *also known as* **Manual Pages**

Description:

> `man` is used to display the manual pages (documentation) for various commands in Linux. It provides detailed information, usage instructions, and options for each command.

**Available Flags:**

`<command>` ***(Show Manual for the Specified Command)***
> `man <command>` displays the manual page for the specified command.

Examples:

`man ls`

> Displays the manual page for the `ls` command

`man grep`

> Displays the manual page for the `grep` command

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="history"></a> `history`

Description:

> `history` is a command that shows a list of previously executed commands in the current shell session. It provides a history of all the commands you have executed.

**Available Flags:**

`history` does not have any flags.

Examples:

`history`

> Displays the command history of the current shell session

###### [ ← Back to table of contents ](#tableOfContents)
---

### <a name="alias"></a> `alias`

Description:

> `alias` is used to create, list, or remove command aliases in Linux. Aliases are shortcuts or alternate names for commands or command combinations.

**Available Flags:**

`<alias-name>` ***(Define an Alias for a Command)***
> `alias <alias-name>` defines a new alias for the specified command.

`-p` or `--p` ***(List Aliases)***
> `alias -p` lists all defined aliases.

`unalias` ***(Remove an Alias)***
> `unalias` removes the specified alias.

Examples:

`alias ll='ls -l'`

> Creates an alias 'll' for the `ls -l` command

`alias c=clear`

> Creates an alias 'c' for the `clear` command

`alias -p`

> Lists all defined aliases

`unalias ll`

> Removes the alias 'll'

###### [ ← Back to table of contents ](#tableOfContents)
---

## <a name="symbols"></a> Symbols

### <a name="tilde"></a> ` ~ ` | Tilde | Users Home Directory

The tilde symbol (~) represents the user's home directory in Linux. For example, if the current user is "john," typing `cd ~` will take them to the "/home/john" directory.

Examples:

`cd ~`

> Takes you to your home directory

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="pipe"></a> ` | ` | Vertical Line | Pipe

The vertical line (|) is known as the "pipe" symbol in Linux. It is used to connect the output of one command as the input to another. For example, `command1 | command2` will send the output of `command1` as the input to `command2`.

Example:

`ps aux | grep "chrome"`

> Here, [ pas aux ](#ps) lists all processes running on the system, and then the output is passed through the pipe "` | `" to [ grep ](#grep) "chrome", which filters and displays only the lines containing the word "chrome" (typically indicating Chrome browser processes).

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="asterisk"></a> ` * ` | Asterisk | Wildcard

The asterisk (*) is a wildcard symbol in Linux that represents zero or more characters in a file or directory name. For example, `file*.txt` will match all files starting with "file" and ending with ".txt."

Example:

`ls documents/*.txt`

> In this command, [ ls ](#ls) is used to list the files in the documents directory, and the pattern `*.txt` is passed as an argument. The asterisk (`*`) will match any file name in the documents directory that ends with ` ".txt" `, and the result will be a list of all the text files in the directory.

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="questionMark"></a>  ` ? ` | Question Mark | Wildcard

The question mark (?) is another wildcard symbol in Linux, representing a single character in a file or directory name. For example, `file?.txt` will match "file1.txt" and "fileA.txt" but not "file12.txt."

Example:

`ls logs/log?.txt`

> In this command, [ ls ](#ls) is used to list the files in the logs directory, and the pattern `log?.txt` is passed as an argument. The question mark (`?`) will match any single character in that position of the filename. So, this command will list all the files in the logs directory with names like `"log1.txt"`, `"log2.txt"`, `"log3.txt"` and so on.

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="exclamationMark"></a>  ` ! ` | Exclamation Mark | Bang

The exclamation mark (!) is commonly referred to as "bang" in Linux. It is often used in combination with other commands, like in history substitution. For example, `!n` will execute the nth command from the command history.

Example:

Suppose you run the command `ls -la`, You can then run:

`!!`

> This will then rerun the [ ls ](#ls) command because it was the last command ran.  

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="dollarSign"></a>  ` $ ` | Dollar Sign | Variable

The dollar sign ($) is used to represent a variable in Linux. Variables store data that can be accessed and manipulated by scripts and commands. For example, `$HOME` represents the user's home directory.

Examples:

`echo $HOME`

> This will display the path to the user's home directory, such as "/home/john" for user "john." 

`echo $PATH`

> This will display a list of locations (directories) where the computer looks for programs and commands when you type something in the terminal.

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="quotation"></a>  ` ' ` | Quotation | Text Literal

The single quotation mark (') is used to create a text literal in Linux. Anything within single quotes is treated as a literal string, and variables or special characters inside it are not expanded. For example, `'Hello $USER'` will be displayed as it is, without expanding the `$USER` variable.

Examples:

`echo '$HOME'`

> This will ***NOT*** display the path to the user's home directory, such as "/home/john" for user "john." but will literally display the characters $HOME. Checkout [  $  | Variable ](#dollarSign) for an example of printing out the users home directory or [  "  | Double Quotation ](#doubleQuotation) for an example of printing out the users home directory concatenated in a string.


###### [ ← Back to table of contents ](#tableOfContents)


### <a name="doubleQuotation"></a>  ` " ` | Double Quotation | Text Literal with Expansions

The double quotation mark (") is used to create a text literal with expansions in Linux. Variables and certain escape sequences inside double quotes are expanded. For example, `"Hello $USER"` will display "Hello" followed by the actual username.

Example:

Suppose your username is `john` and you're home directory is at `/home/john`

`echo "Hello my name is $USER and my home directory is at $HOME"`

>  Double Quotes is essential in this case to allow the shell to substitute the values of the variables into the string before printing it, resulting in an output like `Hello my name is john and my home directory is at /home/john`. Checkout [  $  | Variable ](#dollarSign) for an example of Variables.


###### [ ← Back to table of contents ](#tableOfContents)


### <a name="dot"></a>  ` . ` | Dot | Current Directory

The dot (.) represents the current directory in Linux. It is used to refer to the current working directory in commands and scripts.

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="doubleDot"></a>  ` .. ` | Double Dot | Parent Directory

The double dot (..) represents the parent directory of the current directory in Linux. It is used to move up one level in the directory structure.

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="doubleDotSlash"></a>  ` ../ ` | Double Dot Slash | Relative Path

The combination of double dot and a forward slash (../) is used to indicate a relative path in Linux. It allows you to specify a file or directory in the parent directory.

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="forwardSlash"></a>  ` / ` | Forward Slash | Directory Separation

The forward slash (/) is used as a directory separator in Linux. It is used to separate directory names in the path of a file or directory.

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="greaterThan"></a>  ` > ` | Greater Than | Output Direction

The greater-than symbol (>) is used for output redirection in Linux. It allows you to redirect the standard output of a command to a file instead of displaying it on the screen. For example, `ls > filelist.txt` will save the output of the `ls` command in the file "filelist.txt."

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="lessThan"></a>  ` < ` | Less Than | Input Direction

The less-than symbol (<) is used for input redirection in Linux. It allows you to feed a file as input to a command. For example, `sort < input.txt` will sort the contents of "input.txt."

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="doubleGreaterThan"></a>  ` >> ` | Double Greater Than | Append Output

The double greater-than symbol (>>) is used for appending output to a file in Linux. It works similarly to the single greater-than symbol, but it appends the output to the file instead of overwriting it.

###### [ ← Back to table of contents ](#tableOfContents)


### <a name="backslash"></a>  ` \ ` | Backslash | Escape Character

The backslash (\) is the escape character in Linux. It is used to treat special characters literally or to escape characters that have special meanings in Linux. For example, `\$` will be displayed as "$" instead of being interpreted as a variable.

###### [ ← Back to table of contents ](#tableOfContents)

