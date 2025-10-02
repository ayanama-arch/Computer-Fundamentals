### **MAC Address (Media Access Control Address)**

**Definition:**
A MAC address is a **unique hardware identifier** assigned to a network interface card (NIC) for communication on the **data link layer (Layer 2)** of the OSI model.

---

### **Key Points:**

1. **Format:**

   - 48 bits (6 bytes), usually written as: `00:1A:2B:3C:4D:5E` or `00-1A-2B-3C-4D-5E`.
   - First 3 bytes = **OUI (Organizationally Unique Identifier)** → identifies the manufacturer.
   - Last 3 bytes = **NIC-specific serial number** → unique per device.

2. **Type:**

   - **Unicast:** Identifies a single device.
   - **Broadcast:** `FF:FF:FF:FF:FF:FF` → all devices in the network.
   - **Multicast:** Certain addresses for a group of devices (specific range).

3. **Function:**

   - Identifies devices **locally** on a network segment.
   - Used by **Ethernet, Wi-Fi, and other Layer 2 protocols** for delivering frames.
   - Works with **switches** to forward frames correctly.

4. **Permanence:**

   - Usually **burned into NIC** (hardware), called **physical or burned-in address**.
   - Can be **changed (spoofed)** via software in most modern devices.

5. **Relation with IP:**

   - IP address = logical, network-layer identifier (Layer 3).
   - MAC address = physical, link-layer identifier (Layer 2).
   - ARP (Address Resolution Protocol) maps IP → MAC for local delivery.

---

### **Example in Linux/Windows**

- **Linux:** `ifconfig` or `ip link show`
- **Windows:** `ipconfig /all` → “Physical Address”

**Example MAC:** `00:1B:44:11:3A:B7`

---
