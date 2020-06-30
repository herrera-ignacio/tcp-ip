# ICMP: Internet Control Message Protocol

We know IP is a connectionless or _unreliable_ method of packet delivery. __IP has a built-in error reporting protocol__, the _Internet Control Message Protocol_ (ICMP). Note that ICMP does not deal with error messages but 'control messages'.

## ICMP and Ping

The easiest way to look at ICMP is with `ping` and `tracerout`.

Ping utility is just a way to __bounce packets off a target device and see if it is there__, that is, it has the IP address that was provided, is powered on, and alive. The device might still not function in the correct way, but at least the device is present and accounted for.

Ping employs messages in request-reply pairs using the ICMP protocol. An _Echo request_ is sent out which basically tells the receiver to _send an ICMP Echo message back_. Once the reply is received, the next request is sent, statistics compiled as the procedure goes along, and so on.

__Firewalls sometimes screen out ICMP messages__ in the name of security. A well-known Denial of Service (DoS) attack called the _Ping of Death_ uses malformed (usually enormous) and fragmented ping packets to disrupt a target. In these cases, even a failed ping does not prove that a device is not working properly and diagnostics become more complex.

## Traceroute

Traceroute is not an ICMP-based network utility in the same sense that ping is. However, traceroute uses ICMP messages to perform its functions, and for many people the next step after ping is traceroute.

After ping has been used to verify that an IP address is reachable over the network, the next logical step is to __determine _how_ the packets make their way to the destination and back__. In other words, we would like to trace the route from source to destination. IP networks route around failures and routing tables can change, but paths are usually stable on the order of hours if not days when things are not going completely haywire.

Traceroute implementations vary even more than those for ping. Some have graphical displays and use other Internet utilities to display location and administrative information about the routers and networks unconvered. This in turn has made many network administrators so nervous that they routinely block traceroute ICMP messages with firewalls or route filters to hide topology details.