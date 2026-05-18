# TryHackMe — Linux Fundamentals Part 1

## 🧠 What I learned

### Basic Linux Commands

| Command | Description |
|---|---|
| `echo` | Outputs text provided by the user |
| `whoami` | Shows the current logged-in user |

---

## 📁 Interacting With the Filesystem

| Command | Full Meaning | Description |
|---|---|---|
| `ls` | Listing | Lists files and folders |
| `cd` | Change Directory | Moves between directories |
| `cat` | Concatenate | Displays file contents |
| `pwd` | Print Working Directory | Shows current directory location |

---

## 🔎 Searching for Files

### Using `find`

- Used to search for files by name

Example:

```bash
find -name passwords.txt

To find all .txt files:

find -name *.txt

🔍 Searching File Contents With grep
grep searches inside files for specific text or values

Example: Count entries in a file:

wc -l access.log

Example: Search for an IP address inside a log file:

grep "81.143.211.90" access.log
🔁 Recursive Search With grep
grep -R searches through files and subdirectories

Example:

grep -R "PRETTY_NAME" /etc/

This searches for PRETTY_NAME inside /etc/ and its subdirectories.

⚙️ Shell Operators
Operator	Description
&	Runs a command in the background
&&	Combines multiple commands in one line
>	Redirects output and overwrites existing content
>>	Redirects output and appends without overwriting

## 📸 Proof of Completion

![Linux Fundamentals Part 1](../assets/linux-fundamentals-part-1.jpg)

📌 Notes

This room helped me understand:

Basic Linux commands
How to move around the filesystem
How to search for files and file contents
How shell operators control command output
