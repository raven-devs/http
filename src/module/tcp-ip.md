# TCP / IP

## How Information Travels on the Internet

Data travels across the internet in packets. Each packet can carry a maximum of 1,500 bytes. Around these packets is a wrapper with a header and a footer. The information contained in the wrapper tells computers what kind of data is in the packet, how it fits together with other data, where the data came from and the data's final destination.

When you send an e-mail to someone, the message breaks up into packets that travel across the network. Different packets from the same message don't have to follow the same path. That's part of what makes the Internet so robust and fast. Packets will travel from one machine to another until they reach their destination. As the packets arrive, the computer receiving the data assembles the packets like a puzzle, recreating the message.

All data transfers across the Internet work on this principle. It helps networks manage traffic -- if one pathway becomes clogged with traffic, packets can go through a different route.

That's not the case with traffic across IP networks. If one connection should fail, data can travel across an alternate route. This works for individual networks and the Internet as a whole. For instance, even if a packet doesn't make it to the destination, the machine receiving the data can determine which packet is missing by referencing the other packets. It can send a message to the machine sending the data to send it again, creating redundancy. This all happens in the span of just a few milliseconds.

## TCP/IP: What Is It And How Does It Work?

The Transmission Control Protocol and the Internet Protocol create what is known a TCP/IP model.

### What Is An IP Address?

The Internet protocol or IP delivers (routes and addresses) data packets between a source (device or application) and their destination. It makes sure that those packets arrive at the right destination. It defines the rules and formats for applications and devices to communicate and exchange those data packets on a specific network or across different connected networks.

IP addresses are unique identifiers responsible for sending data to the correct location on the internet or a local network. They basically make communication via the internet possible.

IP stands for Internet Protocol, which is a set of rules that facilitates data communication between networks. Each internet-connected network or device within a network needs an Internet Protocol address to send and receive data.

The format of an IP address is a set of numbers separated by dots or colons. For example, 17.172.224.47 (Internet Protocol version 4) or 1301:7db8:86a3:3010:0000:8a4e:0474:7104 (Internet Protocol version 6). The number and range of these values separated by punctuation depend on the type/version of the IP address.

IP addresses are allocated by the Internet Assigned Numbers Authority (IANA), a subsidiary of the Internet Corporation for Assigned Names and Numbers (ICANN), a nonprofit organization based in the US.

IANA doesn’t assign IP addresses individually but instead assigns them en masse to organizations, institutions and internet service providers who then assign them on a smaller scale.

### What is TCP?

The transmission control protocol or TCP organizes data in a specific manner to protect them while exchanged between a client and a server. It’s a very used protocol on networks by all types of devices and applications. TCP protects data’s integrity from the sending and all the way to their delivery.

TCP stands for Transmission Control Protocol, which was created in the 1970s by the Defense Advanced Research Projects Agency (DARPA) of the US Department of Defense. In fact, the entire TCP/IP protocol suite was created by two DARPA scientists – Vint Cerf and Bob Kahn.

Out of all available communication methods, theirs became the global standard and is now maintained by the Internet Engineering Task Force (IETF), the nonprofit agency responsible for developing internet standards.

The TCP is a protocol just like IP. However, TCP is the internet protocol that connects a specific server to a particular client. So, together, the Transmission Control Protocol and Internet Protocol introduce the rules that allow computers to communicate via the internet.

Information online travels via data packets – the same data packets that the IP makes sure reach the right place. The information is effectively separated into these packets for easier and faster travel. Once the packets arrive at their intended destination, they get assembled back into that same information.

The TCP protocol ensures that:

- All data packets are reassembled in the proper order
- No data packets are lost
- There are no delays that could affect the quality of data or the reassembly process

In other words, TCP collects and reassembles data packets while IP ensures data packets are delivered to the right destination.

## TCP vs IP

Although the Transmission Control Protocol and the Internet Protocol are two completely different protocols, they are typically grouped together due to the vast importance of TCP/IP and because they are often meaningless without each other.

That said, each of the two main protocols in this protocol suite does a different thing. IP obtains the address to which data needs to be sent. Once the IP address of the destination is known, TCP ensures data reaches it.

