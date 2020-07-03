# IGP: Interior Gateway Protocol

Type of protocol used for exchanging routing information between gateways within an autonomous system.

Routers initially know only about their immediate environments. They know the IP addresses and prefixes configured on their local interfaces, and at most a little more statically defined information.

So routers offer to and ask their neighbor routers (adjacent routers one hop away) about the routing information they know. Little by little, each router then builds up a detailed routing information database about the TCP/IP network.

For this they use __routing protocols__. IGPs run between the routers inside a single routing domain, our autonomous system. IGPs do not share information learned across AS boundaries except physical interface addresses if necessary.

## Three major IGP

* RIP: Routing Information Protocol (_distance vector_)
* OSPF: Open Shortest Path First (_link-state_)
* IS-IS: Immediate System-Intermediate System (_link-state_)

### RIP: Routing Information Protocol

Often declared obsolte, is still used and remains a routing protocol for small networks.

RIP is a _distance-vector_ routing protocol, meaning it makes decisions based on one thing: how many routers (hops) are there between here and the destination. Link speeds do not matter, nor does congestion near another router. To RIP, the 'best' route always has the fewest number of hops.

### OSPF: Open Shortest Path First

Link-state protocol with a set of metrics that can be used to reflect much more about a network than just the number of routers encountered between source and destination. In OSPF, a router attempts to route based on the 'state of the links'.

### IS-IS: Immediate System-Intermediate System

Other common link-state routing protocol. 

If is used instead of OSPF as an IGP within an AS, there must be strong reasons for doing so as it is an ISO protocol that bas been adapted/_integrated_ for IP in order to carry IP routing information inside non-IP packets.

IS-IS packets are ConnectionLess Network Protocol (CLNP) packets, that have ISO addresses, not IP source and destination addresses.

It is more complex but also much more flexible.
