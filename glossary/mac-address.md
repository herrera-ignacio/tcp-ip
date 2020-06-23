# MAC Address

The MAC addresses used in 802 LAN frames are all 48 bits (6 bytes) long. The first 24 bits (3 bytes) are assigned by the IEEE to the manufacturer of the NIC (manufacturers pay for them). This is the Organizationally Unique Identifier (OUI). The last 24 bits (3 bytes) are the NIC manufacturer’s serial number for that NIC. Some protocol analyzers know the manufacturer’s ID (which is not pub- lic but seldom suppressed) and display this along with the address. This is how Ethereal displays MAC addresses not only in hex but starting with “Intel_” or “Juniper_.”.

LAN implementers and vendors quickly saw that the IEEE 802.3 hardware arrangement was more flexible (and less expensive) than DIX Ethernet. They also saw that the DIX Ethernet II frame structure was simpler and could carry slightly more user data than the complex IEEE 802.3 frame structure. Being practical people, the vendors simply used the flexible IEEE 802.3 hardware with the simple DIX Ethernet II frame structure, creating the mixture that is commonly seen today on most LANs.

Today, just because the hardware is IEEE 802.3 compliant (e.g., 100BaseT), does not mean that the frame structure used to carry IP packets is also IEEE 802.3 compliant. The frame structure is most likely Ethernet II.
