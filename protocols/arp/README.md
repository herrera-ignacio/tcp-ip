# ARP - Address Resolution Protocol

Internet, or any internetwork, is made up of a combination of physical networks such as LANs and internetworking devices such as routers. A packet sent by a host might pass through several different physical networks before finally reaching its destination.

Hosts and routers at the Network Layer are identified by their network addresses. In TCP/IP this is the IP address. At the Data Link Layer, the interface that sends and receives frames is identified by the physical or hardware address, like 48-bit MAC address.

We need to map back and forth between addresses at the network and hardware levels. In TCP/IP this mapping, called __Binding__, is provided by the __Address Resolution Protocol__. ARP results are stored in an __ARP cache__ on a host so that the entire process does not have to be constantly repeated, and MAC table entries are purged periodically.

## ARP and LANs

ARP maps IPv4 addresses to Phyisical Addresses.  There are four different cases where ARP is used:

### Host to Host

ARP sender is a host and wants to send a packet to another host on the same LAN. In this case, the IP address of the destination is known and the MAC address of the destination must be found.

### Host to Router

ARP sender is a host and wants to send a packet to another host on a different LAN. A forwarding (routing) table is used to find the IP address of the router. In this case, the IP address of the router is known and the MAC address of the router must be found.

### Router to Router

ARP sender is a router and wants to forward a packet to another router on the same LAN. A forwarding (routing) table is used to find the IP address of the router . IP address of the router is known and the MAC address of the destination router must be found.

### Router to Host

The ARP sender is a router and wants to forward a packet to a host on the same LAN. IP address of the host is known and MAC address of the host must be found.

## In Detail

Suppose we start the LAN2 host `lnxclient` sneding a short message to host `winsrv2`. Because this is the first time that these devices have communicated in a long time, an ARP request is broadcast on LAN2 and the sender waits for reply.

An ARP reuest goes out as a broadcast frame with an all-zero MAC address field. It's looking for the MAC address that gores with the target IP address. The ARP reply frame returns the reply with the correct MAC address plugged into the all-zero field.

The devices that send the ARP requests cache the results, and the device that receives the ARP request usually also caches the MAC address in the arriving ARP request. The idea is that if one device in a pair sends in one direction, the other device in the pair will probably send in the opposite direction as well.

Entries in the ARP cache are deleted when no communication occurs with another device, usually after 300 seconds of silence between the devices. We can force the ARP cache to empty by using `arp -d -a`.

The common types of ARPs, host to host ARPs, are only used when the destination is on the same LAN subnet as the source.

## ARP Packets

ARP messages ride inside Ethernet frames, or any LAN frame, in exactly the same way as IP packets. There is no need to use an IP address here anyway, ARP frames are valid only for a particular LAN segment and never leave the local LAN (cannot be routed).

## Proxy ARP

Proxy ARP is an older technique (it was called the "ARP Hack") that was used in early routers, and is still supported in some routers today. LANs connected y bridges had hosts that did not (and could not) use different IP network addresses. 

## ARP and IPv6

IPv6 really has no need for a separate ARP function. Instead, the _Neighbor Discovery Protocol (ND or NDP)_. ND is really a superset of most of the functions of IPv5's ARP, ICMP Redirect, and ICMP Router Discovery features. This

### ICMPv6

The address resolution process in IPv6 uses ICMPv6 messages and is part of the _Neighbor Discovery (ND) process_. Generally, a multicast Neighbor Solicitation message is sent and a unicast Neighbor Advertisement message is received in reply.

### Neighbor Discovery Protocol

NDP is the way that IPv6 hosts and routers find things out about their immediate neighborhood, typically the LAN segment.

NDP functions are performed only for local IPv6 addresses, and unlike ARP, are not broadcast ("Everyone pay atention to this") but rather multicast ("Only those interested pay attention to this").
