# Routing and Peering

## Routing Protocols

A __routing protocol__ is run on a router (and can be run on a host) to __allow the router to dynamically learn about its network neighborhood and pass this knowledge on__, until every router has built a consistent view of the network 'map' and the least cost ('best') place to forward traffic toward any reachable destination.

Until the protcol _converges_ there is always the possibility that some routers do not have the latest view of the network and might forward packets incorrectly.

## Routing Policies

A __routing policy__ can be defined as a __rule implemented on the router to determine the handling of routing protocol information__. This is intended to minimize the effects of malicious users.

The term should not be confused with __policy routing__.

## Policy Routing

Policy routing is usually defined as the __forwarding of packets based not only on destination address, but also on some other fields in the TCP/IP header__.

Confusingly, policy routing can be made more effective with routing policies.

