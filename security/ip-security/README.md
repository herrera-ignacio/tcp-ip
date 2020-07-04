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

## IPSec vs SSL/TLS

IPSec typical usage is LAN to LAN and Client to LAN thus forming an encrypted tunnel over some untrusted network like the Internet (VPNs). Once traffix exits the IPSec tunnel, it goes to its destination as unprotected clear text.

HTTPS (TLS) encrypts client to server and provides end-to-end protection regardless of the underlying network.

They perform __different functions__.

The purpose of IPsec is to give the remote computer direct access to the central network, making it a full member. Remote users have access to any file storage locations, programs, printers, and backups, exactly as if they were in the office. IPsec is therefore a robust system that gives users whatever resources they need, wherever they are located.

SSL VPNs work by accessing specific applications whereas IPsec users are treated as full members of the network.

Beyond security concerns, it’s also crucial to think about what services VPN users will need to access. If they will only be using web-based applications like email and cloud storage, SSL may be the right choice. Remote users can quickly connect to the applications they use without being confused by the ones they don’t. This makes SSL ideal for clients and freelance employees. But if users require full access—such as central office team members who are traveling—IPsec is the way to go. IPsec VPNs give users the ability to do whatever they can normally do while sitting in the main office from wherever they are.
