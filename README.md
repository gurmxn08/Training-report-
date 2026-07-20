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



# Module 2: PC & Network Troubleshooting  
# 1. Common PC Boot Issues and Solutions  
A boot issue means the computer does not start properly.  
No power: Check the power cable, switch, and PSU.  
Black screen: Check monitor connection and RAM.  
Operating System not found: Check boot order and hard disk.  
Boot loop: Use Safe Mode or Startup Repair.  
Slow boot: Remove unnecessary startup programs.  
# 2. Diagnosing Hardware Failures  
RAM (Random Access Memory):  
1.Computer restarts frequently.  
2.System becomes slow or freezes.  
3.Beep sound during startup.  
4.Blue Screen (BSOD) appears.  
5.Reseat or replace the RAM.  
HDD (Hard Disk Drive):  
1.Files take time to open.  
2.Clicking or unusual noises.  
3.Disk read/write errors.  
4.Operating system fails to load.  
5.Check disk health or replace HDD.  
GPU (Graphics Processing Unit):  
1.No display on monitor.  
2.Screen flickers or shows lines.  
3.Games crash or lag.  
4.Computer overheats.  
5.Update drivers or replace GPU.  
PSU (Power Supply Unit):  
1.PC does not turn on.  
2.Random shutdowns.  
3.Burning smell from PSU.  
4.Fans do not spin.  
5.Replace faulty PSU.  

## PC Hardware Troubleshooting  
# 3. BIOS/UEFI Settings and POST Errors  
BIOS/UEFI starts before the operating system.  
It checks all hardware using POST (Power-On Self-Test).  
Wrong BIOS settings can stop the PC from booting.  
Beep codes indicate hardware problems.  
Reset BIOS if settings are incorrect.  
# 4. Peripheral Troubleshooting  
Keyboard:  
Check USB connection.  
Try another USB port.  
Restart the computer.  
Update keyboard driver.  
Mouse:  
Clean the sensor.  
Replace batteries (wireless).  
Check USB connection.   
Update drivers.  
Printer:  
Check power and USB/Wi-Fi connection.  
Ensure paper and ink are available.  
Restart the printer.  
Reinstall printer drivers.  
# 5. Blue Screen of Death (BSOD) and System Crash Analysis  
BSOD is a Windows error screen.  
Usually caused by faulty drivers or hardware.  
Restart the computer.  
Check the error code.  
Update drivers or repair Windows.  
## Software/System Troubleshooting  
# 6. Safe Mode, System Restore, Recovery Tools  
Safe Mode:  
Starts Windows with only essential drivers.  
System Restore:  
Returns the system to an earlier working state.  
Recovery Tools:  
Used to repair boot problems and recover Windows.  
# 7. OS Repair (Windows/Linux Basics)  
Windows:  
Startup Repair  
System File Checker (SFC)  
Reset This PC  
System Restore  
Linux:  
Boot into Recovery Mode.  
Repair file system.  
Update or reinstall packages.  
# 8. Virus/Malware Symptoms and Basic Removal  
Symptoms:  
Computer becomes slow.  
Unwanted pop-up ads.  
Unknown programs appear.  
Files disappear.  
Browser redirects automatically.  
Removal:  
Update antivirus.  
Run a full system scan.  
Remove infected files.  
Keep Windows updated.  
# 9. Driver Issues and Device Manager  
Drivers help hardware communicate with the operating system.  
Missing drivers may stop devices from working.  
Open Device Manager to check hardware.  
Update or reinstall drivers.  
Restart the computer after updating.  
# 10. Disk Errors and Formatting Utilities  
Disk errors can cause data loss or slow performance.  
Scan the disk for errors.  
Remove bad sectors if possible.  
Format the drive if necessary.  
Always back up important data before formatting.  
## Networking Basics  
# 11. IP Addressing, Subnetting, Default Gateway  
IP Address  
A unique number given to every device on a network.  
Subnetting  
Divides a large network into smaller networks.  
Default Gateway  
The device (usually a router) that connects the local network to other networks or the Internet.  

