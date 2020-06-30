# Routing

Internet is the largest router-based network in the world. The most essential network nodes are routers and not bridges or switches or any other exotic device. This does not mean that there are not nother types of network devices. It just means that __routing is the most important function in moving packets from source to destination__.

## Roting Table and Forwarding Table

There are two different types of network tables used in routers and hosts.

The Routing Table holds all the information that a device knows about network addresses and interfaces, and is usually held in a fairly user-friendly format.

The Forwarding Table is usually a machine-coded internal table that contains the routes actually used by the device to reach destinations. In most cases, the Routing Table holds more information than is distilled into the Forwarding Table.

## Routing

Routing is done entirely with IP addresses. A host can use _Direct Delivery_ to send packets directly to another host, perhaps using a VLAN, or use _Indirect Delivery_ if the destination host is reachable only through a router.
