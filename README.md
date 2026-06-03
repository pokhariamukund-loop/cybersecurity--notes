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
Sending = Layer7 - Layer1
Receiving = Layer1 - Layer7

================================================
ROOM 4 - PACKETS & FRAMES
================================================

WHAT ARE PACKETS:
- Data is broken into smaller pieces = packets
- Each packet travels independently across network
- Reassembled at destination
- Like sending a book page by page

PACKET STRUCTURE:
- Header = source IP, destination IP, packet number
- Payload = actual data being sent
- Footer = error checking information

WHY PACKETS:
- More efficient than sending all data at once
- If one packet lost = only resend that packet
- Multiple packets can take different routes

THREE WAY HANDSHAKE (TCP):
- How two devices establish connection
- Step 1: SYN = "I want to connect"
- Step 2: SYN-ACK = "OK I accept"
- Step 3: ACK = "Great lets communicate"
- Used every time you visit a website

CLOSING CONNECTION (TCP):
- Step 1: FIN = "I want to close"
- Step 2: ACK = "OK"
- Step 3: FIN = "I'm closing too"
- Step 4: ACK = "Done"

UDP PACKETS:
- No handshake needed
- Just sends packets without checking
- Faster but less reliable
- Used for gaming, video streaming

PORTS:
- Like doors on a device
- Different services use different ports
- Port 80 = HTTP (websites)
- Port 443 = HTTPS (secure websites)
- Port 22 = SSH (remote access)
- Port 21 = FTP (file transfer)
- Port 25 = SMTP (email)
- Range: 0-65535

================================================
ROOM 5 - EXTENDING YOUR NETWORK
================================================

INTRODUCTION TO PORT FORWARDING:
- Allows devices outside network to access
  services inside your network
- Example: hosting a website from home
- Router forwards specific port to specific device
- Without port forwarding = outside cannot reach
  inside your network

FIREWALLS:
- Security device that monitors network traffic
- Allows or blocks traffic based on rules
- Like a security guard checking everyone

Types of Firewalls:
- Stateless Firewall
  = Checks each packet individually
  = Uses fixed rules
  = Fast but less smart

- Stateful Firewall
  = Tracks entire connection
  = Understands context
  = Smarter and more secure

Firewall Rules:
- Based on: IP address, port, protocol
- Can block specific countries, IPs, ports
- Example rule: Block all traffic on port 23

VPN (Virtual Private Network):
- Creates encrypted tunnel between devices
- Makes it look like you're in different location
- Hides your real IP address
- Bypasses geographic restrictions
- Used by: businesses, privacy conscious users

How VPN Works:
- Your device → encrypted tunnel → VPN server
  → internet
- Websites see VPN server IP not your IP

Types of VPN:
- PPP = basic authentication
- PPTP = allows data to travel outside network
- IPSec = encrypts data using IP framework

NETWORK DEVICES SUMMARY:
- Router = connects networks, finds best path
- Switch = connects devices, uses MAC addresses
- Firewall = filters traffic, security
- VPN = encrypted private connection
- Proxy = acts as middleman for requests

================================================
SECURITY RELEVANCE
================================================

IMPORTANT FOR CYBERSECURITY:
- Packets = understanding how data travels
- Port scanning = finding open ports (Nmap tool)
- Firewalls = understanding what to bypass
- VPN = used by attackers to hide identity
- Port forwarding = exposing services to internet

COMMON ATTACKS:
- Port Scanning = attacker finds open ports
- Firewall Bypass = attacker evades firewall rules
- Packet Sniffing = capturing packets on network
- SYN Flood = sending many SYN packets = DoS attack

IMPORTANT PORTS TO MEMORIZE:
- 21 = FTP
- 22 = SSH
- 23 = Telnet (insecure)
- 25 = SMTP (email)
- 80 = HTTP
- 443 = HTTPS
- 3389 = RDP (Remote Desktop)
- 8080 = Alternative HTTP

