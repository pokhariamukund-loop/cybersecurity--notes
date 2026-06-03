# cybersecurity--notes
My cybersecurity learning journey
================================================
ROOM 1 - WHAT IS NETWORKING
================================================

DEFINITION:
Network = two or more devices connected 
to share data and resources

TYPES OF NETWORKS:
- LAN (Local Area Network)
  = Small area like home, office, school
  = Fast speed, limited range
  = Example: Your home WiFi

- WAN (Wide Area Network)
  = Large area covering cities/countries
  = Example: The Internet

- MAN (Metropolitan Area Network)
  = City level network

HOW DEVICES ARE IDENTIFIED:
- IP Address
  = Unique address for every device
  = Like a house address for your device
  = Example: 192.168.1.1
  = IPv4 = 4 numbers (192.168.1.1)
  = IPv6 = newer, longer format

- MAC Address
  = Permanent hardware address
  = Built into network card by manufacturer
  = Used within local network only

KEY DEVICES:
- Router = connects different networks together
- Switch = connects devices within same network
- Hub = old device, sends data to ALL devices
- Firewall = blocks unwanted traffic

PING:
- Tests if device is reachable on network
- Measures time for data to travel and return
- Command: ping google.com
- Lower ping = better connection

================================================
ROOM 2 - INTRO TO LAN
================================================

LAN TOPOLOGIES:

1. STAR TOPOLOGY
   = All devices connect to central switch
   = Most common in modern networks
   Pros: reliable, easy to add devices
   Cons: if central switch fails, all fail

2. BUS TOPOLOGY
   = All devices on single cable
   = Old style network
   Pros: cheap, easy to install
   Cons: one cable fails = everything fails

3. RING TOPOLOGY
   = Devices connected in a circle
   Pros: works well under heavy traffic
   Cons: one device fails = whole network fails

IMPORTANT CONCEPTS:

- DHCP (Dynamic Host Configuration Protocol)
  = Automatically assigns IP to devices
  = When you connect to WiFi, DHCP gives IP
  = Without DHCP you manually set IP

- ARP (Address Resolution Protocol)
  = Converts IP address to MAC address
  = Used when devices communicate on same network

- Default Gateway
  = IP address of your router
  = All traffic going outside passes through here
  = Example: 192.168.1.1

- Subnetting
  = Dividing large network into smaller ones
  = Makes networks more efficient and secure

PRIVATE IP RANGES:
- 192.168.x.x = Home/small office
- 10.x.x.x = Large organizations
- 172.16.x.x = Medium networks

================================================
ROOM 3 - OSI MODEL
================================================

WHAT IS OSI MODEL:
= Framework explaining how data travels in network
= 7 layers, each with specific job
= Helps understand and troubleshoot networks

MEMORY TRICK:
"Please Do Not Throw Sausage Pizza Away"

THE 7 LAYERS:

LAYER 7 - APPLICATION
= What user interacts with directly
= Examples: HTTP, HTTPS, FTP, DNS, SSH
= When you open browser = this layer

LAYER 6 - PRESENTATION
= Translates and formats data
= Handles encryption/decryption
= Examples: SSL, TLS, JPEG, MP3

LAYER 5 - SESSION
= Creates and manages connections
= Handles login sessions
= Examples: NetBIOS, RPC

LAYER 4 - TRANSPORT
= End-to-end communication
= Two protocols:

  TCP (Transmission Control Protocol):
  = Reliable, checks data arrived correctly
  = Slower but accurate
  = Used for: web, email, file download
  = 3-way handshake: SYN → SYN-ACK → ACK

  UDP (User Datagram Protocol):
  = Fast, does NOT check delivery
  = Used for: gaming, video calls, streaming

LAYER 3 - NETWORK
= Handles IP addresses
= Routing data between networks
= Devices: Routers
= Examples: IP, ICMP

LAYER 2 - DATA LINK
= Handles MAC addresses
= Data transfer between devices
= Devices: Switches
= Examples: Ethernet

LAYER 1 - PHYSICAL
= Actual hardware and cables
= Converts data to electrical signals
= Examples: Ethernet cables, WiFi signals

HOW DATA TRAVELS:
Sending = Layer 7 → Layer 1
Receiving = Layer 1 → Layer 7
