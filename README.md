# Common Commands for Linux and Mac OS

This document is a markdown dictionary with copy and paste commands that can be used for Linux Flavors as well as Mac OS

## File System

### `cd` *also known as* **Change Directory**

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

### `pwd` *also known as* **Print Working Directory**

Description:

> This command is used to display the full path of the current directory in which the user is working. This command is beneficial for keeping track of the user's location within the complex file hierarchy of Linux.


Examples:

`pwd`

> Displays to the Command Line Interface the current directory in which the user is working

---

### `ls` *also known as* **List**

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

### `mkdir` *also known as* **Make Directory**

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

### `rmdir` *also known as* **Remove Directory**

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
### `rm` *also known as* **Remove Files or Directories**

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
### `cp` *also known as* **Copy Files and Directories**

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

### `mv` *also known as* **Move or Rename Files**

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
