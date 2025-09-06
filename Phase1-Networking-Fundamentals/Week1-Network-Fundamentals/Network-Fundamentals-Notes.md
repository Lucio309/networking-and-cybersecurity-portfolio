# Phase 1 - Network Fundamentals

## 📖 Topics Covered
- Week 1: What is Networking?
- Week 2: Intro to LAN
- Week 3: OSI Model
- Week 4: Packets & Frames
- Week 5: Extending Your Network

---

## 📝 Notes

### Week 1. What is Networking?

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

#### Task 4. Ping (ICMP)

- Ping is one of the fundamental network tools which uses the **Internet Control Message Protocol** packets to check performance of connection between devices.

- Ping sends a test message to another device and measures how long it takes to get a reply. The syntax to do a simple ping is **ping IP address or website URL**.

     ##### Try Hack Me Questions
     - What protocol does ping use?
     - Answer : ICMP

     - What is the syntax to ping 10.10.10.10?
     - Answer : ping 10.10.10.10
 
     - What flag do you get when you ping 8.8.8.8?
     - Answer : THM{I_PINGED_THE_SERVER}
    
 📸 Results are saved in the [Screenshots](./Screenshots) folder.


### Week 2. Intro to LAN

#### Task 1. Introducing LAN Topologies

- In networking, "topology" refers to the layout or structure of how devices are connected in a network.

  ##### Different Topologies

     - **Star Topology** - All devices connect individually to a central device like a switch or hub, making it reliable and easy to expand. While it can be more expensive due to extra cabling and equipment, it allows for straightforward addition of new devices. However, if the central device fails, the entire network can go down, and larger networks may require more maintenance and troubleshooting.
     
       <img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/40b817bf-7bfd-4cc3-8b1c-9ff09ea60a8c" />
     
     - **Bus Topology** - All devices connect along a single backbone cable, making it simple and cost-effective to set up. However, because all data travels on the same cable, the network can become slow and bottlenecked with heavy use, and troubleshooting is difficult. Additionally, the backbone cable is a single point of failure—if it breaks, the entire network goes down.

          <img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/44a3bcce-cf75-4119-97c1-285ad0d6e9e3" />
     
     - **Ring Topology** - Devices are connected in a loop, sending data around the ring until it reaches its destination, which reduces cabling and reliance on central hardware. While troubleshooting is easier due to the single data direction, this can also slow communication since data may pass through many devices before reaching its target. However, a failure in any device or cable breaks the entire network.
     
          <img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/7eba7dd6-d05d-4e0d-a28a-9fee561bd261" />

##### Switches

- A switch is a device that helps connect many gadgets (like computers and printers) in a network using Ethernet cables. 

- It keeps track of which device is connected to each port and sends data only to the intended device, unlike a hub that broadcasts data to all devices.

<img width="1058" height="606" alt="image" src="https://github.com/user-attachments/assets/09cb7812-a3d1-441c-87ca-96b459a1b6fa" />

- Switches and routers can connect to each other to create multiple paths for data, making the network more reliable. If one path fails, data can take another route, preventing downtime. This may slow the network slightly but keeps it running smoothly.

##### Routers

- A router connects different networks and helps send data between them. Routing is the process of finding the best path for the data to travel so it reaches the right place.

<img width="1077" height="357" alt="image" src="https://github.com/user-attachments/assets/032fb4ff-49c0-4343-b132-15064b606480"/>


##### Try Hack Me Questions

- What does LAN stand for?
- Answer: Local Area Network

- What is the verb given to the job that routers perform?
- Answer: Routing

- What device is used to centrally connect multiple devices on the local network and transmit data to the correct location?
- Answer: Switch

- What topology is cost-efficient to set up?
- Answer: Bus Topology

- What topology is expensive to set up and maintain?
-Answer: Star Topology

-Complete the interactive lab attached to this task. What is the flag given at the end?
-Answer: THM{TOPOLOGY_FLAWS}
 
##### Try Hack Me Labs - Topology Flaws

Attached to this task is an interactive practical featuring the discussed LAN topologies. Learn about the various ways in which they are vulnerable to breaking. Break the LAN topologies to retrieve the flag.


#### Task 2. A Primer on Subnetting
#### Task 3. ARP
#### Task 4. DHCP




