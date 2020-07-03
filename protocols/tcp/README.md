# TCP: Transmission Control Protocol

TCP establishes end-to-end connections over the unreliable, best-effort IP packet service using a special sequence of three TCP segments sent from client to server and back called a _three-way handshake_. 

The protocol uses unique terminology for the connection process. A single bit called the __SYN__ (synchronization) bit is used to indicate a connection request.

Connections and data segments are acknowledged with the __ACK__ bit, and a request to terminate a connection is made with the __FIN__ bit.

## Connection establishment

The normal TCP connection establishment's three-way handshake establish three important pieces of information that both sides of the connection need to know:

1. ISNs to use for outgoing data.
2. Buffer space available locally for data, in bytes.
3. Maximum Segment Size (MSS) that sets the largest segment that the local host will accept.

TCP's three-way handshake has two important functions:

1. Makes sure both sides know that they are ready to transfer data
2. Allows both sides to agree on the ISN, which are sent and acknowledged during the handshake.
