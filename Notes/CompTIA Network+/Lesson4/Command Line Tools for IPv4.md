**ipconfig**
![[Pasted image 20251203101539.png]]

**Internet Control Message Protocol or ICMP**
Mostly used to report errors and send messages about the delivery of a packet. ICMP message types are generated under error conditions in most types of unicast traffic.
- echo request/reply - usually used for testing a connection with the ping utility.
- destination unreachable - a host on a remote network (or a protocol or a port on a host) cannot be contacted. This might be cause by a configuration error by a host or router.
- time exceeded - this is used when the TTL field on an IP packet reaches zero.
- redirect - if there are in fact multiple router in one network, a more efficient route can identified, the default gateway can send a redirect message to the host to update its routing table. The router still delivers the original message.

**Using ping command line for analyzing network configuration**
- ping loopback address (127.0.0.1) to verify TCP/IP is installed and loaded correctly. *If it failed the TCP/IP protocol is not correctly installed in the local system*
- ping IP address of workstation to verify it was added correctly. *If it fails there might have been a configuration error or the network adapter could be faulty*
- ping the default gateway to make sure that you can communicate with a host on the local network. *If a host in local network can't be pinged then verify the sendin host's IP configuration such as subnet mask, IP address and so on*
- ping IP address of a remote host to verify you can communicate with hosts outside of the local network. *If it fails use tracert to investigate the route being taken*