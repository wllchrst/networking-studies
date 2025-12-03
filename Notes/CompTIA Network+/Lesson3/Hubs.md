Hubs are no longer widely deployed in modern network architecture, as the hub role has been taken by switch. They are also known as multiport repeaters, where every port in the hubs is connected in the same collision domain. All communications are half-duplex, and it works at the physical layer on the OSI model. Hubs work by having internally wired with transmit (Tx) and receive (Rx) pairs for each port, the steps is like this:
- A node sends a frame on its Tx pair (obviously for transmitting the frame)
- The hub receives a weakened and distorted transmission using its Tx pair.
- The hub regenerates the transmission, performs a crossover and floods the regenerated frame through all the port on their Rx pairs.
- The server and other nodes receive the frame on their Rx pairs.

![[Pasted image 20251125081555.png]]