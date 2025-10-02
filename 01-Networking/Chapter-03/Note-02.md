## **IP Addressing (IPv4)**

- **Total addresses:** 2³² = 4,294,967,296
- **Range:** 0.0.0.0 – 255.255.255.255
- **Structure:** IP = **Network Part + Host Part**

  - **Network Part:** identifies the network
  - **Host Part:** identifies devices on that network

---

## **IP Address Classes (Based on First Octet)**

| Class | First Octet Range | Network Bits | Host Bits | Total Hosts | Default Subnet Mask | Usage                   |
| ----- | ----------------- | ------------ | --------- | ----------- | ------------------- | ----------------------- |
| A     | 0–127             | 8            | 24        | 16,777,216  | 255.0.0.0           | Very large networks     |
| B     | 128–191           | 16           | 16        | 65,536      | 255.255.0.0         | Medium-sized networks   |
| C     | 192–223           | 24           | 8         | 256         | 255.255.255.0       | Small networks          |
| D     | 224–239           | —            | —         | —           | —                   | Multicast               |
| E     | 240–255           | —            | —         | —           | —                   | Experimental / Reserved |

---

### **Class A Details**

- **Format:** N.H.H.H (Network.Host.Host.Host)
- **Network bits:** 8
- **Host bits:** 24
- **Valid Address Range:** 1.0.0.0 – 126.255.255.255
- **Private Range:** 10.0.0.0 – 10.255.255.255
- **Default Subnet Mask:** 255.0.0.0
- **Reserved Addresses:**

  - 0.0.0.0 → Default route
  - 127.0.0.1 → Loopback / testing

> Class A is for **very large enterprise networks**.

### **Class B & C**

- **Class B:** Medium networks, default mask 255.255.0.0, range 128.0.0.0 – 191.255.255.255
- **Class C:** Small networks, default mask 255.255.255.0, range 192.0.0.0 – 223.255.255.255

### **Class D (Multicast)**

- **First Octet Range:** 224 – 239
- **Purpose:** Used for **multicast groups** (sending data to multiple devices simultaneously)
- **Network/Host Bits:** Not applicable in the usual sense
- **Total Hosts:** Not defined like A, B, or C
- **Default Subnet Mask:** Not used
- **Usage Example:** Video conferencing, streaming to multiple users, etc.

---

### **Class E (Experimental / Reserved)**

- **First Octet Range:** 240 – 255
- **Purpose:** Reserved for **experimental use or future purposes**
- **Network/Host Bits:** Not defined
- **Total Hosts:** Not applicable
- **Default Subnet Mask:** Not used
- **Usage:** Typically **not used in normal networks**; reserved for research/testing

---

💡 **Memory Tip:**
Think of Classes like this:

- **A, B, C → Hosts & Networks (usable)**
- **D → Multicast (special group communication)**
- **E → Experimental / future (never assigned to regular devices)**

---

## **Subnet Mask**

- A **32-bit number** that shows:

  1. Which part is **network**
  2. Which part is **host**

- **CIDR / Prefix Length:** `/n` shows number of **network bits**

  - Example: `10.0.0.0/8` → 8 network bits → Class A

---

## **Reserved IP Addresses**

| Address                       | Purpose                             |
| ----------------------------- | ----------------------------------- |
| 0.0.0.0                       | Default route / unspecified address |
| 127.0.0.1                     | Loopback / testing                  |
| 10.0.0.0 – 10.255.255.255     | Private Class A network             |
| 172.16.0.0 – 172.31.255.255   | Private Class B network             |
| 192.168.0.0 – 192.168.255.255 | Private Class C network             |
| 224.0.0.0 – 239.255.255.255   | Multicast addresses                 |
| 240.0.0.0 – 255.255.255.254   | Experimental / future use           |

---

✅ **Tips to Remember:**

- **Class A → Huge networks**, **Class B → Medium**, **Class C → Small**
- **Subnet mask** tells which part is network vs host
- **Reserved IPs** are for private, loopback, multicast, or experimental use

---
