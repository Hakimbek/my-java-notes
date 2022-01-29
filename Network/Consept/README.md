# Java Networking
Java Networking is a concept of connecting two or more computing devices together so that we can share resources.

Java socket programming provides facility to share data between different computing devices.

## Advantage of Java Networking
- Sharing resources
- Centralize software management

# The java.net package supports two protocols,

## TCP
Transmission Control Protocol provides reliable communication between the sender and receiver. TCP is used along with the Internet Protocol referred as TCP/IP.

## UDP
User Datagram Protocol provides a connection-less protocol service by allowing packet of data to be transferred along two or more nodes

# Java Networking Terminology

## 1) IP Address
IP address is a unique number assigned to a node of a network e.g. 192.168.0.1 . It is composed of octets that range from 0 to 255.
It is a logical address that can be changed.

## 2) Protocol
A protocol is a set of rules basically that is followed for communication. For example:
- TCP
- FTP
- Telnet
- SMTP
- POP etc.

## 3) Port Number
The port number is used to uniquely identify different applications. It acts as a communication endpoint between applications. 
The port number is associated with the IP address for communication between two applications.

## 4) MAC Address
MAC (Media Access Control) address is a unique identifier of NIC (Network Interface Controller). A network node can have multiple NIC but each with unique MAC address.
For example, an ethernet card may have a MAC address of 00:0d:83::b1:c0:8e.

## 5) Connection-oriented and connection-less protocol
In connection-oriented protocol, acknowledgement is sent by the receiver. So it is reliable but slow. The example of connection-oriented protocol is TCP.
But, in connection-less protocol, acknowledgement is not sent by the receiver. So it is not reliable but fast. The example of connection-less protocol is UDP.

## 6) Socket
A socket is an endpoint between two way communications.

# Java Socket Programming
Java Socket programming is used for communication between the applications running on different JRE. Java Socket programming can be connection-oriented or connection-less.

Socket and ServerSocket classes are used for connection-oriented socket programming and DatagramSocket and DatagramPacket classes are used for connection-less socket programming.

The client in socket programming must know two information:
1. IP Address of Server, and
2. Port number.

# Socket class
A socket is simply an endpoint for communications between the machines. The Socket class can be used to create a socket.

# ServerSocket class
The ServerSocket class can be used to create a server socket. This object is used to establish communication with the clients.
