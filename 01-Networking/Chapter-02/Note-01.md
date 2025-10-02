# OSI Model

The **OSI (Open Systems Interconnection) model** is a conceptual framework that standardizes how different networking systems communicate. It consists of **7 layers**, each with a specific role in handling data transmission across a network.

---

## **1. Physical Layer (Layer 1)**

### **Role**: Defines the physical connection between devices and transmits raw data (bits) over a medium.

### **Functions**:

- Manages **electrical, optical, or radio signals**.
- Specifies **cables, connectors, and transmission media** (e.g., fiber optics, Ethernet cables).
- Ensures bit synchronization.

### **Example**:

- Ethernet cables, fiber optics, and wireless signals (Wi-Fi, Bluetooth).

---

## **2. Data Link Layer (Layer 2)**

### **Role**: Ensures reliable data transfer over the physical link by handling framing, error detection, and MAC addressing.

### **Functions**:

- Divides data into **frames**.
- Uses **MAC (Media Access Control) addresses** to identify devices.
- Handles **error detection and correction** (e.g., CRC - Cyclic Redundancy Check).
- Controls **access to the transmission medium** (e.g., CSMA/CD in Ethernet).

### **Example**:

- Ethernet (MAC addresses), Wi-Fi (802.11).

---

## **3. Network Layer (Layer 3)**

### **Role**: Determines the best path for data to travel between devices and handles logical addressing (IP addresses).

### **Functions**:

- **Routing**: Finds the best path for packets to reach their destination.
- **Logical Addressing**: Assigns **IP addresses** to devices.
- **Packet Switching & Forwarding**.

### **Example**:

- **IP (Internet Protocol)** – IPv4, IPv6.
- **Routers** – Forward packets based on IP addresses.

---

## **4. Transport Layer (Layer 4)**

### **Role**: Ensures end-to-end communication, reliability, and data integrity between applications.

### **Functions**:

- **Segmentation & Reassembly**: Breaks data into smaller **segments** and reassembles them at the destination.
- **Error Detection & Correction**.
- **Flow Control**: Prevents sender from overwhelming the receiver.
- **Multiplexing**: Allows multiple applications to communicate over a single network connection.

### **Example**:

- **TCP (Transmission Control Protocol)** – Reliable, connection-oriented.
- **UDP (User Datagram Protocol)** – Fast, connectionless.

---

## **5. Session Layer (Layer 5)**

### **Role**: Manages and controls sessions between applications.

### **Functions**:

- **Session Establishment & Termination**.
- **Synchronization**: Ensures data is properly organized.
- **Maintains communication states**.

### **Example**:

- **Remote Desktop Protocol (RDP)** – Maintains a session for remote access.
- **VoIP Calls** – Keeps a session active during a call.

---

## **6. Presentation Layer (Layer 6)**

### **Role**: Converts data into a format that the application layer can understand.

### **Functions**:

- **Data Encryption & Decryption** (SSL/TLS for secure communication).
- **Data Compression** (reducing data size for faster transmission).
- **Data Encoding & Translation** (e.g., ASCII to Unicode).

### **Example**:

- **SSL/TLS (Secure Sockets Layer / Transport Layer Security)** – Encrypts HTTPS websites.
- **JPEG, MP3, MP4** – Compresses media files.

---

## **7. Application Layer (Layer 7)**

### **Role**: Provides network services directly to applications.

### **Functions**:

- **User Interface for Network Services** (e.g., browsers, email clients).
- **Handles Application-Specific Protocols**.
- **Interacts with software applications**.

### **Example**:

- **HTTP/HTTPS** – Web browsing.
- **SMTP, IMAP, POP3** – Email.
- **FTP (File Transfer Protocol)** – File transfer.
- **DNS (Domain Name System)** – Resolves domain names to IP addresses.

---

### **Summary of the OSI Model**

