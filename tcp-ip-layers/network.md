# Network layer (IP)

> Delivers data in the form of a _packet_ from source to destination, across as many links as necessary, to systems that are not directly connected to the source, performing __fragmentation__ if needed, __routing__ by using __routing tables__ to store information about reachable systems, and __forwarding__ by using those tables for packet delivery.

The biggest difference from the Data Link layer is that the Data Link layer is in charge of data delivery between adjacent systems ("one hop awaay"), while the Network layer __delivers data to systems that are not directly connected to the source__.

How does the network layer know where the packet came from (so the sender can reply)? The key concept at the Network layer is the __network address__, whether an end system or intermediate system. It is important to realize that this network address is __different from, and independent of, the physical address__ used by frames that carry the packets between adjacent systems.

![network layer](./iamges/network.png)

A key issue is how the network addresses "map" to physical addresses, a processes known generally as __address resolution__. In TCP/IP a special family of address resolution protocols takes care of this process. __The network address is a logical address__, and should be organized so that devices can be grouped under a part of that address, in a fashion similar to a telephone number, for example, 212-555-1212 in the North American public switched telephone network (PSTN). The sender need only look at the area code or "network" portion of this address (212) to determine if the destination is local (area codes are the same) or needs to be sent to an intermediate system to react the 212 area code.

In TCP/IP, the network address is the beginning of the device's complete IP address. A group of hosts is gathered under the network portion of the IP address. IP network addresses, like area codes, are globally administered to prevent duplication, while the rest of the IP address is locally administered, often independently.

In some cases, the packet that arrives at an intermediate system inside a frame is too large to fit inside the frame that must be sent out This is not uncommon, different link and LAN types have different maximum frame sizes. The Network layer must be able to __fragment a data unit across multiple frames and eassemble the fragments at the destination__.

Network layer uses one or more __routing tables__ to store information about reachable systems. They must be created, maintained, and purged of old information as the network changes due to failures, addition or deletion of systems and links, or other configuration changes. This whole process is called __routing__, and the use of these tables for packet delivery is called __forwarding__. The __forwarding of packets always takes place hop by hop__.

In a very real sense, the Network layer is at the very heart of any protocol stack, and TCP/IP is no exception. __The protocol at this layer is _IP__, either IPv4 or IPv6.

![network layer](./images/network-layer.png)
