# Training-Report
# Module 1: Fundamentals of Unix/Linux & BASH Essentials
## Introduction to Linux
# Linux Installation:
# •	Installing Linux in a Virtual Machine (Virtual Box / VMware)
1.Download the Linux ISO file (e.g., Ubuntu).  
2.Install VirtualBox or VMware on your computer.  
3.Open the software and click New to create a virtual machine.  
4.Enter the virtual machine name and select Linux as the operating system.  
5.Allocate RAM (minimum 2 GB, recommended 4 GB or more).  
6.Create a virtual hard disk (20–25 GB or more).  
7.Attach the Linux ISO file as the startup/boot disk.  
8.Start the virtual machine and choose Install Linux.  
9.Select language, keyboard, and installation options.  
10.Create a user account by entering your username and password.
11.Wait for the installation to complete.
12.Restart the virtual machine and remove the ISO file if prompted.
13.Log in and start using Linux.
# •	Bare-metal installation (Dual boot / full disk), Partitioning schemes: MBR vs GPT, /, /home, /swap, /boot
Bare-metal installation means installing Linux directly on the computer's hard drive instead of inside a virtual machine.

1. Dual Boot
 a)Linux is installed alongside Windows.
 b)You can choose which operating system to use when the computer starts.
 c)Best if you want to use both Windows and Linux on the same PC.
2. Full Disk Installation
 a)Linux uses the entire hard drive.
 b)All existing data and the previous operating system are removed.
 c)Best if you want to use only Linux.
# Partitioning Schemes: MBR vs GPT
MBR (Master Boot Record)	                                               GPT (GUID Partition Table)
1.Older partition style	                                             1.Modern partition style
2.Supports up to 2 TB disk size	                                     2.Supports disks larger than 2 TB
3.Maximum 4 primary partitions	                                     3.Supports many partitions (typically up to 128)
4.Used with Legacy BIOS	                                             4.Used with UEFI systems
5.Less secure                                                       5.More reliable with backup partition information
# Common Linux Partitions
1. / (Root Partition)
a)Main partition of Linux.
b)Contains the operating system and system files.
c)Required for every Linux installation.
2. /home
a)Stores user files, documents, downloads, pictures, and personal settings.
b)Keeping it separate helps protect personal data during OS reinstallation.
3. /swap
a)Used as virtual memory when RAM is full.
b)Also helps with hibernation on some systems.
4. /boot
a)Contains bootloader files and the Linux kernel.
b)Required for starting the operating system.

## Introduction to BASH & Linux Command Line Essentials:
# 1.Shell and BASH
A Shell is a command-line interface that allows users to communicate with the Linux operating system. It accepts commands from the user, sends them to the kernel, and displays the output.
Examples of Shells:
1.Bash (Bourne Again Shell)
2.Sh (Bourne Shell)
3.Zsh (Z Shell)
4.Csh (C Shell)
BASH : BASH (Bourne Again Shell) is the most commonly used shell in Linux. It is the default shell in many Linux distributions and is used to run Linux commands and shell scripts.
Features of BASH:
1.Executes Linux commands.
2.Supports shell scripting.
3.Maintains command history.
4.Supports auto-completion using the Tab key.
5.Allows variables, loops, and conditional statements.
 # 2.Files system structure: /, /home, /etc, /var, etc.
 The Linux file system is organized in a tree-like structure. Everything starts from the root directory (/), and all other files and folders are stored inside it.
