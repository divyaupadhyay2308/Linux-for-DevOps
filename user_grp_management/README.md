# Linux User & Group Management

A complete practical guide to **Linux User and Group Management** from basic to advanced level.
This repository is designed for DevOps Engineers, Cloud Engineers, and System Administrators who want clear concepts, commands, and real-world administration tasks.

It can also be used for last-minute Linux interview revision.

---

## `USER`

* A user is an account that allows a person or service to log in and interact with the Linux system.

* Each user has:

    - Username

    - User ID (UID)

    - Primary Group ID (GID)

    - Home Directory

    - Default Shell

Example user entry:
```
/etc/passwd
```

Example:
```
devops:x:1001:1001:DevOps User:/home/devops:/bin/bash
```

Explanation:
```
username : password placeholder : UID : GID : comment : home directory : shell
```
Types of users in Linux:
```
| User Type   | Description                           |
| ----------- | ------------------------------------- |
| Root User   | Superuser with full system privileges |
| Normal User | Regular user with limited permissions |
| System User | Used by services and applications     |
```

Example command:
```
whoami
```
Shows the currently logged-in user.

---

## `GROUP`

* A group is a collection of users that share the same permissions.

* Groups help simplify permission management for files, directories, and services.

* Group information is stored in:
```
/etc/group
```

Example:
```
docker:x:999:devops
```
Explanation:
```
group_name : password placeholder : GID : users
```

Example groups in a server:
```
| Group  | Purpose                   |
| ------ | ------------------------- |
| dev    | Developers                |
| qa     | Testers                   |
| docker | Docker access             |
| sudo   | Administrative privileges |
```

---

## Why User & Group Management Matters

* Linux is a multi-user operating system where multiple users can access the system simultaneously.

* Without proper access control:

    - Sensitive files could be accessed by unauthorized users

    - Systems could become insecure

    - Accidental changes could break production systems

* Proper user and group management helps in:

    - Access control

    - System security

    - Resource isolation

    - Permission management

    - Production environment administration

Every **file, process, and service** in Linux runs under a user and group context.

* Linux follows the Principle of Least Privilege:

    - Users should only have the permissions necessary to perform their tasks.

---

## Understanding Users and Groups

This section explains the different **types of users and groups in Linux**.

---

### Types of Users

- **root** → Superuser with full permissions on the system  
- **normal user** → Regular user who can log in and perform daily tasks  
- **system user** → Accounts created by the system for services like `nginx`, `mysql`, `sshd`  
- **service account** → Dedicated account used by an application or process to run securely  

---

### Types of Groups

- **primary group** → The main group assigned to a user when the account is created  
- **secondary group** → Additional groups assigned to a user to grant extra permissions  

---

### Useful Commands

```bash
id
whoami
groups
```

---

### Important Files

Explain each one:

- **/etc/passwd** → user account information

- **/etc/shadow** → encrypted passwords

- **/etc/group** → group information

- **/etc/gshadow** → secure group info

- **/etc/login.defs** → default user account settings

- **/etc/skel/** → default files copied to new user home directory

Useful commands:

```bash
cat /etc/passwd
cat /etc/group
sudo cat /etc/shadow
```

Also explain /etc/passwd fields:
```
username:x:UID:GID:comment:home-directory:login-shell
```
---

### Basic User Management
Cover user creation, deletion, checking details.
Commands:
```
useradd
adduser
passwd
id
finger
who
w
```
Examples:
```
sudo useradd devopsuser
sudo passwd devopsuser
id devopsuser
```
Create user with home directory:
```
sudo useradd -m devopsuser
```
Create user with custom shell:
```
sudo useradd -m -s /bin/bash devopsuser
```
Delete user:
```
sudo userdel devopsuser
```
Delete user with home directory:
```
sudo userdel -r devopsuser
```
Also explain difference:

- **useradd** → low-level command

- **adduser** → more friendly interactive command (mostly Debian/Ubuntu)
- 
---

### Basic Group Management

Commands:
```
groupadd
groupdel
groupmod
groups
id
getent group
```

Examples:
```
sudo groupadd devops
getent group devops
sudo groupdel devops
```

Explain:
- creating groups

- deleting groups

- checking group membership

---

### Password Management

Cover:

- setting password

- changing password

- locking/unlocking password

- forcing password change

Commands:
```
passwd
chpasswd
passwd -l
passwd -u
passwd -e
```

Examples:
```
sudo passwd devopsuser
sudo passwd -l devopsuser
sudo passwd -u devopsuser
sudo passwd -e devopsuser
```

Explain:

* -l locks account password

* -u unlocks password

* -e expires password immediately

---
