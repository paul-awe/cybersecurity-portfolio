# TryHackMe Day 32–33: Virtualisation Basics

## Room Information

- **Room Name:** Virtualisation Basics
- **Platform:** TryHackMe
- **Status:** Completed ✅
- **Day:** 32–33
- **Difficulty:** Beginner
- **Topics Covered:** Virtualisation, Hypervisors, Virtual Machines (VMs), Containers, Docker, Hardware Utilization

---

## Overview

In this room, I learned how virtualization powers modern IT infrastructure by allowing multiple systems and applications to run on the same physical hardware.

Before virtualization, organizations often followed a simple rule:

> One Server = One Application

While this approach worked, it was expensive, inefficient, and difficult to scale. Virtualization was introduced to solve these problems by enabling multiple virtual systems to share the same physical hardware safely and efficiently.

This room also introduced hypervisors, virtual machines, containers, and Docker, all of which are essential technologies used in modern cloud computing, cybersecurity, and enterprise environments.

---

## Key Concepts Learned

### 1. What is Virtualisation?

Virtualisation is the process of creating virtual versions of computer systems that share physical hardware resources.

Instead of purchasing a separate server for every application, organizations can run multiple virtual machines on a single physical server.

### Benefits of Virtualisation

- Better hardware utilization
- Lower infrastructure costs
- Faster deployment
- Easier scalability
- Improved resource management
- Better testing environments

---

## Problems Before Virtualisation

Before virtualization, organizations faced several challenges:

### High Costs

Every service required its own physical server.

This increased:

- Hardware costs
- Electricity costs
- Cooling expenses
- Maintenance expenses
- Data center space requirements

### Low Hardware Utilization

Many servers only used:

```text
5% – 20%
```

of their available resources.

This resulted in wasted:

- CPU power
- Memory
- Storage

### Slow Deployment

Deploying a new server could take days or even weeks.

### Difficult Scaling

Growing applications often required purchasing additional hardware.

---

## Understanding the Building Analogy

The room used a building analogy to explain virtualization.

| Building Analogy | Virtualisation Component |
|-----------------|--------------------------|
| Building | Physical Server |
| Apartments | Virtual Machines |
| Tenants | Operating Systems / Applications |
| Building Manager | Hypervisor |

Just as multiple apartments can exist in one building, multiple virtual machines can run on one physical server.

Each VM remains isolated while sharing hardware resources.

---

## 2. Hypervisors

A Hypervisor is the software responsible for creating and managing virtual machines.

### Responsibilities of a Hypervisor

- Creates virtual machines
- Allocates CPU resources
- Allocates RAM resources
- Allocates storage resources
- Maintains isolation between VMs
- Starts and stops VMs
- Clones and manages VMs

The hypervisor acts as the layer between physical hardware and virtual machines.

---

## Types of Hypervisors

### Type 1 Hypervisor

Runs directly on physical hardware.

Characteristics:

- High performance
- Enterprise-grade
- Ideal for data centers
- Used in production environments

#### Common Uses

- Production Servers
- Database Servers
- Data Centers

---

### Type 2 Hypervisor

Runs inside an existing operating system.

Characteristics:

- Easy to install
- Great for learning
- Suitable for home labs
- Commonly used for testing

#### Common Uses

- Software Testing
- Kali Linux Labs
- Malware Analysis
- Learning Environments

---

## Examples of Type 2 Hypervisors

Popular tools include:

- Oracle VirtualBox
- VMware Workstation

These applications allow users to run multiple operating systems on a single computer.

Examples:

- Windows
- Linux
- Kali Linux
- Ubuntu

---

## 3. Virtual Machines (VMs)

A Virtual Machine (VM) is a virtual computer created by a hypervisor.

Although virtual, a VM behaves like a real computer.

### A VM Has:

- Virtual CPU
- Virtual RAM
- Virtual Storage
- Virtual Network Interface

### VM Advantages

- Isolation from other VMs
- Ability to run different operating systems
- Safe testing environments
- Easy deployment

If one VM crashes, the others continue running independently.

---

## Practical Cybersecurity Uses of VMs

### Malware Analysis

VMs provide a safe environment for testing suspicious files.

### Security Labs

Cybersecurity professionals often run:

- Kali Linux
- Windows
- Vulnerable Machines

inside isolated VMs.

### Operating System Testing

VMs allow testing of different operating systems without needing additional hardware.

---

## 4. Containers

Containers are lightweight environments designed to run applications.

Unlike VMs, containers do not include a full operating system.

Instead, they share the host system's kernel.

### Container Characteristics

- Lightweight
- Fast startup times
- Resource efficient
- Easily scalable
- Application-focused

Containers package:

- Application code
- Libraries
- Dependencies
- Runtime environments

This ensures applications work consistently across different systems.

---

## Containers vs Virtual Machines

| Feature | Virtual Machines | Containers |
|-----------|-----------------|------------|
| Includes OS | Yes | No |
| Resource Usage | Higher | Lower |
| Startup Speed | Slower | Faster |
| Isolation | Stronger | Lightweight |
| Scalability | Good | Excellent |

### Simple Comparison

VMs are like:

> Full apartments

Containers are like:

> Individual rooms inside an apartment

Both provide separation, but containers use fewer resources.

---

## 5. Docker

Docker is one of the most popular containerization platforms.

Docker makes it easier to:

- Build applications
- Package applications
- Deploy applications
- Run applications consistently

### Benefits of Docker

- Fast deployment
- Easy scalability
- Consistent environments
- Efficient resource usage

Docker is widely used in:

- Cloud Computing
- DevOps
- Software Development
- Cybersecurity Labs

---

## Virtualisation Architecture

A typical virtualization setup looks like this:

```text
Physical Server
      │
 Hypervisor
      │
 ├── Virtual Machine A
 │
 └── Virtual Machine B
        │
        ├── Container A
        └── Container B
```

This structure allows organizations to maximize hardware utilization while maintaining isolation between systems.

---

## Key Takeaways

- Virtualisation improves hardware efficiency.
- Hypervisors create and manage virtual machines.
- Type 1 hypervisors run directly on hardware.
- Type 2 hypervisors run inside an operating system.
- Virtual machines provide full operating system environments.
- Containers are lightweight alternatives to VMs.
- Docker simplifies container deployment.
- Virtualisation is a critical technology in modern IT and cybersecurity.

---

## Skills Gained

- Understanding virtualization concepts
- Understanding hardware utilization challenges
- Identifying hypervisor types
- Understanding VM architecture
- Understanding containerization
- Learning Docker fundamentals
- Understanding resource isolation
- Recognizing virtualization use cases in cybersecurity

---

## Completion Proof

Completed the **Virtualisation Basics** room on TryHackMe.

![Completion Badge](../assets/virtualisation-basics.jpg)

---

## Reflection

This room helped me understand how organizations maximize computing resources using virtualization technologies. Learning the differences between physical servers, virtual machines, hypervisors, and containers provided a strong foundation for future topics such as cloud computing, Docker, DevOps, malware analysis, and cybersecurity lab environments.

Virtualisation is one of the most important technologies behind modern data centers, cloud platforms, and cybersecurity testing environments, making it an essential skill for every cybersecurity professional.
