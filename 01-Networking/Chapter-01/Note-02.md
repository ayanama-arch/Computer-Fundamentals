### **Review Questions:**

1. **Identify the five components of a data communications system.**

   - **Message** (data being transmitted)
   - **Sender** (device sending the data)
   - **Receiver** (device receiving the data)
   - **Medium** (channel for data transmission)
   - **Protocol** (rules governing communication)

2. **What are the advantages of distributed processing?**

   - Better resource sharing
   - Higher reliability (fault tolerance)
   - Scalability and flexibility
   - Faster processing via parallelism

3. **What are the three criteria necessary for an effective and efficient network?**

   - **Performance** (measured by speed, response time)
   - **Reliability** (ability to recover from failures)
   - **Security** (protection against unauthorized access)

4. **What are the advantages of a multipoint connection over a point-to-point connection?**

   - More cost-effective (fewer cables and ports required)
   - Easier to add new devices
   - Efficient use of bandwidth

5. **What are the two types of line configuration?**

   - **Point-to-Point:** Dedicated link between two devices
   - **Multipoint:** Shared link among multiple devices

6. **Categorize the four basic topologies in terms of line configuration.**

   - **Mesh & Star:** Point-to-point connections
   - **Bus & Ring:** Multipoint connections

7. **What is the difference between half-duplex and full-duplex transmission modes?**

   - **Half-duplex:** Data flows in both directions, but one at a time (e.g., walkie-talkie).
   - **Full-duplex:** Data flows in both directions simultaneously (e.g., telephone).

8. **Name the four basic network topologies, and cite an advantage of each type.**

   - **Mesh:** High redundancy, reliable.
   - **Star:** Easy troubleshooting, failure of one device doesn’t affect others.
   - **Bus:** Easy to set up, cost-effective.
   - **Ring:** Efficient data transmission, no data collisions.

9. **For \( n \) devices in a network, what is the number of cable links required for mesh, ring, bus, and star topology?**

   - **Mesh:** \( n(n-1)/2 \)
   - **Ring:** \( n \)
   - **Bus:** 1 backbone cable
   - **Star:** \( n \) (each device connects to the central hub)

10. **What are some factors that determine whether a communication system is a LAN or WAN?**

    - **Geographical scope** (LAN is within a building, WAN spans regions)
    - **Data transfer speed** (LANs are faster)
    - **Ownership** (LANs are privately owned, WANs may be public)

11. **What is an internet? What is the Internet?**

    - **internet:** A general term for interconnected networks.
    - **Internet:** The global network using TCP/IP.

12. **Why are protocols needed?**

    - Ensure devices communicate efficiently and correctly.

13. **Why are standards needed?**
    - Ensure interoperability between different manufacturers.

---

### **Exercises:**

14. **What is the maximum number of characters or symbols that can be represented by Unicode?**

    - **1,114,112 characters** (2¹⁶ + 2²⁰ = 1,114,112).

15. **A color image uses 16 bits to represent a pixel. What is the maximum number of different colors that can be represented?**

    - **65,536 colors** (\( 2^{16} \)).

16. **Assume six devices are arranged in a mesh topology. How many cables are needed? How many ports are needed for each device?**

    - **Cables needed:** \( 6(6-1)/2 = 15 \)
    - **Ports per device:** \( 6-1 = 5 \)

17. **For each of the following networks, discuss the consequences if a connection fails.**  
    a. **Mesh topology:** No major impact due to redundancy.  
    b. **Star topology:** Only affected device loses connection.  
    c. **Bus topology:** Whole network fails if backbone is damaged.  
    d. **Ring topology:** Network may fail unless there’s redundancy.

18. **You have two computers connected by an Ethernet hub at home. Is this a LAN, a MAN, or a WAN? Explain.**

    - **LAN** (Local Area Network) because it covers a small area.

19. **In the ring topology, what happens if one of the stations is unplugged?**

    - **Breaks the loop, disrupting communication** unless there’s redundancy.

20. **In the bus topology, what happens if one of the stations is unplugged?**

    - Other devices remain connected unless the backbone is disturbed.

21. **Draw a hybrid topology with a star backbone and three ring networks.**  
    _(Diagram required: A star topology connecting three ring topologies as sub-networks.)_

22. **Draw a hybrid topology with a ring backbone and two bus networks.**  
    _(Diagram required: A ring topology as a backbone with two bus topologies branching out.)_

23. **Performance is inversely related to delay. Which applications are more sensitive to delay?**  
    a. **Sending an e-mail** → Less sensitive  
    b. **Copying a file** → Less sensitive  
    c. **Surfing the Internet** → More sensitive

24. **When a party makes a local telephone call, is this a point-to-point or multipoint connection? Explain.**

    - **Point-to-point**, as it connects two users directly.

25. **Compare the telephone network and the Internet. What are the similarities and differences?**
    - **Similarities:** Both use switching techniques.
    - **Differences:** Telephone uses circuit switching; the Internet uses packet switching.

---