| **Layer**           | **Role**                            | **Example Protocols/Technologies** |
| ------------------- | ----------------------------------- | ---------------------------------- |
| **7. Application**  | User interaction with network       | HTTP, FTP, DNS, SMTP, IMAP         |
| **6. Presentation** | Data translation & encryption       | SSL/TLS, JPEG, ASCII, Unicode      |
| **5. Session**      | Manages communication sessions      | RDP, SIP, NetBIOS                  |
| **4. Transport**    | End-to-end connection & reliability | TCP, UDP                           |
| **3. Network**      | Routing & logical addressing        | IP, ICMP, ARP, OSPF                |
| **2. Data Link**    | Framing, MAC addressing             | Ethernet, Wi-Fi, PPP               |
| **1. Physical**     | Transmission of raw bits            | Cables, Fiber, Wireless            |

Each layer interacts with the layer directly above and below it, making the network communication process structured and efficient.

## 1. What is a Protocol Data Unit (PDU)?

Think of PDUs as **packets of data** at each layer of the network stack.

- Each layer adds its own header (sometimes a footer) to the data it receives from the layer above.
- That “package with extra info” is a PDU.

In simple terms:

> **PDU = Data + Layer-Specific Header (and sometimes trailer)**

The header contains control info that the layer needs: addresses, sequence numbers, flags, etc.

---

### 2. PDU at Each OSI Layer

1. **Application Layer (Layer 7)**

   - PDU name: **Data**
   - Content: actual message the user wants to send (email text, file, HTTP request).
   - Example: `"GET /index.html HTTP/1.1"`

2. **Presentation Layer (Layer 6)**

   - PDU: **Data** (often still called Data)
   - Content: formatted/encoded/encrypted version of the application data.
   - Adds encoding, compression, or encryption headers (if needed).

3. **Session Layer (Layer 5)**

   - PDU: **Data**
   - Content: session control info, e.g., checkpoints, session IDs.
   - Example: in SSL/TLS handshake, session keys and state info are part of PDU.

4. **Transport Layer (Layer 4)**

   - PDU name: **Segment** (TCP) or **Datagram** (UDP)
   - Content: Adds source and destination ports, sequence numbers, flags.
   - Example (TCP segment):

     ```
     [TCP Header: SrcPort=5000, DestPort=80, Seq=1001] + [Data]
     ```

5. **Network Layer (Layer 3)**

   - PDU name: **Packet**
   - Content: Adds source and destination IP addresses, routing info.
   - Example (IP packet):

     ```
     [IP Header: SrcIP=192.168.1.2, DestIP=8.8.8.8] + [Segment]
     ```

6. **Data Link Layer (Layer 2)**

   - PDU name: **Frame**
   - Content: Adds MAC addresses, error checking (CRC), and control info.
   - Example (Ethernet frame):

     ```
     [Ethernet Header: SrcMAC, DestMAC] + [IP Packet] + [CRC]
     ```

7. **Physical Layer (Layer 1)**

   - PDU name: **Bits**
   - Content: Raw electrical, optical, or radio signals that represent the frame.
   - No headers here — just 1s and 0s moving through the medium.

---

### 3. How Data Travels

Think of **wrapping a gift** multiple times:

- App layer: your gift (message).
- Transport: wraps it in a box (segment).
- Network: puts it in a shipping envelope (packet).
- Data Link: adds a label and padding (frame).
- Physical: sends the bits over wire/wireless.

At the receiver: **unwrap layer by layer** until the original message is delivered to the application.

---

### Quick PDU Table

| OSI Layer        | PDU              | Added Info / Header        |
| ---------------- | ---------------- | -------------------------- |
| Application (7)  | Data             | App-specific info          |
| Presentation (6) | Data             | Encoding/compression info  |
| Session (5)      | Data             | Session control info       |
| Transport (4)    | Segment/Datagram | Port numbers, seq#, flags  |
| Network (3)      | Packet           | IP addresses, routing info |
| Data Link (2)    | Frame            | MAC addresses, CRC         |
| Physical (1)     | Bits             | Electrical/optical signals |

---
