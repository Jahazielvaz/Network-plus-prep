# PROTOCOLS
- TCP/IP & UDP Protocols are responsible for transporting data. It would be the road in the truck analogy.

## *LOOK TO INTRODUCTION TO IP1.1.md file for TCP & UDP PROTOCOLS*

### ICMP(Internet Control Message Protocol)
- You can think of it as text messaging between devices to check in and see how somebody might be doing.

- This is another protocol carried by IP, and it's not typically used for data transfer. It's commonly used for administrative purposes. For example, you may want to check to see if a machine is operating or not. At which point you would send an ICMP request, to see if that device is there. If the device is there, it'll send an ICMP response.

- Devices can also use ICMP to notify other devices on the network that things are not going so well. For example if you're sending information to another network, and the router from that network realizes that it's not able to communicate with the other network, it might send you back an ICMP to notify you that it can't establish a connection. It can also notify you that the TTL has expired.

### DNS (Domain Name System)
- Converts names to IP addresses.

### SMTP (Simple Mail Transfer Protocol)
- Server to server email transfer
- We also use this protocol to send mail from a device to a mail server.
- Commonly configured on mobile devices and email clients

### Incoming Mail PROTOCOLS
- Other protocols are used for clients to receive Email
- *IMAP4 (Internet Message Access Protocol V4)*: One of the email receiving protocols
- *POP3 (Post Office Protocol Version 3)*: One of the email receiving protocols
- These protocols authenticate and transfer email to your target node.
- They have basic mail transfer functionality
- *POP3*: Is considered a basic mail transfer protocol
- *IMAP4*: Is most commonly used, as it's the more robust protocol out of the 2.
- *IMAP4* allows us to use multiple clients to access our inbox. So we can see exactly the same mailbox from our mobile device, as we do from our desktop for example.

### FTP (File Transfer Protocol)
- Transfers files between systems
- Authenticates with a username and password
- Full featured functionality (list, add, delete, etc.)

### SFTP (Secure File Transfer Protocol)
- Uses SSH as the underlying protocol to transfer encrypted files. For this reason, it uses the same port number as SSH.
- It's a full feature file transfer protocol. This means, some of the things it can do are, resuming interrupted transfers, directory listings, remote file removal.

### DHCP (Dynamic Host Cofiguration Protocol)
- Automatically configures and assigns IP address, subnet mask, and other options to your node on the network.
- This protocol requires a DHCP server. This could be a standalone server, or it could be within the router/gateway.
- Normally has a pool of IP addresses configured into the server. These addresses are assigned to the node in real time.
- DHCP gives each node a lease and must renew at set intervals.
- Reservations: You can optionally configure reservations for a specific node to have the same IP addresses. This is typically done for servers and other infrastructure devices. This makes it easy if you need to change ip addresses on a number of devices because you can just change the ip address on the server that those devices communicate with.

### HTTP (Hypertext Transfer Protocol)
- This protocol operates at the application layer of the OSI model.
- It's used for communication between the browser and devices. As well as applications (Even if these applications don't run on the browser.)

### HTTPS (Hypertext Transfer Protocol Secure)
- Exactly like HTTP but uses SSL to encrypt all traffic.

### SNMP (Simple Network Management Protocol)
- This protocol is used for gathering metrics on infrastructure devices such as routers, servers, etc.
- Through this protocol you can query and receive data from infrastructure devices.
- There are multiple versions of SNMP
  * V1: It was the first iteration of this protocol. It has a set of well defined, structured tables. It is un-encrypted.
  * V2: Allowed us to transfer bulk data. Still in the clear (No encryption)
  * V3 (Current Version): Provides message integrity, authentication and encryption.

### RDP (Remote Desktop Protocol)
- This allows you to see the screen that is on a remote device.
- Allows you to share the keyboard and the mouse of said device.
- Works on many Windows versions
- Can connect to an entire desktop or just an application.
- There are also remote desktop clients available for other OSs, such as Mac OS, Linux, Unix, etc.

### NTP (Network Time Protocol)
- Every node/device, has it's own internal clock.
- NTP allows all devices to be able to know the standard time and clock speed.
- It's critical to synchronize the clock on all devices. Not only to sync log information, but some of these devices need to be perfectly synced in order to authenticate properly to each other.
- Again, every device must know what the proper date and the proper time is.
- I as an admin get to determine exactly the frequency that NTP will use, to be able to provide the synchronization.
- This is super accurate. On a LAN you can get the accuracy to be better than 1 millisecond.

### SIP (Session Initiation Protocol) (This is a Voice Over IP Protocol)
- It's used for setting up calls, ringing phone, & hanging up.
- Extends voice communication (Adds the following)
  * Video conferencing
  * Instant messaging
  * File transfer
  * etc.

### H.323 (This is another Voice Over IP protocol)
- Similar to *SIP* this protocol allows us to set up VoIP sessions which can call, ring, hang up
- One of the earliest VoIP protocol.
- Many systems still use it.


### SMB (Server Message Block)
- This protocol is used by Microsoft to transfer files between windows devices.
- File sharing, printer sharing
- Also called CIFS (Common Internet File System)

### LDAP / LDAPS (Lightweight Directory Access Protocol)
- All the users, devices, and printers are typically stored in a large db in your network. It's usually accessed through LDAP.
- In other words, this protocol allows the client to communicate with an LDAP server
- Store and retrieve information in a network directory
- *LDAPS* The S stands for secure. This is an encrypted version of the original LDAP, which uses SSL.
