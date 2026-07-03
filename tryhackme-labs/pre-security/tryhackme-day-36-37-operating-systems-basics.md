# TryHackMe Day 36–37: Operating Systems Basics

## Room Information

- **Room Name:** Operating Systems Basics
- **Platform:** TryHackMe
- **Status:** Completed ✅
- **Day:** 36–37
- **Difficulty:** Beginner
- **Topics Covered:** Operating Systems, Kernel Space, User Space, Process Management, Memory Management, GUI, CLI, Operating System Types

---

## Overview

In this room, I learned the fundamentals of Operating Systems (OS) and how they serve as the bridge between users, applications, and computer hardware.

An Operating System is the core software that coordinates everything happening on a computer. Without an OS, applications would need direct access to hardware resources, which would create conflicts, instability, and security issues.

This room introduced the responsibilities of an operating system, privilege separation, security mechanisms, graphical and command-line interfaces, and the various operating systems used across desktops, servers, mobile devices, embedded systems, and cloud environments.

---

# What is an Operating System?

An Operating System (OS) is the software responsible for managing:

- Hardware resources
- Running applications
- User interactions
- Security controls
- File systems
- Memory allocation

The OS sits between:

```text
User
↓
Applications
↓
Operating System
↓
Hardware
```

The OS acts as the central coordinator that ensures all components work together efficiently.

---

## Airport Analogy

The room used a useful airport analogy:

### Hardware

Represents:

- Runways
- Airplanes
- Radar systems
- Fuel systems

These are the physical resources.

---

### Applications

Represent:

- Airlines
- Passengers

Applications constantly request resources and services.

---

### Operating System

Represents:

- Air Traffic Control

The OS:

- Coordinates activity
- Allocates resources
- Prevents conflicts
- Maintains stability

Just as aircraft cannot safely operate without air traffic control, applications cannot efficiently operate without an operating system.

---

# Why Operating Systems Are Important

Without an operating system:

- Applications would compete directly for hardware resources.
- Programs could overwrite each other's memory.
- Devices would be difficult to manage.
- Security would be nearly impossible.

The OS solves these problems through centralized management and coordination.

---

# System Privilege Layers

Modern operating systems separate permissions into different layers.

This design improves:

- Stability
- Security
- Reliability

---

## Kernel Space

Kernel Space is the highly privileged area of the operating system.

Characteristics:

- Direct access to hardware
- Full system privileges
- Controls CPU access
- Controls memory access
- Controls storage devices
- Controls hardware communication

The kernel is the core component of the operating system.

---

## User Space

User Space is where normal applications operate.

Examples:

- Web browsers
- Media players
- Office applications
- Games

Applications in user space cannot directly access hardware.

Instead, they request services from the kernel through:

```text
System Calls
```

---

## Why Privilege Separation Matters

Benefits include:

- Improved stability
- Better security
- Reduced system crashes
- Protection from malicious software

If one application crashes, it is less likely to affect the entire operating system.

---

# Core Responsibilities of an Operating System

Every operating system performs several critical tasks.

---

## 1. Process Management

Process management controls running applications.

Responsibilities:

- Creating processes
- Scheduling processes
- Prioritizing processes
- Terminating processes

Example:

Running:

- A web browser
- Music player
- Chat application

simultaneously without freezing the computer.

---

## 2. Memory Management

The OS controls how RAM is allocated.

Responsibilities:

- Allocating memory
- Protecting memory
- Reclaiming memory
- Managing virtual memory

Benefits:

- Stability
- Isolation
- Efficient resource usage

Each application receives its own protected memory space.

---

## 3. File System Management

The OS organizes and manages files.

Responsibilities:

- Creating files
- Organizing folders
- Managing permissions
- Tracking metadata

Examples:

- Saving documents
- Creating folders
- Setting files as read-only

---

## 4. User Management

Operating systems support multiple users.

Responsibilities:

- User accounts
- Authentication
- Permissions
- Access control

Example:

Logging into a computer with a password.

The OS ensures users only access authorized resources.

---

## 5. Device Management

The OS manages hardware devices through drivers.

Examples:

- Printers
- Keyboards
- Mice
- External drives
- Audio devices

Benefits:

- Simplified hardware support
- Consistent interfaces
- Automatic device detection

---

# Operating System Security

Operating systems provide several security mechanisms before additional security software is installed.

---

## Authentication

Verifies user identity through:

- Passwords
- PINs
- Biometrics

Examples:

- Fingerprints
- Facial recognition

---

## Permissions

Controls what users and applications can:

- Read
- Write
- Execute

Permissions reduce unauthorized access.

---

## Isolation

Processes operate within separate environments.

Benefits:

- Prevents interference
- Improves stability
- Enhances security

---

## System Protection

The OS protects critical system files and settings from unauthorized changes.

This helps maintain system integrity.

---

# Operating System Interfaces

Users interact with operating systems through interfaces.

Two primary methods exist:

