# Multiplexing

Most TCP/IP hosts have only one TCP/IP stack process running, meaning that every packet passing into or out of the host uses the same software process. However, a host system typically runs many applications, and all these share the single network interface through multiplexing.

## Socket interface

Through sockets, TCP/IP process determine the source and destination application for the contents of an arriving segment.

Hosts use sockets to identify TCP connections and sort out UDP request-response pairs, and to make the coding of TCP/IP applications ieasier.
