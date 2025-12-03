At the network layer, IP or internet protocol provides logical host and network addressing and routing. IP that is currently used are IPv4 and IPv6 which later in other notes will be explained what is the key difference.

**IPv4 datagram structure**

![[Pasted image 20251203095142.png]]
- Version field - indicated whether the IP packet/datagram is currently using version 4 or 6.
- Length - give the information of the size of the header and also the payload.
- Protocol - what is contained in the payload so that the receiving host knows how to process it, here are the list of protocol that can be run: **TCP, UDP, ICMP, IGMP, Generic Routing Encapsulation, Encapsulating Security Payload, Enhanced Interior Gateway Routing Protocol**.
- Diffserv - to indicate the priority of the packet, so it can give more attention and facilitate better quality real-time data transfers.
- TTL - The amount of time a packet can stay on the network. While TTL is defined in seconds, nowadays it is interpreted as maximum hop count that can happen.
- ID, Flags, and Fragment Offset - indicate whether the IP datagram has been split between multiple packets for transport over the underlying data link layer.
- checksum - field that is used mainly for doing error detection.

**Routing Basics (is not a detailed explanation)**
1. IP tries to establish a connection to the destination source by IP Address. The subnet mask from both the source and destination is applied to find each of the network address.
2. The destination network address is compared with the source's network address. If they are in the same network, IP uses ARP messaging to locate the destination address. Else the packet in sent to default gateway (router)
3. If the packet has been routed the TTL field on the packet field is going to be decreased, if the TTL field is less than zero than the packet is going to be dropped out of the network.
4. The router will determined what to do with the packet by repeating the steps described from the second step on.