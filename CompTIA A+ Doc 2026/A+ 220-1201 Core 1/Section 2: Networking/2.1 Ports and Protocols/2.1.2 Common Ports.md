### Common Port numbers
Common Port numbers are usefull to know to perform some types of firewall configuration and it often use TCP and UDP prt numbers.

### List of Common Ports:

**FTP (File Transfer Protocol)**
- It is a file transfer protocol used by many OS.  
- It is used to List the file available in a partcular directory.  
- It usualy required User name and Password or anonymous , generic login  
- We can Add, Delete, Change the file name and perform other adminstration funtions.
- [ ] TCP port 20  
- Used for Active data transfer.
- [ ] TCP port 21  
- Used for Administration or control port.  

**SSH (Secure Shell)**
- Its provides a encryption for commucation
- [ ] TCP port 22

**Telnet (Telecommuncations Network)**
- It work identical to SSH  
- It will not provide any encryption  
- It is no longer in use but there is any system is very old that does not support SSH it will use this port  
- [ ] TCP port 23

**SMTP (Simple Mail Transfer Protocol)**
- Used to send and email form one server to other
- [ ] TCP port 25

**DNS (Domain Name System)**
- It is used to open websites using readable domain names instead of IP addresses.
- [ ] UDP port 53

**DHCP (Dynamic Host Configuration Protocol)**
- It is a server or appliance that has a pool of available IP addresses. When a device connects to the network, it requests an IP address and configuration parameters from that pool.
- System administrators can also use DHCP to manually reserve IP addresses.
- [ ] UDP port 67
- [ ] UDP port 68

**HTTP (Hypertext Transfer Protocol)**
- It is used to connect to websites without encryption.
- [ ] TCP port 80

**HTTPS (Hypertext Transfer Protocol Secure)**
- It is the same as HTTP but with encryption (SSL/TLS).
- [ ] TCP port 443

**POP3 (Post Office Protocol Version 3)**
- It is used to download emails to your computer.
- It can be referenced using the LDAP protocol.
- [ ] TCP port 110

**IMAP or IMAP4 (Internet Message Access Protocol Version 4)**
- It is used for email access.
- It has a number of additional features not available in POP3 (like server-side storage and synchronization).
- [ ] TCP port 143

**SMB (Server Message Block)**
- It is also referred to as CIFS (Common Internet File System).
- It is used to communicate with different devices like Windows systems and printers.
- [ ] UDP port 137
- It uses NetBIOS Name Service which is similar to DNS.
- [ ] TCP port 139
- It uses NetBIOS Session Service.
- [ ] TCP port 445
- It supports direct SMB communication without NetBIOS.

**LDAP (Lightweight Directory Access Protocol)**
- It is used to manage and control a central directory database.
- It is also used in Active Directory infrastructure.
- [ ] TCP port 389

**LDAPS (Lightweight Directory Access Protocol Secure)**
- It is the secure version of LDAP using SSL/TLS encryption.
- [ ] TCP port 636

**RDP (Remote Desktop Protocol)**
- It is used to control and access Windows devices across a network.
- It also allows connection from macOS, Linux, Unix, iPhone, and other operating systems.
- [ ] TCP port 3389

- [ ] **END**
