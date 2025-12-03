To accommodate the goal of scalable and flexible network design, a network hierarchy is usually used. One common hierarchical network model is called Distributed Switching where a large network is divided in smaller groups that has their own task. As an example of this model, Cisco recommends designing a large enterprise network with four layers: access, distribution, core and data center.

**Access Layer**
Allows end-user devices such as computer, printers and smartphones to connect to the network. The important function of the access layer is to prevent the attachment of unauthorized devices. The layer is implemented by using wall ports for wired and access points for wireless. Switches deployed in this layer is usually called data switches.

**Distribution Layer**
A layer that is in between the access and core layer, which provides fault tolerant interconnections between different access blocks and either the core or other distribution blocks. The layer role is to implement traffic policies, such as routing boundaries, filtering or quality of service.

**Core Layer**
Provides highly available network backbone, any end-user devices should not be attached directly to the core layer. Its purpose is to provide redundant, and reliable traffic paths for data to continue to flow in the distribution and core layer. With only the access and distribution layer the network design is more like a mesh. Connections between distribution layer are made via the core layer, rather than interconnecting distribution layer switches directly.

**Data Center Layer**
A network area that main job is to host network services such as authentication, addressing, DNS), application servers and storage. It is usually connected with a fast bandwidth since it is important to make the services fast.

![[Pasted image 20251125134712.png]]