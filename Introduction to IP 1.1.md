## TERMS TO GET FAMILIAR WITH

### Topology

### Multiplexing
The ability to use multiple applications at the same time.

### TCP (Transmission Control Protocol)
A connection oriented protocol. There is a formal connection made with the separate device on the network. Data is transferred and then that connection is formally terminated at the end of that communication. There is additional overhead that takes place every time you need to send information via TCP. We also refer to TCP as a reliable mode of communication. Every time we send data to every device, we expect to receive an acknowledgment from that device.There is evidence that delivery has been made. TCP also numbers the data it's sending, so new requests could be made for that data. It also allows the receiving device to control the flow of traffic.

### UDP (User Datagram Protocol)
It does not have a formal call set-up, or formal call breakdown process. It's called a connectionless protocol because it starts sending data when it's available, and hopes that the receiving node is actually receiving the data. We call it unreliable delivery. We don't receive an ack from the other device. UDP doesn't have a way to recover data that was lost, and it doesn't have a way to re-order data. No flow control. The sending device will determine how much data will be used to communicate.

### THE SIMILARITIES BETWEEN TCP AND UDP (Which operate at the layer 4 of the OSI model)
They both allow us to Multiplex (to use multiple applications at the same time.)

### IPV4 SOCKETS
A socket is one endpoint of a two-way communication link between two programs running on the network. A socket is bound to a port number so that the TCP layer can identify the application that data is destined to be sent to. An endpoint is a combination of an IP address and a port number.

### IPV4 SOCKETS CLIENT & SERVER COMMUNICATION
- Server: IP address, protocol (TCP or UDP), server application port number.
- Client: IP address, protocol (TCP or UDP), client port number.

### PORTS
- Ports operate at the *Transport Layer*

- Definition: Port numbers are used to determine which part of the network the data will travel to. For example if you have a small lan. You have a server for unencrypted web traffic, and a separate server for encrypted web traffic. The first server would have the assigned port number of 80, and port 443 for traffic that is encrypted. That way the protocol would know which server to send the data to. That way the protocol knows exactly which application the information is going to.

- Port numbers are for communication, not security. Both the server and the client can choose to use ANY port number from the range mentioned below. You shouldn't use port numbers, as a type of security measure.

### PORT TYPES
- Non-ephemeral ports: These are non-temporal, or in other words, permanent port numbers. They're commonly used by applications or services that are running on a server.
  NOTE: *These port numbers usually range from 0 through 1,023*

- Ephemeral ports: These are temporary port numbers that the client usually decides to use randomly as it's sending this information back to the server. The server IP address usually would use a non-ephemeral port number, and the client IP address is commonly going to use an ephemeral port number.
  * NOTE: Although most servers (services) use non-ephemeral (not-temporary) port numbers, this isn't always the case. After all, it's just a number.

- TCP & UDP port numbers are different: This means that even if multiple applications in the network are using the same port 80, there won't be a conflict because one is a TCP port 80 and the other one is a UDP port 80. Although, you won't typically see this. Because most of the time you'll see clients and servers, using the well known port numbers for each protocol, and server/application type.

- *TCP & UDP port ranges: Any number between 0 and 65,535*


--------------------------------------------

## COMMUNICATION NETWORKS

### TELNET (Telecommunication Network):
- Telnet allows you to log into devices remotely, and to be able to access them from the terminal.
- It gives you console access.
- You can communicate to routers, switches, servers, and other devices to be able to administer those machines.
- NOTE: All of this communication is unencrypted. Which means it's a massive security hazard. This is why most people won't use telnet in a modern network.


### SSH (Secure Shell):
- Looks and acts the same as Telnet, but the data is encrypted.
