# IPv4 & IPv6 Addressing

Today it is the most common by far to assign IP addresses automatically with the Dynamic Host Configuration
Protocol, or DHCP. Routers can use DHCP as well. We’ll look at DHCP in a later chapter.

You can manually assign IP address, using a different interface based on the OS.

## Network/Host Boundary

Allow the network/host boundary in IPv4 and IPv6 addresses to be set almost anywhere (there are still some basic rules). When applied to the former, fixed, IPv4 octet boundaries, if you moved the “natural” boundary of the mask to the right of its normal position, this was called subnet- ting and the address space gets smaller. (Actually, even the older “natural” IPv4 addresses could always be subnetted.) And if you moved the “natural” boundary of the mask to the left of its normal position, this was called supernetting and the address space became larger.

## Public/Private

IP addresses, both IPv4 and IPv6, can be public or private. Public network address spaces are assigned by a central authority and should be unique. Private network addresses are very useful, but are not guaranteed to be unique. Therefore, the use of private network address spaces has to be carefully managed, because routers on the Internet would not work properly if a LAN showed up in two places at the same time. Nevertheless, the use of private address spaces in IP is popular for perceived security reasons. The security aspects are often overempha- sized: The expansion of the locally available address space is the key reason for private address use. (If you have one IP address and three hosts, you have a prob- lem without private addressing.) But private address spaces must be translated to public addresses whenever a packet makes it way onto the global public Internet.

Moreover, private IP addresses are not routable outside a local network, so a router is not allowed to advertise a route to a private address space onto the pub- lic Internet. Note that private addresses are just as routable as public ones within your own network (as on the Illustrated Network), or by mutual consent with another party. They are not generally routable on the global public Internet due to their lack of uniqueness and usual practices.

Almost all networks today rely on private network addresses to prevent public IPv4 address exhaustion, so these addresses are not just to test networks and labs any longer.

## IPv4 Address

The IPv4 address is a network layer concept and has nothing to do with the addresses that the data link layer uses, often called the hardware address on LANs. IPv4 addresses must be mapped to LAN hardware addresses and WAN serial link addresses. However, there is no real relationship between LAN media access control (MAC) or WAN serial link addresses in the frame header and the The IPv4 Address 147 IPv4 addresses used in the packet header, with the special exception of multicast addresses.

The original IPv4 addressing scheme established in RFC 791 is known as classful addressing. The 32 bits of the IPv4 address fall into one of several classes based on the value of the initial bits in the IPv4 address. The major classes used for addresses were A, B, and C. Class D was (and is) used for IPv4 multicast traf- fic, and Class E was “reserved” for experimental purposes. Each class differs in the number of IPv4 address bits assigned to the network and the host portion of the IP address.

### Understanding IPv4 Address

IP addresses and their prefixes are read in a certain way and have special mean- ings depending on how they are written and used. For example, the classful IPv4 address 192.168.19.48 is read as “host 48 on IP network 192.168.19.0.” In a classless environment, as on a router, the prefix length, in this case /24, must be known. Routers often drop trailing zeros, 192.168.19.0/24 is the same as 192.168.19/24, in this case /24 refers to the subnet mask, it indicates the first 24 bits of the address are masked (255.255.255.0), and are part of the Network Number, while the remaining 8 bits are part of the host address, this is known as CIDR format. All IP network addresses must have the bits in the host address field set to 0 and this address cannot be assigned to any host.

![ipv4](./ipv4.png)

## IPv6 Address
