# Forwarding IP Packets

## Router Architectures

There are three main steps that a router must follow to process and forward a packet to the next hop.

1. Check an incoming packet for errors and other parameters.
2. Look up destination address in a forwarding table to determine proper output port for the packet.
3. Sending the packet out on that port.

But how are the input ports connected to the output ports? In smaller routers, which can even be implemented on laptop computers with two or more interfaces, software simply examines the packet headers and forward the packets where they need to go.

Small routers, such as those for DSL or small-edge LANs, can allow the incoming packet to sit in memory buffer and adjust header fields, perform tunnel encapsulation, and so on, and then queue the packet for output.

Instead of software-based forwarding architectures, larger routers use hardware-based forwarding fabric architectures.

## IPv6

There are two main strategies that have emerged for dealing with mixed IPv4 and IPv6 environments. These are _dual protocol stacks_ and _tunneling_.

### Dual Protocol Stacks

Hosts are capable of assigning both an IPv6 and IPv4 addresses to their network interface if they all implement a sort of 'split' IP network layer, that decides if packets should be handed off to the IPv4 process or to the IPv6 process.

### Tunneling

Tunneling occurs whenever the normal sequence of encapsulation headers is violated.

Normally, a message is broken up into segments, which are put inside packets placed inside frames that are sent as a sequence of bits to an adjacent system. The receiver usually expects that the frame contains a packet, and so on, but what if it doesn’t? Then the device is using tunneling.

Tunneling in a mixed IPv4 and IPv6 network is used to transport IPv6 packets over a series of IPv4 routers or to an IPv4 hosts.
