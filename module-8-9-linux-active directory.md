===============================================
MODULE 2 - LINUX FUNDAMENTALS
================================================

LINUX FUNDAMENTALS PART 1:

WHY LINUX:
- Free and open source
- Most servers run Linux
- All hacking tools run on Linux
- Kali Linux = hacking OS built on Linux

BASIC COMMANDS:
- echo = print text to screen
- whoami = show current username
- pwd = show current directory
- ls = list files
- cd = change directory
- cat = read file contents
- find = search for files
- grep = search inside files

INTERACTING WITH FILESYSTEM:
- ls -a = show hidden files
- ls -la = show detailed file list
- cd .. = go back one folder
- cd / = go to root directory
- cd ~ = go to home directory

CREATING AND EDITING FILES:
- touch file.txt = create empty file
- echo "text" > file.txt = create file with text
- echo "text" >> file.txt = add text to file
- nano file.txt = open text editor
- cp file.txt /destination = copy file
- mv file.txt /destination = move file
- rm file.txt = delete file
- mkdir folder = create folder

SEARCHING FOR FILES:
- find / -name file.txt = find file anywhere
- find /home -name *.txt = find all txt files
- grep "password" file.txt = find word in file
- grep -r "password" /home = search all files

FILE PERMISSIONS:
Format: rwxrwxrwx
- r = read (4)
- w = write (2)
- x = execute (1)
- Three groups: owner / group / others

Examples:
- 777 = everyone full access
- 755 = owner full, others read/execute
- 644 = owner read/write, others read only

Commands:
- chmod 777 file = give all permissions
- chmod +x file = make executable
- chown user file = change owner
- ls -la = see permissions

================================================
LINUX FUNDAMENTALS PART 2:

RUNNING COMMANDS AS ROOT:
- sudo = run as administrator
- sudo su = switch to root user
- su username = switch to another user

MANAGING SERVICES:
- systemctl start apache2 = start service
- systemctl stop apache2 = stop service
- systemctl enable apache2 = start on boot
- ps aux = see running processes
- kill [PID] = stop process

USEFUL OPERATORS:
- & = run in background
  Example: python3 script.py &
- && = run second command if first succeeds
  Example: cd folder && ls
- > = write output to file
  Example: ls > files.txt
- >> = append output to file
- | = pipe output to next command
  Example: cat file.txt | grep password

DOWNLOADING FILES:
- wget [URL] = download file
- curl [URL] = fetch webpage/file
  Example: wget https://example.com/file.txt

================================================
LINUX FUNDAMENTALS PART 3:

TEXT EDITORS IN LINUX:
- nano = beginner friendly
  nano file.txt
  Ctrl+S = save
  Ctrl+X = exit

- vim = advanced, faster
  vim file.txt
  i = insert mode
  Esc = exit insert mode
  :wq = save and quit
  :q! = quit without saving

GENERAL UTILITIES:
- wc -l file.txt = count lines in file
- sort file.txt = sort contents
- uniq file.txt = remove duplicates
- diff file1 file2 = compare two files

TERMINAL MULTIPLEXER:
- Use tmux or screen to run multiple terminals
- Useful for running multiple tools at once

HASHES:
- md5sum file = generate MD5 hash
- sha256sum file = generate SHA256 hash
- Used to verify file integrity

================================================
MODULE 3 - WINDOWS AND AD FUNDAMENTALS
================================================

WHY WINDOWS FOR CYBERSECURITY:
- 90% of corporate networks use Windows
- Active Directory = Windows based
- PNPT exam heavily tests Windows/AD
- Most internship environments use Windows

WINDOWS FUNDAMENTALS:

FILESYSTEM:
- C:\ = main drive
- C:\Windows = OS files
- C:\Users = user profiles
- C:\Program Files = installed programs
- C:\Windows\System32 = critical system files

IMPORTANT FILES/FOLDERS:
- C:\Windows\System32\drivers\etc\hosts
  = local DNS file
- C:\Users\[user]\Desktop = user desktop
- C:\Users\[user]\Documents = user documents

WINDOWS COMMANDS (CMD):
- dir = list files (like ls)
- cd = change directory
- cls = clear screen
- ipconfig = show IP address
- ipconfig /all = detailed network info
- ping = test connection
- type file.txt = read file (like cat)
- copy = copy file
- move = move file
- del = delete file
- mkdir = create folder
- tasklist = show running processes
- taskkill /PID [number] = stop process
- net user = list all users
- net user [username] = user details
- whoami = current user
- systeminfo = system information

POWERSHELL BASICS:
- More powerful than CMD
- Get-ChildItem = list files (like ls)
- Set-Location = change directory (like cd)
- Get-Content = read file (like cat)
- Get-Process = show processes
- Start-Process = start application
- Invoke-WebRequest = download files

================================================
ACTIVE DIRECTORY FUNDAMENTALS
================================================

WHAT IS ACTIVE DIRECTORY:
- Microsoft service managing users/computers
- Used in almost every company network
- Domain = collection of computers under AD
- Domain Controller = main server running AD

KEY COMPONENTS:

DOMAIN:
- Group of computers under same AD database
- Example: thm.local
- All computers share same policies and users

DOMAIN CONTROLLER (DC):
- Main server running Active Directory
- Stores all user accounts and passwords
- Manages authentication
- Most important server to compromise!

ORGANIZATIONAL UNITS (OUs):
- Folders for organizing users/computers
- Example: IT department, HR department
- Apply different policies to different OUs

USERS AND COMPUTERS:
- User accounts = people logging in
- Computer accounts = machines in domain
- Service accounts = running applications

GROUPS:
- Security Groups = control access permissions
- Distribution Groups = email lists
- Example: "Domain Admins" = highest privilege

GROUP POLICY (GPO):
- Rules applied to users and computers
- Example: force password complexity
- Example: disable USB drives
- Applied through SYSVOL network share
- Can apply to entire domain or specific OUs

AUTHENTICATION IN AD:

KERBEROS:
- Default authentication in Windows AD
- Uses tickets instead of passwords
- Process:
  1. User requests ticket from DC
  2. DC sends encrypted ticket
  3. User uses ticket to access resources
- Important for pentesting attacks!

NTLM:
- Older authentication method
- Still used as backup
- Less secure than Kerberos
- Can be cracked with tools

TREES, FORESTS AND TRUSTS:
- Tree = multiple domains sharing same namespace
  Example: thm.local + uk.thm.local
- Forest = collection of multiple trees
- Trust = allows users from one domain
  to access resources in another domain

================================================
SECURITY RELEVANCE
================================================

WHY AD IS IMPORTANT FOR PENTESTING:
- Compromising DC = owning entire network
- Common AD attacks:
  - Pass the Hash = use password hash directly
  - Kerberoasting = crack service account passwords
  - Golden Ticket = forge authentication tickets
  - BloodHound = map AD attack paths

TOOLS FOR AD PENTESTING:
- BloodHound = visualize AD attack paths
- Mimikatz = extract passwords from memory
- Impacket = AD attack toolkit
- CrackMapExec = AD enumeration

THESE ATTACKS ARE IN PNPT EXAM! ✅

================================================
REVISION QUESTIONS
================================================
1. What command shows current user in Linux?
2. What does chmod 777 do?
3. How do you search for a file in Linux?
4. What is a Domain Controller?
5. What is Group Policy used for?
6. What is Kerberos?
7. Difference between NTLM and Kerberos?
8. What is a Golden Ticket attack?
9. What is SYSVOL?
10. What command lists users in Windows?
================================================