# 12. MAC Address, DNS, DHCP Basics  
MAC Address  
A unique physical address assigned to every network device.  
DNS (Domain Name System)  
Converts website names (like google.com) into IP addresses  
DHCP (Dynamic Host Configuration Protocol)  
Automatically assigns IP addresses to devices.  

# 13. Types of Cables and Connectors  
RJ45  
Standard connector used for Ethernet cables.  
Straight-Through Cable  
Used to connect different devices (PC to Switch).  
Crossover Cable  
Used to connect similar devices (PC to PC or Switch to Switch).  

# 14. Crimping and Cable Testing Basics  
Crimping attaches an RJ45 connector to a network cable.  
A crimping tool is used for this process.  
Cable testers check whether the cable is working correctly.  
They detect wiring faults and broken connections.  
## Network Troubleshooting  
# 15. Diagnosing Connectivity Issues  
Ping  
Checks whether another device is reachable.  
Traceroute  
Shows the path taken by data packets.  
ipconfig (Windows)    
Displays network configuration.  
ifconfig (Linux)  
Displays network interface details.  

# 16. Resolving IP Conflicts and DHCP Errors  
IP Conflict  
Occurs when two devices use the same IP address.  
Solution  
Restart the router.  
Renew the IP address.  
Assign a unique IP.  
DHCP Error  
Occurs when a device cannot obtain an IP address automatically.  
Solution  
Restart the router.  
Enable DHCP.  
Renew the IP configuration.  
# 17. Basic Router/Switch Configuration & Reset  
Connect the device properly.  
Log in to the router settings.  
Configure IP address, Wi-Fi name, and password.  
Save the settings.  
Reset the router if configuration problems occur.  
# 18. Wi-Fi Connectivity Issues  
Common causes:  
Wrong Wi-Fi password.  
Weak signal.  
Too much interference.  
Router is too far away.  
Wi-Fi is turned off.  
Solutions:  
Move closer to the router.  
Restart the router.  
Check the password.  
Change the Wi-Fi channel if needed.  
# 19. Firewall and Antivirus Blocking Checks  
Firewall protects the computer from unauthorized access.  
Antivirus protects against viruses and malware.  
Sometimes they may block trusted applications.  
Check firewall and antivirus settings.  
Allow the required application if it is safe.  



# Module 3: Introduction to HTML & Web Basics
## Introduction to HTML and Web Basics 
# 1. What is HTML and How Browsers Render It    
HTML (HyperText Markup Language) is the standard language used to create web pages. It defines the structure of a webpage using different tags.
A web browser (such as Chrome, Edge, or Firefox) reads the HTML code and converts it into a webpage that users can see and interact with. This process is called rendering.
# 2. Structure of an HTML Document
Every HTML page follows a basic structure.
a)DOCTYPE  
i)Declares that the document is an HTML5 document.  
ii)Helps the browser display the webpage correctly.  
b)Head  
i)Contains information about the webpage.  
ii)Includes the page title, CSS links, meta information, and other settings.   
iii)This content is not directly shown on the webpage.  
c)Body   
i)Contains all the visible content.  
ii)Everything displayed on the webpage, such as text, images, buttons, and links, is placed inside the body.
## Introduction to HTML & Web Basics 
# 3. HTML Tags  
HTML uses tags to organize webpage content.  
a)Headings    
i)Used to create titles and headings.  
ii)There are six heading levels, from largest to smallest.  
b)Paragraphs  
i)Used to write normal text and descriptions.  
c)Lists  
i)Used to display information in an organized way.  
ii)Lists can be ordered (numbered) or unordered (bulleted).  
d)Links  
i)Connect one webpage to another.  
ii)Users can click links to open websites or other pages.  
e)Images  
i)Used to display pictures on a webpage.  
ii)Images make the webpage more attractive and informative.  
## Introduction to HTML & Web Basics
# 4. Forms and Input Types
An HTML form collects information from users.  
Common input types include:  
a)Text  
b)Password  
c)Email  
d)Number   
e)Date  
f)Radio Button  
g)Checkbox  
h)File Upload   
i)Submit Button  
Forms are commonly used for login pages, registration forms, surveys, and contact pages.  
# 4. Semantic HTML
Semantic HTML uses meaningful tags that describe the purpose of the content.
a)Header  
i)Contains the website title, logo, or navigation.  
b)Footer  
i)Contains copyright information, contact details, or links.  
c)Nav   
i)Contains navigation menus and webpage links.    
d)Section  
i) Groups related content into different sections.  
e)Article  
i)Represents an independent piece of content, such as a blog post or news article.   
Semantic HTML improves readability, accessibility, and search engine optimization (SEO). 
## Introduction to HTML & Web Basics
# 5.Basic Styling Using Inline and Internal CSS
1.CSS (Cascading Style Sheets) is used to change the appearance of HTML pages.  
a)Inline CSS  
i)CSS is written directly inside an HTML element.  
ii)It affects only that specific element.  
b)Internal CSS  
i)CSS is written inside the <style> section of the HTML document.  
ii)It applies styles to the entire webpage.  
CSS is used to change:  
1.Text color  
2.Background color  
3.Font size  
4.Borders  
5.Spacing  
6.Alignment  
# 6. Create a Personal Portfolio Website (Multi-Page)
A personal portfolio website is used to introduce yourself and showcase your skills and work.
A simple portfolio may include:  
Home Page – Introduction and welcome message.  
About Page – Personal details, education, and skills.  
Projects Page – Information about projects or achievements.  
Contact Page – Contact information or a contact form.  

