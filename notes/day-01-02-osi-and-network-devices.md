# Day 01 – OSI Model & Network Devices

## 🧠 Topic 1: OSI Model (Open Systems Interconnection)

The OSI model explains how data moves from one device to another across a network.  
It consists of **7 layers**, each with a specific function.

### 🔹 Layer 1 – Physical Layer
- Deals with hardware (cables, connectors, signals)
- Handles transmission of raw bits

### 🔹 Layer 2 – Data Link Layer
- Responsible for local network communication
- Uses **MAC addresses**
- Includes Data Link Control (DLC) protocols

### 🔹 Layer 3 – Network Layer
- Responsible for routing data between networks
- Uses **IP addresses**

### 🔹 Layer 4 – Transport Layer
- Ensures proper delivery of data
- Think of it like a **post office**
- Protocols:
  - TCP (reliable)
  - UDP (faster, no guarantee)

### 🔹 Layer 5 – Session Layer
- Manages communication sessions
- Handles start, stop, and restart of connections
- Includes tunneling and control protocols

### 🔹 Layer 6 – Presentation Layer
- Handles data formatting and encryption
- Includes:
  - Character encoding
  - Encryption/decryption
- Often combined with Application layer

### 🔹 Layer 7 – Application Layer
- What users interact with directly
- Protocols include:
  - HTTP
  - FTP
  - DNS
  - POP3

---

## 🌐 Topic 2: Network Devices

Network devices help forward and manage traffic across networks.

### 🔹 Router (Layer 3)
- Routes traffic between different networks (IP-based)
- Connects LAN and WAN
- Can use fiber or copper connections

### 🔹 Switch (Layer 2)
- Forwards traffic within a local network
- Uses MAC addresses

### 🔹 Firewall
- Filters traffic based on rules
- Can filter by port, IP, or application

### 🔹 Load Balancer
- Distributes traffic across multiple servers
- Prevents downtime and overload
- Features:
  - TCP offload
  - SSL offload
  - Caching

### 🔹 Proxy Server
- Acts as an intermediary between user and internet
- Functions:
  - Caching
  - Access control
  - URL filtering
  - Content scanning

---

## 💾 Storage Systems

### 🔹 NAS (Network Attached Storage)
- File-level storage
- Works like a shared network folder

### 🔹 SAN (Storage Area Network)
- Block-level storage
- High-speed network
- Used for databases and enterprise systems

---

## 📡 Wireless & Network Expansion

### 🔹 Access Point (AP)
- Connects wireless devices to a wired network
- Extends Wi-Fi coverage

### 🔹 Router vs Access Point
- Router → manages traffic, IP assignment, security  
- AP → provides wireless access only

### 🔹 Wireless LAN Controller
- Centralized management of multiple access points
- Handles:
  - Deployment
  - Monitoring
  - Security

---

## 🌍 Networking Technologies

### 🔹 Content Delivery Network (CDN)
- Uses distributed servers
- Delivers content from nearest location
- Improves speed and performance

### 🔹 Virtual Private Network (VPN)
- Secures data over public networks
- Encrypts and decrypts traffic

### 🔹 Quality of Service (QoS)
- Prioritizes important traffic
- Controls bandwidth and data flow

---

## ⏱️ Key Concept

### 🔹 Time To Live (TTL)
- Limits how long data can exist in a network
- Prevents infinite loops
- In DNS: measured in seconds
- In networking: counts number of hops

---

## 📌 What I Learned
- The OSI model explains how data travels across a network
- Different devices operate at different OSI layers
- Network performance and security depend on proper device configuration
- Technologies like VPN, CDN, and QoS improve security and efficiency

---

## ❓ What I Didn’t Fully Understand Yet
- Subnetting (to revisit later)
- Deep differences between TCP and UDP in real scenarios
