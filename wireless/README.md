# Wireless LANs and IEEE 802.11

Wireless technologies are the fastest-growing form of link layer for IP packets, whether for cell phones or home office LANs.

The basic components of the IEEE 802.11 wireless LAN architecture are the wireless stations, such as a laptop, and the access point (AP). The AP is not strictly necessary, and a cluster of wireless stations can communicate directly with each other without an AP. This is called an IEEE 802.11 inde- pendent, basic service set (IBSS) or ad hoc network. One or more wireless sta- tions form a basic service set (BSS), but if there is only one wireless station in the BSS, an AP is necessary to allow the wireless station to communicate. An AP has both wired and wireless connections, allowing it to be the access “point” between the wireless station and the world. In a typical home wireless network (an arbitrarily low limit), one BSS supports up to four wireless devices, and the AP is bundled with the DSL router or cable modem with the high-speed link for Internet access. (The DSL router or cable modem can have multiple wired connections as well.) In practice, the number of systems you can connect to a given type of AP depends on your performance needs and the traffic mix.

## Wi-Fi

An intended interoperable version of the IEEE 802.11 architecture is known as Wi-Fi, a trademark and brand of the Wi-Fi Alliance. It allows users with properly equipped wireless laptops to attach to APs maintained by a service provider in restaurants, bookstores, libraries, and other locations, usually to access the Internet.

If there are APs present, each wireless station in IEEE 802.11 needs to associ- ate with an AP before it can send or receive frames. For Internet access, the 802.11 frames contain IP packets, of course. The network administrator for every AP assigns a Service Set Identifier (SSID) to the AP, as well as the channels (fre- quency ranges) that are associated with the AP. The AP has a MAC layer address as well, often called the BSSID.

The AP is required to periodically send out beacon frames, each including the AP’s SSID and MAC layer address (BSSID), on its wireless channels. These channels are scanned by the wireless station. Some channels might overlap between multiple APs, because the “WiFi Jungle” has no central control, but (hope- fully) there are other channels that do not. In practice, interference between over- lapping APs is not a huge problem in the absence of a high volume of traffic.

After selecting an AP by SSID, the wireless host uses the 802.11 association protocol to join the AP’s subnet. The wireless station then uses DHCP to get an IP address, and becomes part of the Internet through the AP.

## IEEE 802.11 Mac Layer Protocol

IEEE 802.11 defines two MAC sublayers: the distributed coordination function (DCF) and the point coordination function (PCF). The PCF MAC is optional and runs on top of the DCF MAC, which is mandatory. PCF is used with APs and is very complex, while DCF is simpler and uses a venerable access method known as carrier sense multiple access with collision avoidance (CSMA/CA).

Note that while Ethernet LANs detect collisions between stations sending at the same time with CSMA/CD, wireless LANs avoid collisions. Collision detection is not appro- priate for wireless LANs for a number of reasons, the most important being the _hidden terminal problem_.

## The IEEE 802.11 Frame

Although the IEEE 802.11 frame shares a lot with the Ethernet frame (which is one reason some packet sniffers can parse wireless frames as if they were Ethernet), there are a number of unique fields in 802.11.
