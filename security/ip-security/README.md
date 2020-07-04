# IPSec: Internet Protocol Security

Secure network protocol suite that __authenticates and encrypts the packets of data to provide secure encrypted communication between two computers over an IP network__. It is used in Virtual Privated Networks (VPNs).

IPSec is part of a public key infrastructure (PKI) based on several things such as public key encryption, secure key exchange for the Internet (IKE), and several related concepts and protocols. It includes protocols for establishing mutual authentication between agents at the beginning of a session and negotiation of crpyotgraphic keys to use during the session.

Support for IPSec is optional in IPv4 but mandatory in IPV6.

IPSec consists of two main 'core' protocols, AH and ESP.

## AH

Allos a receiver to verify that the claimed originator of the message actually did send it, and that none of the data has been altered while in transit.

It also prevents captured messages from being used again in the future (.e., when a hacker cannot read the password but knows that this packet will log in the user when sent). This is called a _replay_ attack.

## ESP

ESP encrypts the payload of the message itself.

Separating this encryption process from the authentication process, although in practice are normally used together, allows them to evolve independently, so advances in encryption do not require changes in authentication and vice versa.

