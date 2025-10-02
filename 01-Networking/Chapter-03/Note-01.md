## **IP Addressing (IPv4)**

- **Length:** 32 bits (binary)

- **Structure:** Two main parts

  1. **Network Part** – identifies the network
  2. **Host Part** – identifies devices within that network

- **Octets:**

  - 32-bit address divided into **4 octets** for simplicity
  - **1 octet = 8 bits**
  - Range of each octet: **0–255**

- **Representation:** Dotted Decimal Notation

  - Example: `192.168.1.1`
  - Easier to read than binary

- **Summary:**

  > IP = 32-bit binary → split into 4 octets → converted to decimal → dotted format (0–255 per octet)

---

## **Major Internet Organizations (Authority Hierarchy)**

### **1. ICANN (Internet Corporation for Assigned Names and Numbers)**

- **Role:** Global coordination of DNS, IP addresses, and protocol identifiers
- **Scope:** Highest-level authority

### **2. IANA (Internet Assigned Numbers Authority)**

- **Role:** Operates under ICANN; manages IP address blocks, protocol numbers, and DNS root zones
- **Scope:** Global, operational authority

### **3. IETF (Internet Engineering Task Force)**

- **Role:** Develops Internet standards & protocols (TCP/IP, HTTP, etc.)
- **Scope:** Standards are voluntary but widely adopted

### **4. W3C (World Wide Web Consortium)**

- **Role:** Standardizes Web technologies (HTML, CSS, XML)
- **Focus:** Web interoperability

### **5. ISOC (Internet Society)**

- **Role:** Advocates for open Internet development, policy, and global Internet growth
- **Focus:** Policy & advocacy rather than technical enforcement

### **6. RIRs (Regional Internet Registries)**

- **Examples:** ARIN, RIPE NCC, APNIC, LACNIC, AFRINIC
- **Role:** Allocates IP addresses & AS numbers within regions
- **Scope:** Regional authority, under ICANN/IANA

---

## **Authority Table (Biggest → Smallest)**

| Rank | Organization | Role                                          |
| ---- | ------------ | --------------------------------------------- |
| 1    | ICANN        | Global coordination of DNS & IP addresses     |
| 2    | IANA         | Manages IPs, protocol numbers, DNS root zones |
| 3    | IETF         | Develops Internet standards & protocols       |
| 4    | W3C          | Web standards & interoperability              |
| 5    | ISOC         | Global Internet advocacy & policy             |
| 6    | RIRs         | Regional IP allocation & management           |

---

✅ **Tip to Remember:**
Think **ICANN → IANA → IETF/W3C → ISOC → RIRs** as descending layers of **authority** from global technical control to regional management.

---
