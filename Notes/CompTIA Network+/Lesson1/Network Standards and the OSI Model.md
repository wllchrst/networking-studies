Standards is created because of the complexity of computer hardware and software increases, the problem of successfully communicating between the systems become more difficult, hence the use of standards of network models.

One of the most famous network models is called **Open Systems Interconnection (OSI)** Model, which consists of 7 different layers which is going to be explain later. However OSI model is not a standard or a specification, it serves as a functional guideline of designing network protocols, software and for troubleshooting networks.

---
## Protocol Data Units (PDU)
Protocol is a set of rules enabling systems to communicate by exchanging data in a structured format. Two of the most important function is to provide addressing (describing where the data should go) and encapsulation add fields in a header to whatever data is being transmitted. 

At each layer of the OSI model for two nodes to communicate they must be running the same protocol this is called **same layer interaction**. 

To transmit or receive a communication, on each node, each layer provides services for the layer above and uses the services provided by the layer below, or called **adjancent layer interaction**.

A sending node have a data, which uses the data to travel down each layer of the OSI model, each layer except for physical layer always add a header into the data, this is called **encapsulation**. When the data is being received at the receiving node, it performs the reverse process or usually called de-encapsulation.

---
## OSI Model
OSI model consists of 7 layers which is easily remember with this sentence "Please Do Not Throw Sausage Pizza Away"

Physical, Data Link, Network, Transport, Session, Presentation, Application

**Physical Layer**
A node is any device that can communicate with other nodes via network interfaces. A link between this network nodes is created using some form of physical media. Physical layer usually takes form of a **cable**, but **wireless transmission** also provide the same function using media such as **radio transmissions**. PHY layer is responsible in the act of transmitting and receiving **bits**. At the physical layer, a segment is one where all the nodes share the same media, a network is usually divided into segments to cope with the physical restrictions of media used, usually to improve performance or security.

Physical Layer specifies the following:
1. Physical topology - layout of nodes and transmissions established by the transmission media
2. Physical interface - mechanical specifications for the network medium, cable specifications, medium connector and pin-out details.
3. The process of transmitting and receiving signals over the network medium.

Devices that operates at the physical layer:
- Transceiver - part of a network interface that sends and receives signals over the network media
- Repeaters - A device that amplify the signal to extend the maximum allowed distance media type. Exactly as the name say repeaters it repeats the signal to make the electronic signals stronger and able to send signal further.
- Hubs - Multiport repeaters, allowing multiple device to connect to the hub and receive the message.
- Media converters - converts one media signaling type to another.
- Modems - Device that covert between digital and analog signal transmissions.

**Data Link**
The addresses of interfaces within the same network or a segment is called **local address or hardware address** where all nodes can send traffic to one another using only this address, without the need of IP Address. Hence this layer Data link (DL) is responsible for transferring data between nodes on the same segment using only hardware address. DL is responsible for organizing the stream of bits from the physical layer and converting it into structured units called frames. Data links add headers fields that consists of destination and source hardware address.

Another important function of the data link layer is to do error checking such as, identifying truncated or corrupted frames. Data link layer is also responsible determining how multiple nodes in one segment can share access to the network media.

Devices:
- Network adapters or network interface cards - hardware component that joins a host into a network, helping it by assembling and disassembling frames.
- Bridges - joins two network segment while minimizing the performance reduction of having more nodes on the same network.
- Switches - advance type of bridge with many ports, a switch creates links between large numbers of nodes more efficiently
- Access points - Allows nodes with wireless network cards to communicate with wireless network and wired ones.

![[Pasted image 20251119095509.png]]

IEEE 802 standards is a standards by the organization called IEEE which oversees the development and registration of electronic standards. Based on the regulation of IEEE, the Data link layer is split into two sublayers which is Media Access Control (MAC) and Logical Link Control. Media Access Control Layer covers how multiple network interface share a single transmission medium:
- Logical topology - bus or ring
- Media access method - contention or token passing.
- Addressing the- format for the hardware address of each network interface.
- Frame format
- Error checking mechanism
Logical Link Control sublayer is used to provide standard over giving the network layer service interface, regardless what MAC sublayer protocol is used.

**Network Layer**
Third layer is responsible for moving data around a network of networks, known as an internetwork or the internet. Data link capable of forwarding data in a single segment only using the hardware address, however network layer move information around an internetwork by using logical network and host ids. Each packet moves router by router through the internetwork to the target network. Once the packet has arrived to the target network the hardware destination address can finally be used.

> The general convention to talk about PDUs at the network layer as packets or datagrams, however the term packets is often used to describe PDUs at any layer.

Main devices used at this layer are routers and layer 3 switch that combines the functionality of router, switch and firewall.

![[Pasted image 20251119104012.png]]

**Transport Layer**
Known as host-to-host or end-to-end layer, the content of the packets starts to become significant. It is responsible to identify each type of network application by assigning it a port number, for example HTTP request mapped into port 80 and email is mapped to port 25.

On the sending host, data received from the upper layers is packaged as a series of layer 4 PDUs, referred to as segments. Additionally the layer is also responsible for ensuring reliable data delivery, meaning any lost or damaged packets are resent. Devices in this layer include multilayer switch which work as load balancers, and many types of security appliances.

**Session and Presentation**
The upper layer of OSI model is usually associated between providing useful interface between the upper layer and transport layer.

Session Layer
The layer is responsible in managing dialog between two hosts, session layer manage the process of establishing the dialog, managing the data transfer and tearing down the session. Session can work in three modes:
- One-way / Simplex, only one system is allowed to send the message and the other is receive.
- Two-way alternate/half-duplex
- Two-way simultaneous/Full-Duplex

Presentation Layer
The layer is responsible in transforming the data needed for the application and the network layer. Communicating computers may use different character coding systems such as ASCII. It is also responsible for doing data compression and encryption.

**Application Layer**
Application is at the most top of the OSI stack, it doesn't give service to any layer on top of it. The main responsibility of the layer is to provide an interface on network hosts that have established a communication channel.

![[Pasted image 20251119134011.png]]

---
>Even though OSI model has its used for network design and troubleshooting, in practical terms networking is dominated with the TCP/IP suite.

## Transmission Control Protocol/Internet Protocol
Known as TCP/IP suite maps to only 4 layer which is Application, Transport, Internet and Link (network interface). Each layer in this model is corresponds to one or more layer of the OSI model.

![[Pasted image 20251120090519.png]]

**Link/Network Interface Layer**
It is an encapsulation of layers from OSI model of data link layer and physical layer. Basically it defines the host's connection to the network media. It is mainly responsible in the interchange of frames between hosts. The technologies used can be LAN (Ethernet or Wi-Fi) or WAN-based (T-carrier, ISDN, or DSL).

**Internet Layer**
Precisely Internetwork layer provides addressing and routing functions. It provides the ability to fragment large frames into smaller packets. The protocol this layer layer uses is the Internet Protocol and Address Resolution Protocol

> ARP is a protocol in networking which is responsible in mapping device's logical IP address to its physical MAC address on a local network. However it is usually mixed up whether the protocol runs in Data Link layer or Internetwork layer since the need of MAC Address. It is better to interpret it as layer 2.5 protocol.

**Transport Layer**
Establish the connection between two host. It breaks the Application-layer information into **segments**. TCP/IP suite provides two methods of data delivery: 
- Connection-oriented delivery using the **Transmission Control Protocol (TCP)**
- Connectionless delivery using the **User Datagram Protocol (UDP)**

**Application Layer**
This is the layer at which many TCP/IP services can be run, which is HTTP, FTP, SMTP

