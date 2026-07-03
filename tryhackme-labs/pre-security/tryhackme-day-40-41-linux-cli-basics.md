# TryHackMe Day 40–41: Linux CLI Basics

## Room Information

- **Room Name:** Linux CLI Basics
- **Platform:** TryHackMe
- **Status:** Completed ✅
- **Day:** 40–41
- **Difficulty:** Beginner
- **Topics Covered:** Linux Terminal, File Navigation, System Information, Linux Commands, File Searching

---

## Overview

In this room, I learned the fundamentals of working with the Linux Command Line Interface (CLI). Instead of relying on a graphical user interface, Linux users and cybersecurity professionals often interact directly with the system through terminal commands.

The room introduced basic navigation, file management, system information gathering, and file searching techniques that form the foundation of Linux administration and cybersecurity operations.

---

# What is the Linux Terminal?

The Linux Terminal is a text-based interface that allows users to interact directly with the operating system by typing commands.

Cybersecurity professionals use the terminal because:

- It is faster than graphical interfaces
- It provides greater control over the system
- Many security tools operate exclusively in the terminal
- It allows automation through scripting

Learning the terminal is one of the most important steps toward becoming a cybersecurity professional.

---

# Learning Objectives

During this room I learned how to:

- Understand the purpose of the Linux terminal
- Navigate the Linux filesystem
- Locate files using search commands
- Read file contents
- Gather system information
- Understand basic Linux commands
- Explore important Linux directories

---

# Linux Filesystem Basics

Linux stores data using a hierarchical directory structure.

Example:

```text
/
├── home
├── etc
├── var
├── usr
├── bin
└── tmp
```

Everything in Linux exists within this filesystem structure.

---

# Command 1: pwd

## Print Working Directory

The `pwd` command displays the current directory location.

Example:

```bash
pwd
```

Output:

```text
/home/ubuntu
```

Purpose:

- Shows where you currently are in the filesystem
- Helps prevent navigation mistakes
- Useful when working across multiple directories

---

# Command 2: ls

## List Directory Contents

The `ls` command displays files and folders inside the current directory.

Example:

```bash
ls
```

Output may include:

```text
Desktop
Documents
Downloads
Music
Pictures
Projects
```

This command is used constantly in Linux environments.

---

## ls -l

The `-l` option provides detailed information.

Example:

```bash
ls -l
```

Additional information shown:

- Permissions
- Owner
- Group
- File size
- Modification date

This is useful when investigating files and permissions.

---

## ls -al

The `-a` option displays hidden files.

Example:

```bash
ls -al
```

Hidden files begin with a dot:

```text
.bashrc
.profile
.Xauthority
```

These files are often used for configuration purposes.

---

# Hidden Files

Linux hides files beginning with a period (`.`).

Examples:

```text
.bashrc
.profile
.config
```

These files are not secret but are hidden to reduce clutter.

Many Linux settings are stored inside hidden files.

---

# Command 3: cd

## Change Directory

The `cd` command allows movement between folders.

Example:

```bash
cd Documents
```

Changes location to:

```text
/home/ubuntu/Documents
```

This is one of the most frequently used Linux commands.

---

## Moving Back a Directory

To move up one level:

```bash
cd ..
```

Example:

```text
/home/ubuntu/Documents
```

becomes

```text
/home/ubuntu
```

The two dots (`..`) represent the parent directory.

---

# Command 4: find

## Searching for Files

The `find` command searches for files within directories.

Example:

```bash
find ~ -name mission_brief.txt
```

Explanation:

- `~` = Home directory
- `-name` = Search by filename

Output:

```text
/home/ubuntu/projects/mission_brief.txt
```

This command is extremely valuable during investigations and incident response.

---

# Why Security Professionals Use find

Common uses include:

- Locating log files
- Finding suspicious files
- Searching for malware artifacts
- Identifying configuration files

The `find` command is one of the most powerful Linux utilities.

---

# Command 5: cat

## Reading File Contents

The `cat` command displays the contents of a file.

Example:

```bash
cat mission_brief.txt
```

Output:

```text
Mission details and instructions
```

The command is frequently used for:

- Reading configuration files
- Viewing logs
- Examining text documents

---

# Gathering System Information

System information helps administrators and security teams understand:

- Operating system details
- Available resources
- Current users
- Kernel versions

This information is important during troubleshooting and investigations.

---

# Command 6: whoami

## Identify Current User