What’s more, the two are entirely different types of protocols. While IP is one of the leading communications protocols in the world, TCP is a transport layer protocol.

This difference in the type also means that the two main protocols work on different layers within the TCP/IP system that uses four abstraction layers. Two of these layers are the network layer and the transport layer. IP works on the former and TCP – on the latter.

In the end, the responsibilities of the two protocols are different:

- IP is responsible for locating the proper path for delivering packets
- TCP is responsible for end-to-end delivery and the correction of errors on that path

Consider the following analogy to fully understand how these two protocols are so different yet codependent.

The IP is the phone number assigned to a phone, while the TCP is the technology that allows the phone to ring and for people with different phone numbers to talk to each other. The phone number is useless unless there’s a way for you to speak to a person on the other end of the line, while the technology facilitating the communication is equally meaningless without the phones and numbers using it.

## What is in the TCP/IP protocol suite?

TCP/IP was developed so computers would have a way to send data to each other. It’s named after the two main protocols we’ve discussed already – TCP and IP. However, TCP/IP is a protocol suite containing many other protocols, including three more that are fundamental to this model:

- Internet Control Message Protocol (ICMP)
- Internet Group Management Protocol (IGMP)
- Address Resolution Protocol (ARP)

Network devices usually use the ICMP to send error messages. The IGMP allows hosts and routers from IPv4 networks to establish multicast group memberships. And the ARP helps discover link-layer addresses.

Some other common protocols in the TCP/IP model include:

- File Transfer Protocol (FTP)
- Hypertext Transfer Protocol (HTTP)
- Simple Mail Transfer Protocol (SMTP) / Post Office Protocol (POP3) / Internet Message Application Protocol (IMAP)
- Secure Shell (SSH)

## How does TCP/IP function?

IP protocol works through different resources, like the IP addresses. To connect to the Internet, domains and devices get a unique IP address to be identified and allowed to communicate (exchange data) with other connected devices.

Data travel across networks separated into pieces (packets). Every piece gets IP information (IP address) attached for routers to read it and send the packet to the correct destination. Once there, the way for those packets to be handle will depend on the kind of protocol (commonly TCP or UDP) combined with the IP to transport them.

IP is a connectionless protocol. All data packets are just addressed, routed, and delivered without existing acknowledgment from the destination to the source. This lack is resolved through the Transmission Control Protocol.

TCP secures the travel and delivery of data packets across networks through a specific process. To start, a connection between the source and the destination is required, even before the transmission of data begins. This, because TCP is a connection-oriented protocol. To work properly, it needs to guarantee this active connection until the sending and receiving of data get completed.

When the communication begins, TCP takes the sender’s messages and chops them into packets. To protect messages’ integrity, TCP numbers every packet. Then packets are ready to go to the IP layer for being transported. They will be dispatched to travel around different routers and gateways of the network to reach their destination. No matter all the packets are part of the same message, they can have different routes to arrive at the same destination.

Once they all hit their destination, TCP proceeds to re-build the message by putting all their pieces (packets) together again to make a proper delivery.

This ideal scenario can be affected if networks face issues. Data packets could get lost in transit, duplicated, or disordered. The advantage is TCP’s functionality can detect such problems and fix them. The protocol can ask the lost packets to be re-sent to organize them again in the correct order. In case messages can’t be delivered, this is reported to the sender (source).

As you see, the Internet is a packet-switched network. All data are chopped into packets that are dispatched through lots of different routes simultaneously. When they finally hit their destination, they get re-built by TCP. And IP is in charge of the packets to be sent to the correct destination.

TCP/IP uses something called a client-server communication model. In it, the user or the device (the client) sends a request to another computer (the server) within a network. Its goal is to send a message from one device to another without it being broken or corrupted but still delivered promptly.  

The whole protocol suite places the most emphasis on accurately completing its primary task. And since an entire message can easily be corrupted, it always breaks it down into the data packets we’ve already discussed. This system ensures that the protocol doesn’t have to send the entire message all over again in the case of a corrupted or broken packet.

The system works as each packet can take a different path to arrive at the destination, where all packets reassemble.

