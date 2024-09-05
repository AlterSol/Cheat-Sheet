## Introduction
Linux is a powerful and widely-used open-source operating system. It provides a variety of commands to perform different tasks efficiently, from basic file manipulation to advanced network configuration and system administration. This cheat sheet covers essential Linux commands, file management, networking, package management, and other useful operations for both beginners and experienced users.

## Basic Commands
- `pwd` : Print the current working directory.
- `ls` : List the contents of a directory.
- `cd [directory]` : Change the current directory.
- `mkdir [directory]` : Create a new directory.
- `rmdir [directory]` : Remove an empty directory.
- `rm [file]` : Remove a file.
- `rm -r [directory]` : Remove a directory and its contents recursively.
- `cp [source] [destination]` : Copy files or directories.
- `mv [source] [destination]` : Move or rename files or directories.

## File Permissions
- `chmod [permissions] [file]` : Change file permissions.
- `chown [owner]:[group] [file]` : Change file owner and group.

## File Viewing and Editing
- `cat [file]` : Display the contents of a file.
- `less [file]` : View the contents of a file page by page.
- `nano [file]` : Open a file in the nano text editor.
- `vim [file]` : Open a file in the vim text editor.

## System Information
- `uname -a` : Display all system information.
- `df -h` : Show disk space usage in human-readable format.
- `free -h` : Display memory usage in human-readable format.
- `top` : Display running processes and system resource usage.
- `ps aux` : List all running processes.

## Networking
- `ifconfig` : Display network configuration.
- `ping [host]` : Send ICMP ECHO_REQUEST packets to network hosts.
- `netstat -tuln` : Display network connections, routing tables, etc.
- `curl [url]` : Transfer data from or to a server.

## Package Management (Debian/Ubuntu)
- `apt update` : Update the package list.
- `apt upgrade` : Upgrade all the installed packages.
- `apt install [package]` : Install a new package.
- `apt remove [package]` : Remove a package.

## Searching
- `find [directory] -name [filename]` : Search for files in a directory hierarchy.
- `grep [pattern] [file]` : Search for a specific pattern in a file.

## Archiving and Compression
- `tar -czvf [archive.tar.gz] [directory]` : Create a compressed `.tar.gz` archive.
- `tar -xzvf [archive.tar.gz]` : Extract a `.tar.gz` archive.
- `zip [archive.zip] [file]` : Create a `.zip` archive.
- `unzip [archive.zip]` : Extract a `.zip` archive.

## User Management
- `adduser [username]` : Add a new user.
- `passwd [username]` : Change the password for a user.
- `deluser [username]` : Delete a user.

## File System
- `mount [device] [mount-point]` : Mount a filesystem.
- `umount [mount-point]` : Unmount a filesystem.

## Miscellaneous
- `history` : Show command history.
- `alias [alias_name]='[command]'` : Create an alias for a command.
- `echo $PATH` : Display the current PATH environment variable.
