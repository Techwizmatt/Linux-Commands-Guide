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

---

### <a name="nano"></a> `nano` *also known as* **Nano's ANOther editor**

Description:

> The `nano` command is used to open the Nano text editor in a Linux terminal. This editor is a simple, user-friendly, and lightweight text editor used for creating and editing files. It offers basic features like syntax coloring, search and replace, indentation, and tab completion.

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

---

### <a name="touch"></a> `touch` *also known as* **Change File Timestamps**

Description:

> The `touch` command in Linux is used to create new, empty files. It can also be used to update the timestamps on existing files and directories, without modifying their content. This command is helpful when you need to quickly create a file or update the access or modification times.

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

---

### <a name="cat"></a> `cat` *also known as* **Concatenate**

Description:

> The `cat` command in Linux is used for creating, viewing, and concatenating files. `cat` stands for "concatenate", which means to combine. This command is most often used to display the contents of one or more files in the terminal.

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

---

### <a name="more"></a> `more` *also known as* **Pager**

Description:

> The `more` command in Linux is used to view the contents of a file in a terminal one screen at a time. The `more` command pauses after displaying a screenful of text and provides a prompt at the bottom of the screen. It is helpful when you want to read the contents of a large file without scrolling.

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

---

### <a name="tail"></a> `tail` *also known as* **Output the Last Part of Files**

Description:

> The `tail` command in Linux is used to display the end of a file. By default, it prints the last 10 lines of the specified files. If more than one file is specified, it precedes each set of output with a header giving the file name. The `tail` command is particularly useful for viewing the newest entries in log files.

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

---

### <a name="ln"></a> `ln` *also known as* **Link**

Description:

> The `ln` command in Linux is used to create links between files and directories. There are two types of links that can be created: hard links and symbolic, or soft, links. Hard links are pointers to the file data itself, whereas symbolic links are pointers to other file paths.

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

---

### <a name="find"></a> `find` *also known as* **Find Files and Directories**

Description:

> The `find` command in Linux is a very powerful tool used to search and locate files and directories based on different criteria such as file name, file type, size, and more. It traverses the file system hierarchy from the file paths specified in the command line.

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

---

### <a name="grep"></a> `grep` *also known as* **Global Regular Expression Print**

Description:

> The `grep` command in Linux stands for "global regular expression print". It's used to search text for lines that match a certain pattern. `grep` is highly versatile and can be used with regular expressions for complex pattern matching.

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

---

### <a name="wc"></a> `wc` *also known as* **Word, Line, Character, and Byte Count**

Description:

> The `wc` command in Linux is used to find out the number of lines, words, characters, and bytes in a file. `wc` stands for "word count", but it can count more than just words. It can be a handy tool when you need to know the size or length of a file.

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

---

### <a name="chmod"></a> `chmod` *also known as* **Change Mode**

Description:

> The `chmod` command in Linux is used to change the access permissions of files and directories. It allows you to define who can read, write, and execute a file or directory. Permissions can be set using symbolic modes (using letters) or octal modes (using numbers).

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

---

### <a name="chown"></a> `chown` *also known as* **Change Owner**

Description:

> The `chown` command in Linux is used to change the owner and group of a file or directory. It allows you to specify who the new owner and group should be. This command is generally used by administrators to change the ownership of files/directories.

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

---

### <a name="chgrp"></a> `chgrp` *also known as* **Change Group**

Description:

> The `chgrp` command in Linux is used to change the group ownership of a file or directory. It allows you to specify the new group. This command is often used when a file needs to be accessed by different users, all of whom are members of the same group.

Examples:

`chgrp newgroup filename`

> Changes the group of 'filename' to 'newgroup'

`chgrp -R newgroup directory`

> Changes the group of 'directory' and its contents to 'newgroup' recursively

`chgrp --reference=ref_file target_file`

> Changes the group of 'target_file' to be the same as that of 'ref_file'

`chgrp newgroup file1 file2 file3`

> Changes the group of 'file1', 'file2', and 'file3' to 'newgroup'

---

### <a name="df"></a> `df` *also known as* **Disk Free**

Description:

> The `df` command in Linux is used to display the amount of disk space used and available on the file system. By default, the space is shown in 1K blocks, but this can be adjusted to a more human-readable format.

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

---

### <a name="du"></a> `du` *also known as* **Disk Usage**

Description:

> The `du` command in Linux is used to estimate the space usage of files and directories. This command can be used to track down files and directories that are using large amounts of disk space.

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

---

### <a name="mount"></a> `mount` *also known as* **Mount File Systems**

Description:

> The `mount` command in Linux is used to mount file systems. The command attaches a file system (which could be a device, partition, or network share) to a certain point in the directory tree. This is crucial when you want to access the content of the device or partition.

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

---

### <a name="umount"></a> `umount` *also known as* **Unmount File Systems**

Description:

> The `umount` command in Linux is used to unmount mounted file systems. Unmounting is the process of detaching the file system from the directory tree, making it no longer accessible until it is mounted again. It is an important step before physically removing portable storage devices to prevent data corruption.

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

---

### <a name="file"></a> `file` *also known as* **File Type**

Description:

> The `file` command in Linux is used to determine the type of a file. It's a handy command when you're not sure what a particular file is, as it will try to classify the file's contents according to various tests, including filesystem tests, magic number tests, and language tests.

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

---

### <a name="stat"></a> `stat` *also known as* **File or File System Status**

Description:

> The `stat` command in Linux is used to display detailed status of a particular file or file system. It provides information like size, permissions, creation time, access time, inode number, and more.

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

---

### <a name="tar"></a> `tar` *also known as* **Tape Archive**

Description:

> The `tar` command in Linux is used to create, maintain, modify, and extract files that are archived in the tar format. It's a widely used command for packaging a set of files for distribution or for backup purposes.

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

---

### <a name="gzip"></a> `gzip` *also known as* **GNU zip**

Description:

> The `gzip` command in Linux is used to compress files. Each file is replaced by a gzipped compressed version of itself, with the name original_name.gz. It's widely used for its speed and simplicity, especially for network file transfers and backup operations.

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

---

### <a name="gunzip"></a> `gunzip` *also known as* **GNU unzip**

Description:

> The `gunzip` command in Linux is used to decompress files compressed by `gzip`. The compressed file is replaced by an uncompressed file with the original name.

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

---

### <a name="zip"></a> `zip` *also known as* **Package and Compress (Zip) Files**

Description:

> The `zip` command in Linux is used to package and compress (archive) files. `zip` is useful for packaging a set of files for distribution, for archiving files, and for saving disk space by temporarily compressing unused files or directories.

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

---

### <a name="unzip"></a> `unzip` *also known as* **Extract Compressed Files in a ZIP Archive**

Description:

> The `unzip` command in Linux is used to extract the contents from the zip archives. It supports password-protected archives. It's handy for extracting files and directories efficiently.

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

---



## <a name="systemServices"></a> System and Service manager

## <a name="remoteConnectivity"></a> Remote Connectivity

## <a name="networkingCommands"></a> Networking

## <a name="packageManagement"></a> Package Management

## <a name="otherCommands"></a> Other Commands
