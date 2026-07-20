# Linux Shells

Today I completed the **Linux Shells** room in the TryHackMe Cyber Security 101 learning path. This room introduced me to Linux shells, common shell commands, different shell types, and the basics of Bash scripting. I also learned how scripting can automate repetitive tasks using variables, loops, and conditional statements.

---

# 🧠 What I Learned

## What is a Linux Shell?

A Linux shell is a command-line interpreter that allows users to interact directly with the operating system. While most users rely on the graphical interface (GUI), the shell provides greater control, flexibility, and efficiency for performing tasks.

The shell accepts commands from the user, passes them to the operating system, and displays the output.

---

## Basic Linux Shell Commands

I reviewed several basic commands that are used frequently when working in a Linux terminal.

### Display the Current Directory

```bash
pwd
```

Shows the current working directory.

Example:

```text
/home/user
```

---

### Change Directory

```bash
cd Desktop
```

Moves into another directory.

---

### List Directory Contents

```bash
ls
```

Displays all files and folders in the current directory.

---

### Display File Contents

```bash
cat filename.txt
```

Displays the contents of a file.

---

### Search Inside a File

```bash
grep THM dictionary.txt
```

The `grep` command searches for words or patterns inside files and returns matching lines.

---

# Types of Linux Shells

Linux supports several different shells, each with its own strengths.

## Bash (Bourne Again Shell)

Bash is the default shell on most Linux distributions.

Features include:

- Widely supported
- Shell scripting
- Command history
- Tab completion
- Stable and reliable

Useful commands:

```bash
echo $SHELL
```

Shows the current shell.

```bash
cat /etc/shells
```

Lists all installed shells.

---

## Fish (Friendly Interactive Shell)

Fish focuses on ease of use.

Features:

- Beginner-friendly syntax
- Auto spell correction
- Syntax highlighting
- Command suggestions
- Themes and customization

---

## Zsh (Z Shell)

Zsh is a powerful and highly customizable shell.

Features:

- Advanced tab completion
- Plugin support
- Auto correction
- Excellent scripting capabilities
- Popular with frameworks like **Oh My Zsh**

You can switch shells temporarily using:

```bash
zsh
```

Or permanently using:

```bash
chsh -s /usr/bin/zsh
```

---

# Shell Scripting

A shell script is simply a file containing Linux commands that execute automatically.

Instead of typing the same commands repeatedly, they can be saved inside a script.

A Bash script normally has the extension:

```text
.sh
```

Example:

```bash
nano first_script.sh
```

---

## Shebang

Every Bash script should begin with a shebang.

```bash
#!/bin/bash
```

This tells Linux which interpreter should execute the script.

---

# Variables

Variables store values that can be reused throughout a script.

Example:

```bash
#!/bin/bash

echo "What's your name?"
read name

echo "Welcome, $name"
```

Here:

- `read` accepts user input.
- `name` stores the value.
- `$name` displays the stored value.

---

# Making Scripts Executable

Before running a script, it needs execution permission.

```bash
chmod +x first_script.sh
```

Then execute it with:

```bash
./first_script.sh
```

The `./` tells Linux to run the script from the current directory.

---

# Loops

Loops allow commands to be repeated automatically.

Example:

```bash
for i in {1..10}; do
    echo $i
done
```

This prints the numbers 1 through 10.

Loops are useful whenever the same task must be repeated multiple times.

---

# Conditional Statements

Conditional statements execute code only if a condition is true.

Example:

```bash
if [ "$name" = "Stewart" ]; then
    echo "Access Granted"
else
    echo "Access Denied"
fi
```

This checks the user's input before deciding what to display.

---

# Comments

Comments improve readability without affecting how the script runs.

Example:

```bash
# This is a comment
```

They help explain sections of code and make scripts easier to maintain.

---

# Locker Script

The final lab combined everything learned into one script.

The script used:

- Variables
- Loops
- Conditional statements

It asked the user for:

- Username
- Company Name
- PIN

Only if all three matched the expected values was access granted.

This demonstrated how shell scripting can automate authentication and decision-making.

---

# Key Takeaways

- Linux shells provide a powerful way to interact with the operating system.
- Bash is the most commonly used Linux shell.
- Fish is easier for beginners, while Zsh offers advanced customization.
- Basic commands like `pwd`, `cd`, `ls`, `cat`, and `grep` are essential.
- Shell scripts automate repetitive tasks.
- Variables store user input and reusable values.
- Loops repeat tasks efficiently.
- Conditional statements control program flow.
- Comments make scripts easier to understand and maintain.
- Scripts require execution permission before they can be run.

---

## 📸 Proof of Completion

![Linux Shells](../../assets/06-linux-shells.jpg)
