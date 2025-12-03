On the Internet, TCP/IP addresses must follow a regulated rules with a common to ensure there a no duplicated addresses worldwide. Companies and ISPs usually lease addresses for their networks and customers to gain internet access other than that other available networks are private address.

Public IP address is one that can establish with other IP networks and hosts over the **Internet**. The allocation of this public IP addresses is governed and regulated by IANA and Internet Service Provider. Hosts communicating in the same local network usually uses private addressing. This pool of addresses is defined in RFC 1918 which is:
- 10.0.0.0 - 10.255.255.255 class A private addresses
- 172.16.0.0 - 172.31.255.255 class B private addresses
- 192.168.0.0 - 192.168.255.255 class C private addresses
Through a router configured with a single or a block of public IP address, private network can communicate with the internet through a process called **Network Address Translation (NAT)**.

**Loopback Addresses**, which is a part of class A, the range 127.0.0.0 to 127.255.255.255 is reserved. Specifically addressed for checking if TCP/IP is correctly installed. Every IP host is automatically configured with a default loopback address of 127.0.0.1

**Reserved Address Ranges**, other than loopback, private addresses and class D and class E. Other IPv4 addresses are reserved for other purpose below are the details:
![[Pasted image 20251203120143.png]]

**Classless Inter-Domain Routing (CIDR)**, essentially it uses bits normally assigned to the network to the network ID to mask the complexity of the subnet and host addressing scheme within that network. This also called as **supernetting**.
