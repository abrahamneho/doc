### Different ways for a Network
- [ ] Wireless Networks  
- [ ] ethernet Networks  
- [ ] DSL Networks  
- [ ] other types  

- **Ethernet header**
- ↓ 
- **Network (ethernet Payload)**
- ↓ 
- **IP (Internet Protocol)**
- ↓ 
- [ ] TCP (Transmission Control Protocol)  
- [ ] UDP (User Datagram Protocol)  
- These are refer as an OSI Layer 4 protocol.
- ↓ 
- **Ethernet trailer**

**TCP (Transmission Control Protocol)**
- This is the protocol which is connection oriented.  
- It is refers to as reliable delivery.  
- It includes an acknowledgment process.  
- It refer to this as flow control, which means speed up or slow down the data.  

**UDP (User Datagram Protocol)**
- This is connectionless protocol  
- It refers to as unreliable delivery  
- It has no acknowledgments  
- There is no flow control  
- Advantage comparing to TCP  
- *Very little Overhead*
- *Example*
- [ ] DHCP (Dynamic Host Configuration Protocol)  
- [ ] TFTP (Trivial File Transter Protocol)  

**Resend data is the process done by the appication which means the data will be resend automaticaly using TCP protocol**
- [ ] HTTPS (Hypertext transfer protocol secure)  
- [ ] SSH (Secure shell)  
- These are using Resend data method

## Port Number
Port Number is used to refer the particular service, means there are different service are there using the same IP, So the Port number is used to identfy the right service.
- It is used to deliver the data in a right serivce.

**There are types of port Numbers which are used by applcations and client (user)**
- TCP port xx is not equal to UDP port xx  
- [ ] Nonephemeral ports (Permanent port numbers)
- This types of ports is always be a same number  
- The port are between port 0 and port 1023  

- [ ] ephemeral ports (Temporarily port numbers)
- It is the random port numbers used for the communection  
- The port are between port 1024 and 65,535  

- [ ] **END**
