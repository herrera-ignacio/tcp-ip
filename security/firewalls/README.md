# Firewalls

Technique for adding security to TCP/IP and the internet. They can be hardware or software designed to protect individual hosts, clients, servers, or the entire LANs.

## Type of firewalls

There are lots of different firewall configurations.

The three major types of firewalls are:

* Packet filters
* Application proxy
* Stateful inspection

### Packet Filters

Packet filters establish site security access rules (or _policies) that examine the TCP/IP header of each packet and decide if it should be allowed to pass through the firewall.

Policies can and usually differ for inbound and outbound packets.

### Application Proxy

Proxy sits between protected network and rest of the world. Every packet sent outbound is intercepted by the proxy, which initiates its own request and processes the response. Thus, clients and servers never interact directly and the entire contect of the packet can be inspected byte by byte if necessary.

### Stateful Inspection

Simple packet filters do not maintain a history of the streams of packets, nor do they know anything about the relationship between sequential packets. They cannot detect flows or more sophisticated attacks that rely on a sequence of packets with specific bits set.

In contrast to stateless firewall filter that inspects packets singly and in isolation, stateful filters __consider state information from past communications and applications to make dynamic decisions__ about new communications attempts. To do this, stateful firewall filters look at flows or conversations established.
