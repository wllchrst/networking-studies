Below are the guide and the explanation of each component of doing SVI configuration in the Virtual Local Area Network (VLAN) manner.

**Components and terminology explanation**
- Virtual Local Area Network is a way to split up network that is physically connected and in the same area virtually. This grouping is based on functional or security needs. The benefits of VLAN is improving network performance, enhance security by isolating traffic and simplify network management.
- Switch - layer 2 component, that is mainly responsible to connecting a lot of computers in the picture since switch has many ports.
- Switchport modes - specification for a network switch that determines whether the port it operates as an **access** port (for end devices like Personal Computers) or **trunk** port (connecting to other switches or routers)
- Multilayer switch - a component that has the functionality of a router & switch.

**Below are the configuration that is needed for each devices**
- **Computer** - each computer should have the IP Address in the right VLAN configuration
- **Switch** - Each interface of the port needs to be configured, mode for trunk to the interface heading to another switch, and mode access for the interface that is connected to the computer.
- **Multilayer Switch** - make each interface into trunk and configure the routing settings.

Commands to show information in switch and multilayer switch:
- `do sh run`
- `do sh vlan`
- `do sh trunk`


![[Pasted image 20251120134740.png]]

references from: 
https://www.youtube.com/watch?v=634muaHJegASw