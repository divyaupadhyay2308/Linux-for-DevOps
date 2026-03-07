## 💻 Basic Linux Commands
These are essential Linux commands every DevOps engineer should know for daily operations and interviews.

### System Information - uname command

* uname stands for Unix Name.
* It is used to display system information about the Linux operating system and kernel.
* The most commonly used option is uname -a, which displays all system details.

Use Case:
  * Identify system architecture
  * Check kernel version
  * Verify server environment
  * Troubleshoot system compatibility issues
    
Basic syntax:
```bash
uname -a
```
---

### hostname - Check hostname

* The hostname command is used to display or set the name of a system (server) on a network.
* Every Linux machine has a unique hostname so it can be identified in a network environment.

Use Casse:
  * Identify servers in clusters and environments
  * Configure monitoring tools
  * Manage multiple servers in production
  * Verify server identity in scripts

Basic syntax:
```bash
hostname
```
---

### whoami – Show Current User

* The whoami command displays the username of the currently logged-in user.

Use Case:
  * Helps verify whether you are running commands as root or a normal user.

Basic syntax:
```bash
whoami
```
---

### date – Display Current Date and Time

* The date command shows the current system date and time.

Use Case:
  * Checking server time
  * Log troubleshooting
  * Automation scripts
    
Basic syntax:
```bash
date
```

---


### uptime – System Running Time

* The uptime command shows how long the system has been running.

Use Case:
  * Used to check system stability and load on servers.
  
Basic syntax:
```bash
uptime
```

---

### ls – List Directory Contents

* The ls command is used to list files and directories.

Use Case:
  * Used to quickly check files, logs, scripts, and configuration files.

Basic syntax:
```bash
ls
```
---

### pwd – Print Working Directory

* The pwd command shows the current directory path where you are working in the Linux file system.

Use Case:
  * Used to confirm the current working location before executing scripts or commands.

Basic syntax:
```bash
pwd
```
---

### cd – Change Directory

* The cd command is used to navigate between directories.

Use Case:
* Used to move between application directories, log folders, and configuration paths.

Basic syntax:
```bash
cd /path
```
---

### mkdir - Create directory

* The mkdir command stands for make directory.
* It is used to create new directories (folders) in the Linux file system.

Use Case:
  * Create application directories
  * Store logs and backups
  * Organize deployment files
  * Prepare project folder structures
    
Basic syntax:
```bash
mkdir folder_name
```
---

### rmdir – Remove Directory

* The rmdir command is used to delete an empty directory.

Use Case:
  * Used to remove unused empty directories from project environments.
    
Basic syntax:
```bash
rmdir folder_name
```

---

### touch – Create Empty File

* The touch command is used to create a new empty file or update the timestamp of an existing file.

Use Case:
  * Create log files
  * Create script files
  * Prepare configuration files
    
Basic syntax:
```bash
touch file.txt
```
---

### cat – Display File Content

* The cat command is used to display the contents of a file.

Use Case:
  * Used to quickly check configuration files or logs.
    
Basic syntax:
```bash
cat file.txt
```
---

### cp – Copy Files or Directories

* The cp command is used to copy files or directories.

Use Case:
  * Creating backup files
  * Copying configuration files
  * Moving application files between directories
    
Basic syntax:
```bash
cp file.txt backup.txt
```
---

### mv – Move or Rename Files

* The mv command is used to move files/directories or rename them.

Use Case:
  * Organize application files
  * Move log files
  * Rename configuration files
    
Basic syntax:
```bash
mv file.txt newfile.txt
```
---

### rm – Remove Files or Directories

* The rm command is used to delete files or directories.

Use Case:
  * Delete temporary files
  * Remove old logs
  * Clean up deployment directories
    
Basic syntax:
```bash
rm file.txt
```

---

## ❓ Getting Help in Linux

Linux provides built-in help for commands.

### man – Manual Command

* The man command is used to display the manual page for any command.

Use Case:
  * Used to quickly learn command options while working on servers.

Basic syntax:
```bash
man command_name
```

Example:

```bash
man ls
```

### help - Command in Linux

* The help command is used to display information about shell built-in commands.
* It provides quick guidance on how to use a command and its options.
* This command mainly works with bash built-in commands.

Use Case:
  * Learning new commands
  * Checking command syntax quickly
  * Troubleshooting shell commands

Basic syntax:
```bash
command --help
```

---

# Quick Summary

## Command	            Purpose
rmdir	          Remove empty directory
touch	          Create empty file
cat	            Display file content
cp	            Copy files/directories
mv	            Move or rename files
rm	            Delete files/directories
man	            Show command manual

----
