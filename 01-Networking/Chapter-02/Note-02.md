## TCP/Ip Protocol

## **TCP/IP Protocol Model Explained**

The **TCP/IP model** (Transmission Control Protocol/Internet Protocol) is the backbone of modern networking, including the Internet. It defines how data is transmitted between devices and is more practical than the **OSI model**.

### **Comparison with OSI Model**

| **Feature**      | **OSI Model (7 Layers)**                             | **TCP/IP Model (4 Layers)**       |
| ---------------- | ---------------------------------------------------- | --------------------------------- |
| **Developed By** | ISO (International Organization for Standardization) | DoD (Department of Defense, USA)  |
| **Architecture** | Theoretical (Conceptual)                             | Practical (Used in real networks) |
| **Layers**       | 7                                                    | 4                                 |
| **Used In**      | Academics & Reference                                | Internet & Real-world networking  |

---

## **Layers of the TCP/IP Model & Their Functions**

### **1. Network Interface Layer (Link Layer)**

**Equivalent to:** OSI **Physical + Data Link Layers**  
**Role:** Manages **hardware-level** transmission of data.

**Functions:**

- Defines how data is **physically sent over the network**.
- Uses **MAC addresses** to identify devices.
- Performs **error detection & correction** at the link level.
- Determines how devices access the physical medium (e.g., Ethernet, Wi-Fi).

**Example Protocols:**

- **Ethernet** – Wired connections.
- **Wi-Fi (802.11)** – Wireless communication.
- **PPP (Point-to-Point Protocol)** – Direct connections.
- **MAC (Media Access Control)** – Device addressing.

---

### **2. Internet Layer**

**Equivalent to:** OSI **Network Layer**  
**Role:** Handles **logical addressing, routing, and packet forwarding**.

**Functions:**

- Assigns and manages **IP addresses**.
- **Routes packets** from source to destination across networks.
- Provides **error reporting** and diagnostics.

**Example Protocols:**

- **IP (Internet Protocol)** – Assigns IP addresses and routes packets.
  - **IPv4** – Standard 32-bit addressing (e.g., 192.168.1.1).
  - **IPv6** – Newer 128-bit addressing.
- **ICMP (Internet Control Message Protocol)** – Error handling (e.g., Ping command).
- **ARP (Address Resolution Protocol)** – Resolves IP addresses to MAC addresses.
- **RARP (Reverse ARP)** – Resolves MAC addresses to IP addresses.

---

### **3. Transport Layer**

**Equivalent to:** OSI **Transport Layer**  
**Role:** Ensures **end-to-end communication** between devices.

**Functions:**

- **Segmentation & reassembly** of data.
- **Error detection & correction** for reliable communication.
- **Flow control** – Prevents sender from overwhelming the receiver.
- **Multiplexing** – Allows multiple applications to use the same network connection.

**Example Protocols:**

- **TCP (Transmission Control Protocol)** – Reliable, connection-oriented communication.
  - Ensures **data arrives completely and in order**.
  - Uses **ACK (Acknowledgment)** and **Retransmission**.
  - Example: Web browsing, email, file transfer.
- **UDP (User Datagram Protocol)** – Fast, connectionless communication.
  - No guarantee of delivery, order, or error correction.
  - Example: Live streaming, VoIP calls, online gaming.

---

### **4. Application Layer**

**Equivalent to:** OSI **Application + Presentation + Session Layers**  
**Role:** Provides **services & applications** for user interaction.

**Functions:**

- Manages **network services** such as email, file transfer, and web browsing.
- Handles **data representation, encoding, and encryption**.
- Establishes **sessions** between applications.

**Example Protocols:**

- **HTTP/HTTPS** – Web browsing.
- **FTP (File Transfer Protocol)** – File sharing.
- **SMTP, POP3, IMAP** – Email transmission.
- **DNS (Domain Name System)** – Converts domain names (e.g., google.com) to IP addresses.
- **SNMP (Simple Network Management Protocol)** – Network monitoring.
- **Telnet/SSH** – Remote access.

---

## **Comparison: OSI vs. TCP/IP Layers**

| **OSI Model** (7 Layers) | **TCP/IP Model** (4 Layers) | **Example Protocols** |
| ------------------------ | --------------------------- | --------------------- |
| **Application (7)**      | **Application**             | HTTP, FTP, SMTP, DNS  |
| **Presentation (6)**     | **Application**             | SSL/TLS, JPEG, ASCII  |
| **Session (5)**          | **Application**             | NetBIOS, RPC          |
| **Transport (4)**        | **Transport**               | TCP, UDP              |
| **Network (3)**          | **Internet**                | IP, ICMP, ARP         |
| **Data Link (2)**        | **Network Interface**       | Ethernet, Wi-Fi       |
| **Physical (1)**         | **Network Interface**       | Cables, Fiber         |

---

## **How TCP/IP Works in Real Life (Example Scenario)**

Imagine you are loading a webpage **(www.example.com)** on your browser.

1. **Application Layer**

   - Your browser sends an **HTTP request** to the web server.
   - DNS translates **www.example.com** into an IP address.

2. **Transport Layer**

   - TCP divides the request into small **segments**.
   - It ensures reliable delivery by numbering each segment.

3. **Internet Layer**

   - IP assigns a **source and destination IP address** to each packet.
   - ICMP checks for errors during transmission.

4. **Network Interface Layer**
   - Ethernet or Wi-Fi **physically transmits** the packets.
   - The router forwards packets to the destination.

At the **server side**, the process is reversed, and the **webpage is sent back** to your browser!

---

## **Key Differences Between OSI and TCP/IP Models**

| **Feature**          | **OSI Model** (7 Layers)                | **TCP/IP Model** (4 Layers)                         |
| -------------------- | --------------------------------------- | --------------------------------------------------- |
| **Design**           | Theoretical model                       | Practical model                                     |
| **Number of Layers** | 7                                       | 4                                                   |
| **Used In**          | Reference model for research            | Internet & real-world networks                      |
| **Reliability**      | Clear separation of functionalities     | More flexible & efficient                           |
| **Security**         | Built-in encryption at different layers | Security handled at the application layer (SSL/TLS) |

---

## **Final Thoughts**

- The **OSI model** is useful for understanding **networking concepts**.
- The **TCP/IP model** is the **real-world implementation** used on the Internet.
- **TCP ensures reliability**, while **UDP prioritizes speed**.

---

### TCP Three-Way Handshake (Connection Establishment)

**Purpose:** Establish a reliable TCP connection and synchronize sequence numbers between client and server.

**Steps:**

1. **SYN (Client → Server)**

   - Client requests connection.
   - Sets SYN flag, chooses initial sequence number (e.g., `seq=100`).

2. **SYN-ACK (Server → Client)**

   - Server acknowledges client’s SYN (`ack = client_seq + 1`).
   - Sends its own SYN with server sequence number (e.g., `seq=500`).

3. **ACK (Client → Server)**

   - Client acknowledges server’s SYN (`ack = server_seq + 1`).
   - Connection is now established; data transfer can begin.

**Key Points:**

- Ensures both sides agree on sequence numbers.
- Prevents old or duplicate connections.
- Enables reliable, ordered data transmission.

**Analogy:** Phone call handshake: “Hello → Yes, ready → Got it, start talking.”

---
