# **Types of IP Addresses**

IP addresses can be classified in **three different ways**:

---

## **1. Based on Configuration**

| Type           | Description                                                                                                                                           |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Static IP**  | Manually assigned to a device. Stays the same unless changed manually. Ideal for servers, network devices, and situations where a fixed IP is needed. |
| **Dynamic IP** | Automatically assigned by a DHCP server. Can change over time. Commonly used for home networks and client devices.                                    |

---

## **2. Based on Protocol / Availability**

| Type     | Description                                                                                                                     |
| -------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **IPv4** | 32-bit address (e.g., 192.168.1.1). Limited number of addresses (~4.3 billion). Most widely used.                               |
| **IPv6** | 128-bit address (e.g., 2001:0db8:85a3::8a2e:0370:7334). Designed to solve IPv4 address exhaustion. Vastly larger address space. |

---

## **3. Based on Network Type**

| Type           | Description                                                                                                   |
| -------------- | ------------------------------------------------------------------------------------------------------------- |
| **Public IP**  | Globally unique, assigned by ISPs. Accessible from the Internet.                                              |
| **Private IP** | Used within local networks. Not routable on the Internet. Examples: 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 |
| **LAN IP**     | Assigned to devices within a Local Area Network. Usually private IPs.                                         |
| **WAN IP**     | Assigned to devices to connect to the wider Internet. Usually public IPs.                                     |

---

### **Private IP Address Ranges (Commonly Used)**

| Class | Range                         |
| ----- | ----------------------------- |
| A     | 10.0.0.0 – 10.255.255.255     |
| B     | 172.16.0.0 – 172.31.255.255   |
| C     | 192.168.0.0 – 192.168.255.255 |

**Tip:** Private IPs are used inside networks; public IPs are visible to the Internet. NAT (Network Address Translation) is used to map private IPs to public IPs.

---
