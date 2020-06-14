# Ports & Sockets

Frames are sent on LANs and inside a frame are _packets_, which carry the information from device to device. The information can be application data, but there are also packets that perform control and administrative tasks as well as data transfer.

There is usually only one network interface on a host, so all applications must share this common interface, which has the _Network Address_ (IP). How are arriving packets being distributed to the proper application?

## Ports

The Transport layer Protocol that should process the information inside the packet is indicate by the value in the __protocol field of the IPv4 header__. Inside the Tranposrt layer data unit, the __receiving application is indicated by the Port number in the transport layer header__. By looking at the _Protocol_ and _Port_ fields, the TCP/IP stack at the destination knows which application gets the inforamtion. If two applications try to use the same port at the same time, this is an error condition.

## Sockets

A __Socket is the combination of the IP address and Port number__, and this combination will uniquely identify an application.

The socket is also the way that programmers often write networking applications, using the socket as a kind of entry point to the other layers of the protocol stack.