TCP/IP also divides each of its tasks into distinct abstraction layers, two of which we’ve already mentioned. Each layer in this system has a different function, and data has to pass through all of them to get to its destination.

Once it does, TCP/IP can go through the same layers in reverse to correctly reassemble the packets. After, the user gets the entire message, just as it was when it was sent.

This might sound complex and unnecessary, but the four-layer system ensures communication is standardized and possible for the entire planet. That way, all hardware and software can communicate with each other, regardless of their manufacturer or the operating system in use. In other words, it would be impossible to communicate with others properly without this standardization.

As the four-layer solution is essential, let’s cover how it works and what layers it contains.

## What is the TCP/IP model?

The four-layer system of the TCP/IP model consists of the following four layers:

- Application layer
- Transport layer
- Internet layer
- Network access layer

Each layer has its own protocols, which make up a suite of protocols. Each layer also has its own functions that allow this entire system to work well.

### Application layer

This is the top layer, and it supplies an interface for applications and network services to communicate. It identifies participants involved in a communication, defines the access to the network’s resources, and the rules for application protocols and transport services interaction. Application layer includes all the higher-level protocols like DNS, HTTP, SSH, FTP, SNMP, SMTP, DHCP, etc.

The application layer includes all the applications you need to use to access the network and receive communication. The application layer is important for the user for the simple reason that it’s the part you actually see.

In other words, the application layer consists of apps like messaging applications, cloud storage apps and email services.

This layer performs various tasks, including:

- Identifying communication partners
- Synchronizing communication
- Allowing users to log into remote hosts

The layer includes various protocols, including HTTP, FTP and SNMP (Simple Network Management Protocol).

All in all, thanks to the application layer, communication apps don’t have to worry about other layers we’ve discussed, and they get to have standardized data exchange.

### Transport Layer

It defines the amount of data and the rate for transporting data correctly. It receives messages from the application layer, divides them into pieces, transports them, re-builds them following the proper sequence, and solves possible issues to guarantee their integrity and proper delivery. TCP operates in this layer.

The transport layer is responsible for providing a reliable data connection between devices. In other words, the transport layer performs the following tasks:

- Divides data into packets
- Validates packages received from another device
- Ensures that another device acknowledges the packets

This is understandably a much broader function as it includes various other processes. For instance, as the transport layer divides a message into packets, it must also ensure they arrive at their destination intact, so the message stays the same and uncorrupted.

The transport layer is the one that includes the TCP protocol, but it also contains the User Datagram Protocol (UDP), as it replaces the TCP on special occasions. That said, the UDP is typically less reliable as it doesn’t ensure that every data packet reaches its destination. That’s precisely why TCP is the standard protocol within this layer.

### Internet layer

The internet layer, also known as the IP or network layer (not to be confused with the network access layer), is in charge of sending packets and ensuring that data is transferred as precisely as possible. As it controls the direction and pace of traffic, it is somewhat similar to a traffic controller on a road. Additionally, it supplies the procedural steps and functionalities for transferring data sequences. This layer’s protocols include IPv4, IPv6, ICMP, and ARP.

The internet layer, or the network layer, controls traffic routing and facilitates flow control. The second layer in the TCP/IP hierarchy ensures data sending is always accurate and fast. Because of this function, data always reaches the destination, regardless of its route.

Furthermore, the network layer also handles the reassembly of packets once they have reached their destination address.

However, if there’s too much internet traffic, the layer needs time to send information. Of course, thanks to that time, the chances for file corruption are lower.

The network layer deals with several protocols, including routing protocols and multicast group management.

### Network access layer

The OSI model’s data link layer and physical layer are combined to form the network access layer. It outlines the process through which data is actually transferred over the network. It also covers how hardware components that physically interact with a network, such as twisted-pair copper wire, optical fiber, and coaxial cable, transmit data via optical or electrical means. The network access layer is the bottom layer in the TCP/IP model.

The network access layer is also known as the data link layer, the physical layer or the network interface layer. It’s the lowest layer in the TCP/IP layer hierarchy.

It deals with the physical part of the whole communication process. In other words, it handles the hardware infrastructure that allows the computer to communicate with another.