The `whoami` command displays the currently logged-in user.

Example:

```bash
whoami
```

Output:

```text
ubuntu
```

This is useful when verifying account privileges.

---

# Command 7: uname

## Viewing Operating System Information

The `uname` command displays operating system information.

Example:

```bash
uname
```

Output:

```text
Linux
```

This identifies the operating system kernel.

---

## uname -a

For detailed information:

```bash
uname -a
```

Displays:

- Kernel name
- Hostname
- Kernel version
- Architecture
- Operating system type

Example output includes:

```text
Linux
x86_64
GNU/Linux
```

---

# Understanding System Information

Key components returned by `uname -a`:

### Linux

The operating system kernel.

### Hostname

The computer's name.

### Kernel Version

The specific version of Linux installed.

### x86_64

Indicates a 64-bit architecture.

### GNU/Linux

Represents Linux combined with GNU system tools.

---

# Command 8: df -h

## Checking Disk Usage

The `df` command displays disk information.

Example:

```bash
df -h
```

The `-h` flag means:

```text
Human Readable
```

Sizes appear as:

```text
1G
500M
20G
```

instead of raw byte values.

---

# Understanding Disk Information

Important fields include:

### Filesystem

The storage device or partition.

### Size

Total storage capacity.

### Used

Space currently in use.

### Available

Remaining free space.

### Use%

Percentage of disk space consumed.

### Mounted On

Location where the filesystem is attached.

---

# Temporary Filesystems (tmpfs)

Linux may display entries such as:

```text
tmpfs
```

These represent temporary storage in RAM.

Characteristics:

- Fast performance
- Non-persistent
- Cleared after reboot

Common examples:

```text
/dev/shm
/run
```

---

# Exploring the /etc Directory

The `/etc` directory contains important system configuration files.

Navigation:

```bash
cd /etc
```

Listing contents:

```bash
ls
```

Common files found here include:

```text
fstab
os-release
hosts
resolv.conf
```

Understanding `/etc` is essential for Linux administration.

---

# Reading System Configuration Files

Linux stores operating system details inside:

```text
/etc/os-release
```

View contents using:

```bash
cat /etc/os-release
```

This file provides detailed information about the Linux distribution.

---

# Understanding os-release

Important fields include:

### PRETTY_NAME

```text
Ubuntu 24.04.1 LTS
```

Human-readable operating system name.

---

### VERSION_ID

```text
24.04
```

Operating system version.

---

### VERSION_CODENAME

```text
noble
```

Distribution codename.

---

### ID

```text
ubuntu
```

Distribution identifier.

---

# Why Linux Matters in Cybersecurity

Linux is heavily used throughout cybersecurity because:

- Most servers run Linux
- Security tools are built for Linux
- Penetration testing environments use Linux
- Cloud platforms commonly run Linux systems

Examples:

- Kali Linux
- Ubuntu
- Parrot OS
- Debian
- Red Hat Enterprise Linux

A strong Linux foundation is essential for success in cybersecurity.

---

# Key Commands Learned

| Command | Purpose |
|----------|----------|
| pwd | Show current directory |
| ls | List files and folders |
| ls -l | Detailed file listing |
| ls -al | Show hidden files |
| cd | Change directory |
| cd .. | Move to parent directory |
| find | Search for files |
| cat | Display file contents |
| whoami | Show current user |
| uname | Show operating system |
| uname -a | Detailed system information |
| df -h | Display disk usage |

---

# Key Takeaways

- The Linux terminal is a powerful text-based interface.
- `pwd` identifies the current location.
- `ls` displays files and folders.
- `cd` is used to move through directories.
- `find` helps locate files efficiently.
- `cat` displays file contents.
- `whoami` identifies the active user.
- `uname -a` provides system information.
- `df -h` displays disk usage statistics.
- `/etc/os-release` contains Linux distribution details.

---

# Skills Gained

- Linux terminal navigation
- File system exploration
- File searching techniques
- Reading configuration files
- Gathering system information
- Understanding Linux distributions
- Basic command-line operations
- Linux troubleshooting fundamentals

---
## Completion Badge

![Linux CLI Basics](../../assets/linux-cli-basics.jpg)

---
## Reflection

This room gave me my first practical experience using the Linux command line. I learned how to navigate the filesystem, locate files, read configuration data, and gather system information using essential Linux commands. These skills form the foundation for future topics such as user management, permissions, process management, security monitoring, and penetration testing.

---
