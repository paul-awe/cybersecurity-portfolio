# Day 03–04 — Cabling and Ethernet Standards (Professor Messer)

## 🧠 What I learned

### Cabling

- Cable is fundamental to network communication  
- Even wireless communication still connects back to cables  
- You usually only set up cabling infrastructure once, so it must be done properly  

---

### Types of Cable

#### Twisted Pair Copper
- Two wires with equal and opposite signals (Transmit+, Transmit- / Receive+, Receive-)  
- Twisting reduces interference  
- Each pair has a different twist rate  

---

#### Coaxial Cable
- Multiple layers share a common axis  
- Example: RG-6 (used for TV and cable internet)  

- Twinax cable:
  - Has two inner conductors  
  - Used in 10 Gigabit Ethernet  
  - Limited to short distances (~5 meters)  

---

### Important Notes About Cables
- Cables themselves don’t determine speed  
- Data rate depends on signal encoding  

- Must follow manufacturing standards  
- Ethernet uses **IEEE 802.3 standards**  

- Cable categories:
  - Cat6, Cat7, etc  

---

### Plenum Cable
- Used in spaces above ceilings (plenum space)  
- Special fire-rated materials  

- Standard PVC = Polyvinyl Chloride  
- Fire-rated = FEP or low-smoke PVC  

- Less flexible and stricter bend limits  

---

## 🔌 Copper Connectors

### RJ11
- 6 positions, 2 conductors (6P2C)  
- Used for telephone and DSL  

---

### RJ45
- 8 positions, 8 conductors (8P8C)  
- Used for Ethernet  

---

### F-Connector
- Single copper conductor with threaded screw  
- Used for coaxial cable  
- Found in TV and cable internet (DOCSIS)  

---

### BNC Connector
- Bayonet Neill-Concelman  
- Twist-and-lock mechanism  
- Used in coaxial setups, video, and some WAN links  

---

## 🌐 Ethernet Standards

- Ethernet is the most common networking technology  
- Uses copper or fiber depending on the standard  

---

### IEEE 802.3
- Defines Ethernet standards  

Examples:
- 1000BASE-T → 1 Gbps over copper  
- 10GBASE-T → 10 Gbps over copper  
- 1000BASE-SX → 1 Gbps over fiber  

---

### Understanding Ethernet Naming

- Number = speed  
  - 1000 = 1000 Mbps (1 Gbps)  
  - 10G = 10 Gbps  

- BASE = baseband  
  - Single frequency using entire medium  

- Media type:
  - T = twisted pair  
  - F = fiber  
  - SX = short wavelength fiber  

---

## 📌 Key Takeaways

- Cabling is the backbone of all networks  
- Twisted pair is most common for Ethernet  
- Connectors determine how devices physically connect  
- Ethernet standards define speed, signal type, and media  