---

## Graphical User Interface (GUI)

The GUI uses visual elements such as:

- Windows
- Icons
- Menus
- Buttons

Examples:

- Windows Desktop
- macOS Interface
- Android Home Screen

Benefits:

- Easy to learn
- User-friendly
- Visual navigation

---

## Command-Line Interface (CLI)

The CLI uses text commands.

Users type commands directly into a terminal.

Examples:

```bash
dir
ls
cd
pwd
```

Benefits:

- Greater control
- Faster administration
- Automation capabilities
- Precision

CLI skills are essential for cybersecurity professionals.

---

# Operating System Categories

Different environments require different operating systems.

---

## Desktop Operating Systems

Primary Use:

- Personal computing
- Gaming
- Productivity
- Content creation

Characteristics:

- Rich graphical interface
- Multitasking
- User-focused

Examples:

- Windows
- macOS
- Linux

---

## Server Operating Systems

Primary Use:

- Web hosting
- Databases
- Cloud services

Characteristics:

- Stability
- High uptime
- Multi-user support
- Remote administration

Examples:

- Windows Server
- Ubuntu Server
- Red Hat Enterprise Linux

---

## Mobile Operating Systems

Primary Use:

- Smartphones
- Tablets

Characteristics:

- Touch interfaces
- Power efficiency
- Mobile app ecosystems

Examples:

- Android
- iOS

---

## Embedded Operating Systems

Primary Use:

- Smart TVs
- Routers
- Cars
- IoT Devices

Characteristics:

- Lightweight
- Specialized functions
- Limited hardware requirements

Examples:

- OpenWrt
- Ubuntu Core
- Yocto Project

---

## Virtual and Cloud Operating Systems

Primary Use:

- Virtual Machines
- Cloud Infrastructure
- Containers

Characteristics:

- Lightweight
- Scalable
- Rapid deployment

Examples:

- Amazon Linux
- Ubuntu LTS
- Rocky Linux

---

# Real-World Operating System Families

---

## Windows

Most widely used desktop operating system.

Popular Versions:

- Windows 10
- Windows 11

Server Versions:

- Server 2016
- Server 2019
- Server 2022
- Server 2025

---

## macOS

Apple's desktop operating system.

Known For:

- User experience
- Ecosystem integration
- Stability

Recent Versions:

- Sonoma
- Sequoia
- Tahoe

---

## Linux

Open-source operating system family.

Popular Distributions:

- Ubuntu
- Debian
- Fedora

Server Distributions:

- Ubuntu Server
- Debian
- CentOS
- Red Hat

Linux powers most web servers worldwide.

---

## Unix

Enterprise-focused operating systems.

Examples:

- IBM AIX
- Oracle Solaris

Commonly used in:

- Finance
- Government
- Telecommunications

---

## Android

Most widely used mobile operating system.

Runs on:

- Smartphones
- Tablets
- Smart devices

---

## iOS

Apple's mobile operating system.

Runs on:

- iPhones
- iPads

Known for:

- Security
- Performance
- Ecosystem integration

---

# Why So Many Operating Systems Exist

Different devices require different capabilities.

Examples:

### Laptops

Require:

- Ease of use
- Multitasking
- Productivity tools

### Servers

Require:

- Stability
- Security
- Continuous operation

### Mobile Devices

Require:

- Battery efficiency
- Touch interfaces
- Hardware integration

### Embedded Systems

Require:

- Small footprints
- Specialized functionality

No single operating system can perfectly satisfy every requirement.

---

# Key Terminology

## Operating System (OS)

Software that manages hardware, applications, and system resources.

---

## Kernel Space

Privileged area of the OS with direct hardware access.

---

## User Space

Area where normal applications run.

---

## Graphical User Interface (GUI)

Visual interface using icons, windows, and menus.

---

## Command-Line Interface (CLI)

Text-based interface using commands.

---

# Key Takeaways

- Operating systems coordinate hardware and software.
- Kernel space has direct hardware access.
- User space isolates applications for safety.
- Process management controls running applications.
- Memory management allocates and protects RAM.
- Operating systems provide authentication and permissions.
- GUI and CLI provide different ways to interact with a system.
- Different operating systems are designed for different environments.

---

# Skills Gained

- Understanding operating system architecture
- Understanding privilege separation
- Learning kernel and user space concepts
- Understanding process management
- Understanding memory management
- Learning OS security fundamentals
- Understanding GUI and CLI interaction
- Recognizing major operating system families

---

## Reflection

This room provided a strong foundation for understanding how operating systems function behind the scenes. I learned how operating systems manage hardware, applications, memory, users, devices, and security while maintaining system stability. Understanding these concepts is essential for cybersecurity because every security tool, application, and service ultimately relies on the operating system to function securely and efficiently.

---

**Platform:** TryHackMe  
**Room:** Operating Systems Basics  
**Completed:** Day 36–37 of My Cybersecurity Learning Journey
