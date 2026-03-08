# Linux File System

* Understanding the Linux file system is important for DevOps engineers because many production issues involve disks, logs, or storage paths.

* In Linux, **everything is treated as a file** — regular files, directories, devices, and even processes.

* Linux uses a **hierarchical directory structure** that starts from the **root directory `/`**.

```/
├── bin
├── dev
├── etc
├── home
├── media
├── mnt
├── root
├── sbin
├── tmp
├── usr
└── var
```


Every directory in Linux exists under the **root `/` directory**.

---

# Important Linux Directories (Interview Focus)

## `/`
The **root directory** is the top-level directory of the Linux file system.

All files and directories originate from `/`.

Example:

```bash
cd /
ls
```
---

## `/bin` - Binary Files

Contains essential user commands required for system operation.

Example:

```bash
ls
cp
mv
cat
pwd
echo
```
---

## `/sbin` - System Binaries

Contains system administration commands, mostly used by the root user.

Examples:

```bash
reboot
shutdown
fdisk
mount
ifconfig
```
---


## `/etc` - Configuration files

* Contains system configuration files.

* This directory is very important for system administration and DevOps work.

* It stores system wide configuration files for Linux and installed services.

Common files:

/etc/passwd
/etc/shadow
/etc/hosts
/etc/fstab
/etc/ssh/sshd_config

Example:

```bash
cat /etc/passwd
```
This command shows the list of users on the system.

---


## `/home`

Contains home directories for normal users.

Example:

```bash
/home/divya
/home/user1
```

---

## `/root`

Home directory of the root (administrator/super) user.

```bash
/root
```
* Note: This is different from /home.

---

## `/var`

* Contains variable data, such as logs, caches and application data that changes during system operation.

* Very important for production troubleshooting.

Important directory:
```
/var/log
```

Example:
```bash
cd /var/log
ls
```

Common logs:
```
syslog
messages
auth.log
nginx.log
```

Example:

```bash
tail -f /var/log/syslog
```
* This command monitors logs in real time.

---

## `/tmp`

* Stores temporary files created by applications.

* Files here may be deleted automatically after reboot.

Example:

```bash
cd /tmp
```

---


## `/usr` - User Binaries

Contains user programs, libraries, and documentation.

Important subdirectories:

/usr/bin
/usr/lib
/usr/share

* Most installed software goes here.

--- 

## `/dev` - Device Files

Hardware in Linux is accessed as files, and those files live in **/dev**.

Examples:

/dev/sda - Hard Disk
/dev/sda1
/dev/null
/dev/tty - Terminal

Example:

```bash
ls /dev
```

---

## `/media`

* `/media` is used for **automatically mounted removable devices** such as:

- USB drives
- External hard disks
- CD/DVD

* When you plug in a USB device, Linux usually mounts it inside `/media`.

Example:

```bash
ls /media
```

Example path after inserting a USB drive:

/media/username/USB_DRIVE


---

## `/mnt`

* `/mnt` is used for manually mounting temporary filesystems.

* System administrators often use this directory when they want to mount a disk temporarily.

Example use cases:

Mounting a new disk
Mounting an NFS share
Mounting a backup disk


Example command:

```bash
sudo mount /dev/sdb1 /mnt
```
Check mounted files:

```bash
ls /mnt
```