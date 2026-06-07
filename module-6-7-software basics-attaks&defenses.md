================================================
MODULE 6 - SOFTWARE BASICS
================================================

TYPES OF SOFTWARE:
- System Software = OS, drivers, utilities
- Application Software = browsers, games, apps
- Malware = malicious software

HOW SOFTWARE WORKS:
- Source code = human readable code
- Compiler = converts to machine code
- Executable = runnable program (.exe)

SOFTWARE VULNERABILITIES:
- Bug = unintended error in code
- Vulnerability = bug that can be exploited
- Exploit = taking advantage of vulnerability
- Patch = fix for vulnerability
- Zero Day = vulnerability unknown to vendor

SOFTWARE UPDATES:
- Always update software!
- Updates fix security vulnerabilities
- Unpatched software = easy target for hackers
- Example: WannaCry ransomware exploited
  unpatched Windows systems

TYPES OF MALWARE:
- Virus = attaches to files, spreads itself
- Worm = spreads across network automatically
- Trojan = disguised as legitimate software
- Ransomware = encrypts files, demands payment
- Spyware = secretly monitors your activity
- Adware = shows unwanted advertisements
- Keylogger = records your keystrokes
- Rootkit = hides deep in system, hard to detect
- Botnet = network of infected computers

HOW MALWARE SPREADS:
- Phishing emails with attachments
- Malicious websites
- USB drives
- Software downloads
- Network vulnerabilities

================================================
MODULE 7 - ATTACKS AND DEFENSES
================================================

THE CIA TRIAD:
Most important concept in cybersecurity!

C = CONFIDENTIALITY
= Only authorized people can access data
= Example: encryption, passwords, access control
= Attack against it: data breach, eavesdropping

I = INTEGRITY
= Data is accurate and not tampered with
= Example: checksums, digital signatures, hashing
= Attack against it: man in middle, data tampering

A = AVAILABILITY
= Systems and data accessible when needed
= Example: backups, redundancy, DDoS protection
= Attack against it: DDoS attack, ransomware

REMEMBER: CIA Triad = foundation of ALL security!

================================================
CRYPTOGRAPHY CONCEPTS
================================================

WHAT IS CRYPTOGRAPHY:
- Science of securing information
- Converts readable data to unreadable format
- Only authorized parties can read it

KEY TERMS:
- Plaintext = original readable data
- Ciphertext = encrypted unreadable data
- Encryption = converting plaintext to ciphertext
- Decryption = converting ciphertext to plaintext
- Key = secret used to encrypt/decrypt
- Algorithm = method used for encryption

TYPES OF ENCRYPTION:

SYMMETRIC ENCRYPTION:
- Same key used to encrypt AND decrypt
- Fast but key sharing is risky
- Examples: AES, DES
- Problem: how to securely share the key?

ASYMMETRIC ENCRYPTION:
- Two keys: Public key and Private key
- Public key = encrypts (anyone can have it)
- Private key = decrypts (only you have it)
- Slower but more secure
- Examples: RSA, ECC
- Used in: HTTPS, SSH, email encryption

HASHING:
- One way conversion (cannot reverse)
- Same input = always same output
- Used for: passwords, file verification
- Examples: MD5, SHA-1, SHA-256
- Password hashing = stores hash not password

DIGITAL SIGNATURES:
- Proves document came from specific person
- Uses asymmetric encryption
- Provides: authentication + integrity

COMMON ENCRYPTION USES:
- HTTPS = encrypts web traffic
- SSH = encrypts remote connections
- VPN = encrypts all network traffic
- WhatsApp = end to end encryption

================================================
BECOME A HACKER (Offensive Security)
================================================

TYPES OF HACKERS:
- White Hat = ethical hacker, has permission
- Black Hat = criminal hacker, no permission
- Grey Hat = in between, sometimes breaks rules

PENETRATION TESTING:
- Authorized simulation of cyber attacks
- Find vulnerabilities before real hackers do
- Companies pay pentesters to hack them
- Must have written permission!

PENTESTING STAGES:
1. Reconnaissance = gather information about target
2. Scanning = find open ports, services
3. Exploitation = attack vulnerabilities found
4. Post Exploitation = what can you do after?
5. Reporting = document findings, suggest fixes

COMMON ATTACK TYPES:
- Phishing = fake emails to steal credentials
- Brute Force = trying many passwords
- SQL Injection = attacking databases
- XSS = injecting JavaScript into websites
- MITM = intercepting communications
- Social Engineering = manipulating people
- DDoS = overwhelming server with traffic

RECONNAISSANCE TYPES:
- Passive = gathering info without touching target
  (Google, social media, WHOIS)
- Active = directly interacting with target
  (port scanning, ping)

================================================
BECOME A DEFENDER (Defensive Security)
================================================

SOC (Security Operations Center):
- Team monitoring security 24/7
- Detect and respond to attacks
- Uses SIEM tools
- Entry level job: SOC Analyst

DEFENSIVE TOOLS:
- Firewall = filters network traffic
- IDS = Intrusion Detection System
  (alerts when attack detected)
- IPS = Intrusion Prevention System
  (blocks attacks automatically)
- SIEM = Security Information Event Management
  (collects and analyzes security logs)
- Antivirus = detects and removes malware
- EDR = Endpoint Detection and Response

INCIDENT RESPONSE STEPS:
1. Preparation = have plan ready
2. Identification = detect the incident
3. Containment = stop it spreading
4. Eradication = remove the threat
5. Recovery = restore systems
6. Lessons Learned = improve for future

DIGITAL FORENSICS:
- Investigating cyber crimes
- Collecting digital evidence
- Chain of custody = evidence handling
- Tools: Autopsy, FTK, Volatility

THREAT INTELLIGENCE:
- Understanding attacker tactics
- IOC = Indicators of Compromise
  (signs that system was hacked)
- TTPs = Tactics, Techniques, Procedures

================================================
SECURITY FRAMEWORKS
================================================

NIST FRAMEWORK:
- Identify → Protect → Detect → Respond → Recover

OWASP TOP 10:
Most common web vulnerabilities:
1. Broken Access Control
2. Cryptographic Failures
3. Injection (SQL, XSS)
4. Insecure Design
5. Security Misconfiguration
6. Vulnerable Components
7. Authentication Failures
8. Software Integrity Failures
9. Logging Failures
10. Server Side Request Forgery

IMPORTANT FOR:
- Bug bounty hunting
- Web application pentesting
- Security+ exam
- Every cybersecurity interview!

================================================
REVISION QUESTIONS
================================================
1. What is CIA Triad? Explain each part
2. Difference between symmetric and asymmetric?
3. What is hashing used for?
4. What are the 5 pentesting stages?
5. Difference between IDS and IPS?
6. What is a zero day vulnerability?
7. What is social engineering?
8. What is OWASP Top 10?
9. Difference between white/black/grey hat?
10. What is a SOC analyst?
================================================





