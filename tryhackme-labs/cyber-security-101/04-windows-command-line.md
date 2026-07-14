# Windows Command Line

## 🧠 What I Learned

In this room, I learned how to use the **Windows Command Prompt (cmd.exe)** to perform common administrative and troubleshooting tasks without relying on the graphical interface.

Although Windows provides a GUI for almost everything, the command line is often faster, consumes fewer system resources, and is essential for remote administration, scripting, and cybersecurity work.

Learning these commands is an important step toward becoming comfortable working on Windows systems in enterprise environments.

---

## Why Learn the Command Line?

The Windows Command Prompt provides several advantages over using the graphical interface:

- Faster navigation
- Lower system resource usage
- Easier automation through scripts
- Efficient remote administration
- Better troubleshooting capabilities

Many cybersecurity tools and administrative tasks rely on command-line skills, making them an essential part of every security professional's toolkit.

---

## Viewing System Information

I learned several commands used to gather information about a Windows system.

### Display Environment Variables

```
set
```

Shows system environment variables, including the system PATH.

---

### Check Windows Version

```
ver
```

Displays the installed Windows version.

---

### Display Detailed System Information

```
systeminfo
```

Provides information such as:

- Operating System
- Computer Name
- Processor
- Installed Memory
- System Architecture
- Boot Time

This command is useful during system enumeration.

---

## Useful Command Prompt Commands

### Display Help

```
help
```

Shows available commands or help information.

Most commands also support:

```
command /?
```

to display detailed usage instructions.

---

### Clear the Screen

```
cls
```

Clears everything displayed in the terminal.

---

## Viewing Long Output

Sometimes command output is too large to fit on one screen.

Using:

```
command | more
```

allows the output to be viewed one page at a time.

Example:

```
driverquery | more
```

This makes lengthy output much easier to read.

---

# Network Configuration

One of the most useful sections of this room covered networking commands.

---

## Display IP Configuration

```
ipconfig
```

Shows:

- IPv4 Address
- IPv6 Address
- Subnet Mask
- Default Gateway

---

## Detailed Network Information

```
ipconfig /all
```

Displays additional information including:

- MAC Address
- DHCP Status
- DNS Servers
- Lease Information
- Network Adapter Details

This is one of the first commands used during network troubleshooting.

---

## Test Connectivity

```
ping example.com
```

The **ping** command checks whether another host is reachable.

It also measures:

- Packet loss
- Response time
- Network latency

Successful replies confirm network connectivity.

---

## Trace the Network Route

```
tracert example.com
```

The **tracert** command shows every router (hop) between your computer and the destination.

It is useful for locating where network connectivity problems occur.

---

## DNS Lookup

```
nslookup example.com
```

Retrieves the IP address associated with a domain name.

A different DNS server can also be specified.

Example:

```
nslookup example.com 1.1.1.1
```

This queries Cloudflare's DNS server instead of the default DNS server.

---

## Display Network Connections

```
netstat
```

Shows active network connections.

Useful options include:

```
netstat -a
```

Displays all active and listening connections.

```
netstat -b
```

Shows the executable associated with each connection.

```
netstat -o
```

Displays the Process ID (PID).

```
netstat -n
```

Displays numerical IP addresses and port numbers.

A common troubleshooting command combines these options:

```
netstat -abon
```

This reveals listening ports, associated processes, and process IDs, making it very useful during incident response and malware investigations.

---

# Working with Directories

I also learned how to navigate the Windows file system using only the command line.

---

## Show Current Directory

```
cd
```

Displays the current working directory.

---

## List Files and Folders

```
dir
```

Lists files and directories in the current location.

Useful options include:

```
dir /a
```

Displays hidden files.

```
dir /s
```

Lists files recursively through all subdirectories.

---

## Display Folder Structure

```
tree
```

Provides a graphical view of the directory hierarchy.

---

## Change Directory

```
cd FolderName
```

Moves into another folder.

To move back one directory:

```
cd ..
```

---

## Create and Remove Directories

Create a folder:

```
mkdir Backup
```

Delete a folder:

```
rmdir Backup
```

---

# Working with Files

Several commands were introduced for basic file management.

---

## Display File Contents

```
type filename.txt
```

Displays the contents of a text file directly in the terminal.

For longer files:

```
more filename.txt
```

Displays one page at a time.

---

## Copy Files

```
copy file1.txt file2.txt
```

Creates a duplicate of a file.

---

## Move Files

```
move file.txt Destination
```

Moves a file to another location.

---

## Delete Files

```
del file.txt
```

or

```
erase file.txt
```

Both commands permanently remove files.

---

## Wildcards

Windows supports wildcard characters.

Example:

```
copy *.md C:\Markdown
```

Copies every Markdown file into another directory.

---

# Task and Process Management

Another important topic covered was managing running processes.

---

## View Running Processes

```
tasklist
```

Displays every running process together with its:

- Process Name
- Process ID (PID)
- Memory Usage

---

## Filter Processes

Example:

```
tasklist /FI "imagename eq sshd.exe"
```

Displays only processes matching the specified executable.

Filtering makes large process lists easier to analyze.

---

## Terminate a Process

```
taskkill /PID 1234
```

Stops a running process using its Process ID.

This command is particularly useful when dealing with unresponsive applications or suspicious processes.

---

# Additional Useful Commands

Although not covered in depth, I also learned about several important Windows commands:

- `chkdsk` – Checks disks for errors
- `driverquery` – Lists installed device drivers
- `sfc /scannow` – Scans and repairs corrupted Windows system files

These commands are frequently used by system administrators during troubleshooting.

---

# Key Takeaways

From this room I learned that:

- Windows Command Prompt is an essential administrative and cybersecurity tool.
- `systeminfo` provides valuable system enumeration information.
- `ipconfig`, `ping`, `tracert`, `nslookup`, and `netstat` are fundamental networking commands.
- File system navigation can be performed entirely from the command line.
- File and folder management can be automated using built-in commands.
- `tasklist` and `taskkill` are useful for monitoring and managing running processes.
- Most commands support `/ ?` to display built-in documentation.
- Piping output with `| more` makes long command output much easier to read.

This room strengthened my Windows command-line skills and gave me practical commands that I can use for system administration, troubleshooting, and cybersecurity investigations.

---

## 📸 Proof of Completion

![Windows Command Line](../../assets/04-windows-command-line.jpg)
