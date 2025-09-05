# Week 1 – Network Fundamentals

## 📖 Topics Covered
- What is Networking?
- Intro to LAN
- OSI Model
- Packets & Frames
- Extending Your Network

---

## 📝 Notes

### 1. What is Networking?

#### Task 1. What is Networking?

- Networks are connection of things. In terms of computing, it is thepractice of connecting computers so they can share resources and information.

     ##### Try Hack Me Questions
     - What is the key term for devices that are connected together?
     - Answer : Network 


#### Task 2. What is the Internet?

- The internet is a giant network consisting of small networks. Small networks are called private networks and connecting these small networks become public networks.
- The first iteration of the internet was within ARPANET in 1960 but it wasn't until 1989 that Tim Berners-Lee created the **World Wide Web** or Internet as we know.

     ##### Try Hack Me Questions
     - Who invented the World Wide Web?
     - Answer : Network

#### Task 3. Identifying Devices on a Network

- To maintain order, devices should be able to identify and be identifiable in a network.
- Like humans, devices also have fingerprints of their own. Two means of identification are IP address and MAC address
- An **Internet Protocol** or IP address identifies a device’s location on a network, while a **Media Access Control**  or MAC address uniquely identifies the device’s physical hardware.

     ##### IP Address
     
     - An IP address is divided into 4 octets. Private IP addresses are used for communication within a local network, while public IP addresses (assigned by your ISP) are used when communicating over the Internet.
     
     - 👉 IPv4 has about 4.3 billion addresses and is running out, while IPv6 provides a much larger address space and improved features.
     
     ##### MAC Address
     
     - Every device has a physical network interface with a unique MAC address, a 12-character hexadecimal identifier; the first half identifies the manufacturer, and the second half is unique to the device.
     
     💡 Trivia: Did you know that MAC addresses can be spoofed? A device can pretend to use another device’s MAC, which can trick firewalls or Wi-Fi networks that rely only on MAC filtering.
     
     ##### Try Hack Me Questions
     - What does the term "IP" stand for?
     - Answer : Internet Protocol
     
     - What is each section of an IP address called?
     - Answer : Octet
     
     - How many sections (in digits) does an IPv4 address have? 
     - Answer : 4
     
     - What does the term "MAC" stand for?
     - Answer : Media Access Control
     
     ##### Try Hack Me Labs - MAC Spoofing Simulation
     
     - The interactive labs simulate a hotel Wi-Fi network where you have to pay for the service. You'll note that the router is not allowing Bob's packets ( blue) to the TryHackMe website and is placing them in the bin, but Alice's packets (green) are going through fine because she has paid for Wi-Fi. Try changing Bob's MAC address to the same as Alice's to see what happens.
     
     📸 Results are saved in the [Screenshots](./Screenshots) folder.
     
     - Deploy the interactive lab using the "View Site" button and spoof your MAC address to access the site.  What is the flag?
     - Answer: THM{YOU_GOT_ON_TRYHACKME}
