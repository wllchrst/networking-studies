Similar to hubs, bridges is currently not being used in the modern network architecture, however the difference between a bridge and hub is segments on different bridge port are in separate collision domains but the same broadcast domain. Additionally bridges work at the Data Link layer because they use MAC Addresses. Below are the step by step of how bridge works:
1. Computer A sends a transmission to computer D, the frame contains the hardware address of computer source A and destination D.
2. The bridge listens to all traffic on all attached segments and consequently receives the transmission in port 1.
3. The bridge reads the destination address in the frame and based on the destination MAC Address the bridge find the information from the MAC Address table to find where should the frame be transmitted. If the MAC Address is not in memory, the bridge acts like a hub and floods the frame to all segments except for the source segment.

![[Pasted image 20251125081529.png]]