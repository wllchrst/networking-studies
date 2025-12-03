As a network engineer, the profession is usually expected to monitor network performance and response time. The manner in which data is being transmitted between nodes on a network can significantly affect network performance, hence understanding transmission methods is important.

**Signaling and Modulation**
Transmission medium is the physical channel which signals travel allowing nodes to communicate with each other. Different types of transmission media can be classified as two:
- Cabled - physical signal conductor usually mentioned as **bounded media**.
- Wireless - uses free space between nodes, such as microwave radio. Usually called as **unbounded media**.

**Bandwidth, BAUD, and Bit rate**
Bandwidth is the range of frequencies available to the communications channel. Digital signaling typically uses baseband transmission, meaning the complete bandwidth is available to a single transmission channel.

When used to discuss channel capacity, bandwidth is measured in units of of time called hertz (Hz), representing the number of signaling cycles that can be completed in a second. However, the usual way of communicating bandwidth in data communications is by **baud and bit rate**.

A signal transmitted over a communications channel consists of a series of events is referred as **symbols**. The number of symbols that can transmitted in a second is called **baud rate**. On the other side, **bit rate** is the amount of bits that can be transmitted in a second.

**Distance Limitation, Attenuation, and Noise**
Each type of media consistently support a given **data rate** only over a defined **distance**. Attenuation and noise enforce distance limitations on different media types.
- Attenuation - loss of signal strength expressed in decibles, which is usually in the case of networking signal strength at the start and destination.
- Noise - anything that gets transmitted but not the actual signal that is first intended to be transmitted. This can cause errors in data and forcing retransmissions.

**Transmission Media Types**
- Copper cable - used to transmit electrical signals. The cable between two nodes creates a low voltage electrical circuit between two nodes. Two main types of copper cable are twisted pair and coaxial. Unfortunately there is some degree of impedance in the copper conductor, hence resulting in high attenuation, meaning signal loses strength over long links.
- Fiber optic cable - carries very high frequency radiation in the infrared light part of the electromagnetic spectrum, it is usually better compared to coper cable, electrical signals are susceptible to interference and dispersion. Fiber optic supports higher bandwidth over longer links than copper cable also.
- Wireless radio - radio frequency (RF) waves can propagate through the air between sending and receiving antennas.
