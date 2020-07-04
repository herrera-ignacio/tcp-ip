# NAT: Network Address Translation

Method of remapping IP address space into another by modifying network address information in the IP header of packets while there are in transit across a traffic routing device.

The technique was originally used to avoid the need to assign a new address to every host when a network was moved, or when the upstream Internet Service Provider (ISP) was replaced, but could not route the networks address space.

It has become a popular and essential tool in conserving global address space in the face of _IPv4 Address Exhaustion_. One internet-routable IP address of a NAT gateway can be used for an entire private network.

## IP Masquerading

Technique that hides an entire IP address space, usually consisting of private IP addresses, behind a single IP address in another, usually public address space. The hidden addresses are changed into a single public IP address as the source address of the outgoing IP packets so they appear as originating not from the hidden host but from the routing device itself.

Because of the popularity of this technique to conserver IPv4 address space, the term NAT has become virtually synonymous with IP masquerading.

## One-to-one NAT

The simplest type of NAT provides a one-to-one translation of IP addresses, also called _one-to-one NAT_.

## One-to-many NAT

Majority of NATs map multiple private hosts to one publicly exposed IP address.

As traffic passes from the local network to the Internet, the source address in each packet is translated on the fly from a private address to the public address. The router tracks basic data about each active connection (particularly the destination address and port). When a reply returns to the router, it uses the connection tracking data it stored during the outbound phase to determine the private address on the internal network to which to forward the reply.