Within a computer, the physical layer deals with things like the ethernet cable, the network interface card, a wireless network and device drivers.

Besides this, the data link layer also includes the technical infrastructure that enables network connections.

The physical layer helps define how data transmits physically on a network, but it’s also responsible for data transmission between devices that are part of that network.

## TCP/IP vs the OSI model

Now that we’ve explained the TCP/IP model, it’s worth briefly discussing the OSI model – the Open Systems Interconnection Model. The OSI model is only a conceptual framework that describes the typical functions of a networking system.

However, as the OSI reference model describes how apps can communicate online and as it shares some of the same layers from the actual TCP/IP four layers model, it’s worth noting the seven layers it uses:

- Physical layer: Transfers raw bits through the hardware
- Data link layer: Defines the exact format data has within the network
- Network layer: Defines the physical path data must take to reach the destination
- Transport layer: Moves the data with the help of transmission protocols like TCP
- Session layer: Controls ports and sessions and maintains the connection
- Presentation layer: Ensures data uses the proper format
- Application layer: Where apps access network services, the exact apps you use

## TCP vs UDP

There are clear differences between the transmission control protocol (TCP) and User Datagram Protocol (UDP).

- TCP is connection-oriented, while UDP is connectionless. TCP requires an active connection to start and complete the data transmission, while UDP does not.
- TCP can recover lost packets by requiring retransmission. UDP can’t recover them.
- TCP is much slower than UDP because its process involves verification in almost every step. To guarantee the connection is active and the source ready to receive a message, to confirm delivery, etc. UDP only sends, avoiding those confirmation steps.
- TCP protects packets’ integrity efficiently. To protect this is not UDP’s strength. Its mechanism to check integrity (checksum) is less precise.
- TCP delivers ordered messages (by reassembling them based on a numerical sequence). UDP doesn’t offer this function.
- TCP guarantees the data delivery to their recipient. UDP doesn’t.
- TCP detects and fixes possible errors better. It also supplies confirmation of delivery or reports the problem if it’s not possible to deliver. The UDP’s mechanism for error detection (checksum) is simpler and limited. It doesn’t confirm or inform about the delivery.
- TCP’s speed doesn’t solve latency. UDP really does it.
- TCP doesn’t support broadcast, while UDP really does since it does not require response or confirmation.
- The efficiency of TCP makes it ideal for applications that demand full integrity of data, zero loss (HTTP, FTP, IMAP, SSH, SMTP).
- UDP works very well for applications that require high speed and can afford data loss. Think about real-time applications like live video streaming, voice-over IP or online gaming.

## TCP vs HTTP

The Transmission Control Protocol (TCP) and the Hypertext Transfer Protocol (HTTP) also differ between them.

- TCP is used to set communication or a session between two machines (client and server). In contrast, HTTP is used for accessing data of webpages and accessing content (websites) from a web server. It’s a client-server protocol. Requests begin with the recipient, like a browser.
- TCP is a data transfer protocol. HTTP uses TCP for data transfer.
- TCP uses IP addresses, while HTTP uses hyperlinks, also known as URLs.
- TCP is connected-oriented, while HTTP is stateless but not sessionless.
- TCP needs authentication (TCP-AO). HTTP does not.
- TCP process involves a three-way handshake, and this takes some time. HTTP is one-way communication. TCP is slower than HTTP.
- TCP uses different ports (80, 8000, 8080, etc.). HTTP usually uses the 80 port.

## TCP and the Three-Way Handshake

Before transmitting packets, TCP must ensure that a stable connection has been set up between the sender and the recipient. This is where the three-way handshake (or SYN-SYN-ACK) comes in. Much like how you’d traditionally shake hands when meeting a new colleague at work or greeting someone you know on the street, there needs to be a similar exchange of messages and acknowledgments that takes place between the two parties in a TCP connection.

The TCP three-way handshake works as follows:

- The client sends a SYN packet to the server asking him to open a connection.
- The server responds by sending a SYN-ACK, acknowledging receipt of the SYN packet, and confirming that it’s ready to connect.
- The client responds with ACK to validate the connection and the transmission of packets starts.