# Module 3 - How The Web Works
# TryHackMe Pre-Security - Mukund Pokharia

================================================
ROOM 1 - DNS IN DETAIL
================================================

WHAT IS DNS:
- DNS = Domain Name System
- Converts website names to IP addresses
- Like a phonebook for the internet
- Example: google.com = 142.250.181.46
- Without DNS you would type IP addresses
  to visit websites

WHY DNS EXISTS:
- Humans remember names not numbers
- Easier to remember google.com than IP address
- DNS does the translation automatically

================================================
DNS HIERARCHY
================================================

ROOT DOMAIN:
- Top of DNS hierarchy
- Represented by a dot (.)
- Managed by ICANN

TOP LEVEL DOMAIN (TLD):
- Last part of domain name
- Example: .com, .org, .net, .in, .uk
- Two types:
  gTLD = generic (. com, .org, .edu)
  ccTLD = country code (.in, .uk, .us)

SECOND LEVEL DOMAIN:
- Main part of domain name
- Example: google in google.com
- Maximum 63 characters
- Only letters, numbers, hyphens

SUBDOMAIN:
- Part before main domain
- Example: admin in admin.google.com
- Example: mail in mail.google.com
- Can have multiple subdomains

FULL EXAMPLE:
admin.google.com
- admin = subdomain
- google = second level domain
- .com = top level domain

================================================
DNS RECORD TYPES
================================================

A RECORD:
- Maps domain to IPv4 address
- Example: google.com → 142.250.181.46
- Most common record type

AAAA RECORD:
- Maps domain to IPv6 address
- Newer version of A record

CNAME RECORD:
- Maps domain to another domain name
- Example: shop.website.com → shopify.com
- Used for subdomains

MX RECORD:
- Mail Exchange record
- Tells where to send emails for domain
- Example: gmail.com MX → mail servers

TXT RECORD:
- Stores text information
- Used for: email verification, domain ownership
- Used by: Google, spam filters

================================================
HOW DNS WORKS STEP BY STEP
================================================

When you type google.com:

STEP 1 - Check Local Cache
- Your computer checks if it knows the IP already
- Recently visited sites are cached
- If found = use cached IP (fast!)

STEP 2 - Check Recursive DNS Server
- Usually provided by your ISP
- Has large cache of DNS records
- If found = return IP address

STEP 3 - Check Root DNS Server
- If recursive server doesn't know
- Root server directs to TLD server
- Example: directs to .com TLD server

STEP 4 - Check TLD Server
- Handles specific TLD (.com, .org etc)
- Directs to Authoritative DNS server

STEP 5 - Authoritative DNS Server
- Final authority for domain
- Has actual DNS records
- Returns correct IP address

STEP 6 - Response
- IP address sent back to your computer
- Cached locally for future use
- Browser connects to IP address

================================================
DNS TTL (Time To Live)
================================================

- Number telling how long to cache DNS record
- Measured in seconds
- High TTL = cached longer (less DNS requests)
- Low TTL = expires faster (more up to date)
- Example: TTL 3600 = cached for 1 hour

================================================
SECURITY RELEVANCE
================================================

DNS ATTACKS:
- DNS Spoofing/Poisoning
  = Attacker puts fake DNS records
  = Redirects users to fake websites
  = Used for phishing attacks

- DNS Enumeration
  = Finding all subdomains of a target
  = Used in penetration testing
  = Tool: dnsenum, dnsrecon

- DNS Hijacking
  = Attacker changes DNS settings
  = Redirects all traffic

IMPORTANT FOR PENTESTING:
- Finding subdomains = finding attack surface
- Hidden subdomains = forgotten/vulnerable systems
- MX records reveal email providers
- TXT records reveal services used

USEFUL COMMANDS:
# Look up DNS records
nslookup google.com

# Detailed DNS lookup (Linux)
dig google.com

# Find all record types
dig google.com ANY

# Find MX records
dig google.com MX
Sending = Layer 7 → Layer 1
Receiving = Layer 1 → Layer 7
