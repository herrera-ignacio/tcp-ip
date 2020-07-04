# DHCP: Dynamic Host Configuration Protocol

DHCP is a __network management protocol__ used on IP networks whereby a DHCP server __dynamically assignas an IP address and other network configuration parameters to each device on a network so they can communicate with other IP networks.

A DHCP server enables computers to request IP addresses and networking parameters automatically from the _Internet Service Provider (ISP)_, reducing the need for a network administrator or a user to manually assign IP addresses to all network devices.

A router or a residential gateway can be enabled to act as a DHCP server. Most residential network routers receive a globally unique IP address within the ISP network, and within a local network, a DHCP server assigns a local IP address to each device connected to the network.

## Usage

We want to dynamically assign host addresses.

We'll need a server (it can be a linux server) to work as a DHCP server for the IP address ranges desired. It provides TCP/IP a measure of mobility.

With the proper DHCP servers available, a user could unplug a host from one Ethernet LAN subnet, move it across the country, plug it into another subnet, expect the configuration data to be loaded properly, and become productive on the new subnet immediately.
