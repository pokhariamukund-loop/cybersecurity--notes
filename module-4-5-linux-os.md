================================================
MODULE 4 - LINUX FUNDAMENTALS
================================================

WHY LINUX FOR CYBERSECURITY:
- Most servers run Linux
- All hacking tools run on Linux
- Kali Linux = hacking OS
- TryHackMe machines use Linux
- eJPT and PNPT exams use Linux

BASIC LINUX COMMANDS:

FILE NAVIGATION:
- pwd = print working directory (where am I?)
- ls = list files in current directory
- ls -la = list all files with details
- cd [folder] = change directory
- cd .. = go back one directory
- cd ~ = go to home directory

FILE OPERATIONS:
- touch [file] = create new file
- mkdir [folder] = create new folder
- cp [file] [destination] = copy file
- mv [file] [destination] = move/rename file
- rm [file] = delete file
- rm -rf [folder] = delete folder

READING FILES:
- cat [file] = display file contents
- less [file] = display file page by page
- head [file] = show first 10 lines
- tail [file] = show last 10 lines
- grep [word] [file] = search for word in file

FILE PERMISSIONS:
- Every file has permissions
- r = read, w = write, x = execute
- Three groups: owner, group, others
- Example: rwxr-xr-x
- chmod = change permissions
- chmod 777 [file] = give all permissions
- chown = change file owner

USERS AND GROUPS:
- whoami = show current user
- id = show user ID and groups
- sudo = run command as admin
- su [user] = switch user
- passwd = change password
- adduser = add new user

PROCESS MANAGEMENT:
- ps = show running processes
- ps aux = show all processes
- top = live process monitor
- kill [PID] = stop a process
- & = run process in background

NETWORKING COMMANDS:
- ifconfig = show network interfaces
- ip addr = show IP addresses
- ping [IP] = test connection
- netstat = show network connections
- curl [URL] = download webpage
- wget [URL] = download file

SEARCHING:
- find / -name [file] = find file location
- grep -r [word] [directory] = search in all files
- locate [file] = quick file search

TEXT EDITING:
- nano [file] = simple text editor
- vim [file] = advanced text editor
- echo "text" > file = write text to file
- echo "text" >> file = add text to file

================================================
MODULE 5 - OPERATING SYSTEMS BASICS
================================================

WHAT IS AN OPERATING SYSTEM:
- Software managing computer hardware
- Interface between user and hardware
- Examples: Windows, Linux, MacOS

TYPES OF OS:
- Windows = most common desktop OS
- Linux = most common server OS
- MacOS = Apple computers
- Android/iOS = mobile OS

WINDOWS VS LINUX:

| | Windows | Linux |
|---|---|---|
| Cost | Paid | Free |
| Security | Less secure | More secure |
| Hacking tools | Limited | Hundreds |
| Server use | Some | Most |
| Command line | CMD/PowerShell | Bash/Terminal |

================================================
LINUX CLI BASICS
================================================

FILE SYSTEM STRUCTURE:
- / = root directory (top of everything)
- /home = user home directories
- /etc = configuration files
- /var = variable files, logs
- /tmp = temporary files
- /bin = basic commands
- /usr = user programs
- /root = root user home directory

IMPORTANT FILES:
- /etc/passwd = user accounts list
- /etc/shadow = encrypted passwords
- /etc/hosts = local DNS entries
- /var/log = system log files
- ~/.bashrc = user bash configuration

PIPES AND REDIRECTION:
- | (pipe) = send output to next command
  Example: cat file.txt | grep "password"
- > = write output to file
  Example: ls > files.txt
- >> = append output to file
- < = read input from file

USEFUL COMBINATIONS:
- cat /etc/passwd | grep root
  (find root user in passwd file)
- ps aux | grep apache
  (find apache process)
- find / -name "*.txt" 2>/dev/null
  (find all txt files, hide errors)

================================================
WINDOWS CLI BASICS
================================================

BASIC WINDOWS COMMANDS:
- dir = list files (like ls)
- cd = change directory
- cls = clear screen
- ipconfig = show IP address
- ping = test connection
- type [file] = show file contents
- copy = copy file
- del = delete file
- mkdir = create folder
- tasklist = show running processes
- taskkill = stop process
- net user = manage users
- whoami = show current user

WINDOWS POWERSHELL:
- More powerful than CMD
- Get-ChildItem = list files
- Set-Location = change directory
- Get-Content = read file
- Get-Process = show processes

================================================
OPERATING SYSTEM SECURITY
================================================

KEY SECURITY CONCEPTS:

USER ACCOUNTS:
- Standard user = limited permissions
- Administrator = full control
- Principle of least privilege = give minimum
  permissions needed
- Root (Linux) = highest privilege

AUTHENTICATION:
- Something you know = password, PIN
- Something you have = phone, token
- Something you are = fingerprint, face
- MFA = Multi Factor Authentication
  (uses 2 or more of above)

ENCRYPTION:
- Converts data to unreadable format
- Symmetric = same key to encrypt/decrypt
- Asymmetric = public key encrypts,
  private key decrypts
- HTTPS uses asymmetric encryption

COMMON VULNERABILITIES:
- Unpatched software = outdated systems
- Weak passwords = easy to crack
- Misconfiguration = wrong settings
- No MFA = easy account takeover

SECURITY TOOLS:
- Antivirus = detects malware
- Firewall = filters network traffic
- IDS/IPS = detects/prevents intrusions
- SIEM = monitors security events

================================================
SECURITY RELEVANCE
================================================

LINUX SKILLS FOR PENTESTING:
- Navigate target system after exploitation
- Read sensitive files (/etc/passwd, /etc/shadow)
- Find files with find command
- Check running processes
- Escalate privileges

WINDOWS SKILLS FOR PENTESTING:
- Most corporate systems run Windows
- Active Directory = Windows based
- Important for PNPT exam!

================================================
REVISION QUESTIONS
================================================
1. What command shows current directory?
2. How do you list all files including hidden?
3. What is chmod used for?
4. What does /etc/passwd contain?
5. Difference between > and >>?
6. What is sudo?
7. What is principle of least privilege?
8. What is MFA?
9. What does grep do?
10. What command finds a file in Linux?
