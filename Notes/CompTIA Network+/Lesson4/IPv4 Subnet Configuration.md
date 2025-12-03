**IPv4 Broadcast Domains**
One address where all the hosts receive the same broadcast packets. It is established at the network layer usually routers. Consequently it is separate with the network domain, and is always the last IP address in any IP network. So for example if a network has this configuration, network host: 192.168.0.0/24 then the broadcast domain is 192.168.0.255

**IPv4 Multicast**
IPv4 multicasting allow one host on the internet to send multiple content to other hosts that have identified themselves as interested in receiving the packets from the original host. The IGMP or Internet Group Message Protocol is typically used to configure group memberships. In layer 2, multicasts are delivered using a special range of MAC Address, if the switch doesn't support IGMP, it will treat multicast like a broadcast and flood all port.

### Classful Addressing
Allocated a network ID based on the first octet of the IP address, was first employed in the 1980s before the use of subnet to identify network ID portion based of an address and subnet information. The class in classful addressing is determined by the first octet of the IP Address, below are the mapping of the classes information.
![[Pasted image 20251203105132.png]]
However there are reserved address that is used for specific function which is class D ranging from 224.0.0.0 to 239.255.255.255 that is used for multicasting. Class E ranging from 240.0.0.0 to 255.255.255.255 reserved for experimental use and testing.

### Subnet Design
A process of logically dividing a network into smaller subnetworks, with each sub-network having a unique network ID. Below are the reasons of the subnet design:
- A network that contain a very large number of host on the same IP network is really inefficient meaning they are in the same broadcast domain, which create excessive broadcast traffic. To handle this company usually configure Virtual Local Area Network (VLAN) to isolate broadcast domains a create subnets.
- Network that uses different physical technology should have different subnets.
- It is useful to logically divide a network into smaller section for security and administrative control.

### Classless Addressing
A scheme that disregard completely the concepts of classes and default masks in favor of representing the network address with an appropriate size network prefix. It is fully using the subnet design for example an IP address of 192.168.5.5/24 has a network address of 192.168.0.0

