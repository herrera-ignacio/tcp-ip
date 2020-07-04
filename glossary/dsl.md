# DSL: Digital Subscriber Line

Family of technologies that are used to __transmit digital data over telephone lines__. In telecommunications marketing, the term DSL is widely understoon to mean _Assymmetric DSL_ (ADSL), the most commonly installed DSL technology for Internet access.

DSL can be delivered simultaneously with wired telephone service on the same telephone line since DSL uses higher frequency bands for data. On the customer premises, a DSL filter on each non-DSL outlet blocks any high-frequency interference to enable simultaneous use of the voice and DSL services.

In ADSL, data throughput in the upstream direction (to the service provider) is lower, hence the designation of asymmetric service.

## History

Originally designed for the “national net- works” that would offer everything that the Internet does today, but from the telephone company as part of the Integrated Services Digital Network (ISDN) initiatives of the 1980s, DSL was adapted for “broadband” Internet access when the grand visions of the telephone companies as content providers were reduced to the reality of a restricted role as ISPs and little more.

## PPP and DSL

The core of the issue is that ISPs needed some kind of tunneling protocol. Tunneling occurs when the normal mes- sage-packet-frame encapsulation sequence of the layers of a networking protocol suite are violated. When a message is placed inside a packet, then inside a frame, and this frame is placed inside another type of frame (or even another frame- packet-frame sequence), this is a tunneling situation. Although many tunneling methods have been standardized at several different TCP/IP layers, tunneling works as long as the tunnel endpoints understand the correct sequence of headers and content (which can also be encrypted for secure tunnels).

ISPs chose PPP as the solution for this role in DSL. Using PPP made perfect sense. For years, ISPs had used PPP to manage their WAN dial-in users. PPP could easily assign and manage the ISP’s IP address space, compartmentalize users for billing purposes, and so on. As a LAN technol- ogy, Ethernet had none of those features. PPP also allowed user authentication methods such as RADIUS to be used, methods completely absent on most LAN technologies.

## DSL Encapsulation

How are IP packets encapsulated on DSL links? DSL specifications establish a basic DSL frame as the physical level, but IP packets are not placed directly into these frames. IP packets are placed inside PPP frames, and then the PPP frames are encapsulated inside Ethernet frames (this is PPP over Ethernet, or PPPoE). Finally, the Ethernet frames are placed inside the DSL frames and sent to the DSL Access Module (DSLAM) at the telephone switching office. Once at the switching office, it might seem straightforward to extract the Ethernet frame and send it on into the “router cloud.” But it turns out that almost all DSLAMs are networked together by ATM, a technology once championed by the telephone companies. (Some very old DSLAMs use another telephone com- pany technology known as frame relay.) ATM uses cells instead of frames to carry information.
