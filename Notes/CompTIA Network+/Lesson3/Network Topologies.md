**Logical vs Physical network topologies**
- The physical network topology - describes the placement of nodes and how they are connected by the network media physically. For example, one network nodes might be directly connect and in another network the nodes is connected via a switch.
- The logical network topology - describes the flow of the network, based on the previous example physical topology is different but it is the same on the logical network topology.

**Point-to-point links** - simplest type of topology, a single is established between two nodes. A point to point link can be physical or logical, for example a Wide Area Network might have a lot of routers and complicated network architecture but two nodes is connect in a point to point manner is called logical point to point links.

**Bus Topology** - topology with more than two nodes, with shared access topology, meaning that all nodes share the bandwidth of the media. Only one node can be active at any one times, so the nodes must content to put signals on the media. A signal travels down the bus in both directions that is connected to the segment, and the bus is terminated at both ends of the cable to absorb the signal when it has passed all the connected nodes. However this type of physical bus is the basis or earliest Ethernet networks but is no longer in widespread use, since if one cable is broken the whole network is broken making it not reliable.

A logical bus topology is one in which nodes receives all data transmitted at the same time.

**Star Topology** - each endpoint node is connected to a central forwarding node, such as a hub, switch or router. Currently the star topology is the most widely used physical topology. For example, a typical SOHO network would use the star topology because it is easy to reconfigure and monitor.

**Physical star | Logical bus topology** - this happen where the physical topology is designed as a star topology but is using device like a hub at the center of the star, where the hub will transmit a frame to all ports.
![[Pasted image 20251125121122.png]]

**Physical Star | Logical Star** - just like the previous statement it is using the physical star topology but using a device like switch as a center of the star.

![[Pasted image 20251125121131.png]]

**Ring Topology** - each node is wired to its neighbor in a closed loop. A node receives a transmission from its upstream neighbor and passes to its downstream neighbor until the transmission reaches its intended destination. However this topology is no longer used in LANs, but it does remain a feature of many WANs. Where two ring systems (dual counter rotating rings) can be used to provide fault tolerance where one ring is down the other can still operate the whole network.

**Mesh Topology** - commonly used in WANs, especially public networks like the Internet. In theory each device in the network has a point to point link with every device on the network. The number of links each node should have, required by a **full mesh** is expressed as n(n - 1)/2 where n is the number of nodes. However if the number of nodes increases the amount of links that is required for it to be full mesh is a lot. That is why in the real world application **partial mesh** is usually more practical, where the most important nodes or devices receive the most attention for fault tolerance.

![[Pasted image 20251125121727.png]]