# BGP: Border Gateway Protocol

BGP runs on links between the border routers and shares information about routes within autonomous services. It makes sure that every network and interface in any AS located anywhere on the Internet is reachable from every other place, and relies on an underlying IGP (or static routes) as the source of the BGP-distributed information.

## BGP and the Internet

BGP is the glue of the Internet. Generally, an ISP cannot link to another ISP unless both run BGP. 

Contrary to some claims, customer networks do not have to run BGP between their own networks and to their ISPs. Smaller customers especially can define a limited number of static routes provided by the ISP, and larger customers might be able to run IGP passively on the border router's ISP interface.