A multi-page website connects these pages using HTML links, making it easy for users to navigate.  



# Module 4: Introduction to Git and Version Control
# 1. What is Git and Why Use Version Control
Git is a distributed version control system used to track changes in files and source code. It helps developers work together and keeps a complete history of a project.  
Why use Version Control?  
Tracks every change made to a project.  
Allows multiple people to work on the same project.  
Makes it easy to restore previous versions.   
Helps avoid losing important work.  
Supports teamwork and project management.  
# 2. Git Architecture  
Git stores project data in three main areas.  
a)Repository (Repo)  
i)The repository is the main storage location of a Git project.  
ii)It contains all project files and their complete history.  
b)Working Tree (Working Directory)  
i)The working tree is the folder where you create, edit, or delete files.  
ii)It contains the current version of the project.  
c)Index (Staging Area)  
i)The index is a temporary area where changes are prepared before saving them permanently.  
ii)Only staged changes are included in the next commit.  
## Introduction to Git and Version Control
# 3. Core Git Operations  
a) git init  
i) create new Git repository in a project folder.  
ii) It starts version control for the project.  
b)git add  
i)Adds changed files to the staging area.  
ii)It prepares files for the next commit.  
c)git commit  
i)Saves the staged changes permanently in the repository.  
ii)Each commit creates a snapshot of the project.  
d)git status  
i)Shows the current state of the repository.  
ii)It displays modified, staged, and untracked files.  
e)git log  
i)Displays the history of all commits.  
ii)It shows commit IDs, authors, dates, and messages.  
# 4. Branching and Merging  
Branching  
A branch is a separate line of development.  
It allows developers to work on new features without affecting the main project.  
Merging  
Merging combines changes from one branch into another.  
It is commonly used after completing a feature or fixing a bug.  
# 5. Remote Operations  
A remote repository is a copy of the project stored on an online platform such as GitHub or GitLab.  
Push  
Uploads local commits from your computer to the remote repository.  
Pull  
Downloads the latest changes from the remote repository to your local project.  
Remote  
Connects the local repository with an online repository.  
It allows Git to communicate with GitHub or GitLab.  
# 6. GitHub / GitLab Basics
GitHub  
GitHub is a cloud-based platform that hosts Git repositories.  
It is widely used for collaboration, project sharing, and open-source development.  
GitLab  
GitLab is another Git repository hosting platform.  
It provides version control, collaboration, and built-in DevOps tools.

Both platforms allow users to:

Store Git repositories online.
Collaborate with team members.
Track project changes.
Manage issues and code reviews.
Back up project files securely.
