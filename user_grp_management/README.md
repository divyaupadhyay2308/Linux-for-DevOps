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

## Understanding Users and Groups:

Cover:

    - Root user

    - Normal user

    - System user

    - Service account

    - Primary group

    - Secondary group

Explain simply:

### Types of users

    - **root** → superuser with full permissions

    - **normal user** → regular login user

    - **system user** → used by services like nginx, mysql

    - **service account** → dedicated account for application/process

### Types of groups

    - **primary group** → main group of user

    - **secondary group** → additional groups for extra permissions

Commands:
```bash
id
whoami
groups
```