1. / (Root Directory)
a) It is the top-level directory in Linux.
b) All other directories and files are located under it.
c) It is the starting point of the Linux file system.
2. /home
a) Stores user files and personal data.
b) Each user has a separate home folder.
c) Example: /home/vipan
3. /etc
a) Contains system configuration files.
b) Stores settings for the operating system and installed applications.
c) Mostly used by system administrators.
4. /var
a) Stores variable data that changes frequently.
b) Includes log files, cache files, mail, and temporary data.
5. /bin
a) Contains essential Linux commands such as ls, cp, mv, and cat.
# File & Directory permissions (chmod, chown)
In Linux, file and directory permissions control who can read, write, or execute a file or folder. They help protect data and improve system security.
1. File Permissions
There are three types of permissions:
a)Read (r): Allows viewing the contents of a file.
b)Write (w): Allows modifying or deleting a file.
c)Execute (x): Allows running a file as a program or script.
These permissions are assigned to:
a)User (u): File owner
b)Group (g): Users in the same group
c)Others (o): All other users
2. chmod Command (Change Mode):
The chmod command is used to change the permissions of a file or directory.
3. chown Command (Change Owner):
The chown command is used to change the owner of a file or directory.
# Basic file operations: cp, mv, rm, ls, etc.
1. ls (List) : Used to display the files and directories in the current location.
2. cp (Copy) : Used to copy files or directories from one location to another.
3. mv (Move) : Used to move files or directories to a different location or rename them.
4. rm (Remove) : Used to delete files or directories.
5. mkdir (Make Directory) : Used to create a new directory.
6. rmdir (Remove Directory) : Used to delete an empty directory.
7. cat (Concatenate) : Used to display the contents of a file.
# Redirection and Pipes: >, >>, |
1. > (Output Redirection)
a) Used to send the output of a command to a file.
b) If the file already exists, its contents are overwritten.
2. >> (Append Redirection)
a) Used to add the output of a command to the end of a file.
b) It does not overwrite the existing contents.
3. | (Pipe)
a) Used to send the output of one command as the input to another command.
b) It helps combine multiple commands to perform a task.
# Wildcards, quoting, and escaping characters
1. Wildcards
a)Wildcards are special characters used to match file or directory names.
b)They help perform operations on multiple files at once.
Common Wildcards:
a)* – Matches any number of characters.
b)? – Matches exactly one character.
c)[ ] – Matches any one character from the given set or range.
2. Quoting
a)Quoting is used to treat text as a single string.
b)It prevents the shell from interpreting special characters.
Types of Quoting:
a)Single quotes (' ') – Treat all characters literally.
b)Double quotes (" ") – Preserve the text but still allow variables and command substitution.
3. Escaping Characters
a)Escaping is used to give special characters their literal meaning.
b)It is done using the backslash (\) before the special character.
## Introduction to BASH & Linux Command Line Essentials:
# BASH Scripting
# 1. Writing Simple Shell Scripts
A shell script is a text file that contains Linux commands. It helps automate tasks, so the same commands do not have to be typed again and again.
a)Variables
i)Variables are used to store values like names, numbers, or paths.
ii)Their values can be used multiple times in a script.
iii)Example uses: storing a user's name, age, or file name.
b)Printing Text
i)Text is displayed on the screen to show messages or results.
ii)This makes the script easier to understand for the user.
c)Basic Conditionals
i)Conditionals help the script make decisions.
ii)The script checks a condition and performs different actions based on whether it is true or false.
iii)Example: checking if a file exists or if a number is greater than another number.
# 2. Using man and help for Linux Commands
Linux provides built-in documentation to learn about commands.
a)man (Manual)
i)Displays detailed information about a command.
ii)It explains the command, options, and usage.
iii)It is useful when you want complete documentation.
b)help
Shows quick help for shell built-in commands.
i)It provides a short explanation and basic usage.
ii)It is faster than the manual page for built-in commands.
3. Working with Text-Processing Tools
These tools are used to search, edit, and process text files.
a)grep
i)Searches for specific words or patterns in a file.
ii)It helps find matching lines quickly.
b)awk
i)Processes and formats text data.
ii)It is useful for extracting specific columns and generating reports.
c)sed
i)Edits text without opening the file.
ii)It can search, replace, delete, or modify text automatically.
4. File Compression
File compression reduces file size and makes files easier to store or transfer.
a)tar
i)Combines multiple files and folders into a single archive.
ii)It does not compress files by itself.
b)gzip
i)Compresses files to reduce their size.
ii)It is often used together with tar.
c)zip
i)Compresses one or more files into a ZIP archive.
ii)It is commonly used because it works on both Linux and Windows.
