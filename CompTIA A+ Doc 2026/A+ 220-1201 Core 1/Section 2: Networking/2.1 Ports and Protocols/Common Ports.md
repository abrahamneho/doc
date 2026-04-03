## Common Port numbers

Common Port numbers are usefull to know to perform some types of firewall configuration and it often use TCP and UDP prt numbers.

## List of Common Ports:

### FTP (File Transfer Protocol)

TCP port 20  
- Used for Active data transfer.

TCP port 21  
- Used for Administration or control port.  
- It is a file transfer protocol used by many OS.  
- It is used to List the file available in a partcular directory.  
- It usualy required User name and Password or anonymous , generic login  
- We can Add, Delete, Change the file name and perform other adminstration funtions.

### SSH (Secure Shell)

TCP port 22  
- Its provides a encryption for commucation

### Telnet (Telecommuncations Network)

TCP port 23  
- It work identical to SSH  
- It will not provide any encryption  
- It is no longer in use but there is any system is very old that does not support SSH it will use this port  

### SMTP (Simple Mail Transfer Protocol)

TCP port 25  
- Used to send and email form one server to other

### DNS (Domain Name System)

UDP port 53  
- It is used for open the website using the readable names

### DHCP (Dynamic Host Configuration Protocol)

UDP port 67  
UDP port 68  

- It is a server or appliance that has a pool of available IP addresses, when the device connected to the network, it requests an IP address and configuration parameters form that pool.  
- Sys admin can also use DHCP to manually configure IP addresses.

### HTTP (Hypertext Transfer Protocol)

TCP port 80  
- It is used to connect with the website without any encryption

### HTTPS (Hypertext Transfer Protocol Secure)

TCP port 443  
- It is as same as HTTP but with the encryption

### POP3 (Post office Protocol version 3)

TCP port 110  
- It is used to transfer data down to your computer  
- is able to be referenced using the LDAP protocol.

### IMAP or IMAP4 (Internet Message Access Protocol Vertion 4)

TCP port 143  
- It is used for emails.  
- It has number of additional features not available in POP3

### SMB (Server Message Block)

UDP port 137  
- It use NetBIOS name service, which is like DNS  

TCP port 139  
- It use NetBIOS session service  

TCP port 445  
- It is the direct SMB communcation without the NetBIOS  
- It referred as CIFS (Common internet file system)  
- It used used to communicate with different devices like windows or printer.

### LDAP (Lightweight Directory Access protocol)

### LDAPS (Lightweight Directory Access protocol Secure)

TCP port 389  
- It is use to manage and control the central database  
- It also used in Active Directory Infrastruture

### RDP (Remote desktop protocol)

TCP port 3389  
- It is used to control and access windows devices across the network.  
- It also allow you to connect to that Windows computer from Mac OS, Linux, Unix, iPhone, and other OS, as well.

END
