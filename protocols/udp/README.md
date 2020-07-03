# UDP: User Datagram Protocol

The data unit of UDP is not a packet, but a __datagram__, the content of a conectionless packet.

The simple and fast operations of UDP makes it ideal for delay-sensitive traffic like voice samples, multicast digital video, other types of streaming and 'real-time' traffic.

This use of DP is not as originally intended, and there are other things that need to be done before UDP is ready for voice and video.

UDP is used by many common network applications, including DNS, IPTV streaming media applications, voice over IP (VoIP), Trivial File Transfer Protocol (TFTP), and online games. UDP is required for multicast applications.

## What UDP is For

 UDP is defined as __stateless__ (no session information is kept by hosts) and __unreliable__. This does not mean that UDP traffic is somehow lower priority on the network or through routers, it just means that if the application using UDP needs to keep trac of a session history or guarantee deliver then the __application_ itself must do it, because UDP can't and won't.

 There is a whole class of applications that use UDP, some almost exclusively. These are applications that are invoked to exchange quick, request-response pairs of messages, such as DNS.

 Multicast allows one source to send a single packet stream to multiple destinations (TCP is strictly a one-source-to-one-destination protocol), so UDP must be used for multicast data transfer as well.

 In other words, UDP is a __low-overhead__ transport for applications that do not need, or cannot have, the 'point-to-point' connections or guaranteed delivery that TCP provides.
 