# Protocol

> Computer networks enable communication between processes on two different devices that are capable of sending and receiving information in the form of bits (0s and 1s). Processes that exchange bit streams must agree on a _protocol_.

__A protocol is a standard or convention__ that enables and controls the connection, communication, and transfer of information between two communications endpoints, or hosts.

A protocol __defines the rules__ oberning the syntax (what can be communicated), semantics (how it can be communicated), and synchronization (when and at what speed it can be communicated) of the communications procedure.

Protocols can be implemented on hardware, software, or a cambination of both.

> Protocols are not the same as standards. Some stardards have never been implemented as workable protocols, while some of the most useful protocols are only loosely defined.

Most of the protocols specify one or more of the following:

1. __Physical connection__: host typically uses different hardware depending whether the connection is wired or wireless. Protocols are used to supply details about the network configuration.
2. __Handshaking__: rules for the initial exchange of information across the network
3. __Negotiation of parameters__: series of actions to establish the rules and limits used for communicating across the network.
4. __Message delimiters__: what will constitute the start and end of a message on a network.
5. __Message format__: how the content of a message is structured, usually at the "_field_" level.
6. __Error detection__: how the receiver can detect corrupt messages, unexpected loss of connectivity.
7. __Error correction__: what to do about error situations. Note that _error recovery_ usually consists of both error detection and error correction protocols.
8. __Termination of communications__: rules for gracefully stopping communicating endpoints.

## The importance of Protocols

Protocols at various layers provided the abstraction necessary for Internet success. Application developers did not have to concern themselves overly with the physical properties of the network. Expanded use of communications protocols has been a major contributor to the Internet's success, acceptance, flexibility, and power.

## Standards and Organizations

Standards provide essential guidelines to manufacturers, vendors, service providers, consultants, government agencies, and users to make sure the interconnectivity needed today is there.

Data communication standars fall into two major categories:

* __De Jure__: approved by an officially recognized body whose job is to stadardize protocols and other aspects of networking. Often have the force of law, even if they are called _recommendations_.
* __De Facto__: have _not_ been formally approved but are widely followed.

### Internet Protocols

When it comes to the _Internet Protocols_, there are very few official standards, and there are no penalties involved for not following them.

The standards for the TCP/IP protocol suite now come from the __Internet Engineering Task Force (IETF)__, working in conjunction with other organizations. There is no force of law behind Internet standards.

Other important organizations are __Institute of Electrical and Electronic Engineers (IEEE)__, involved in all aspects of wireless LANs (IEEE 802.11), __American National Standards Institute (ANSI)__, that determines what bits mean, __Electronic Industries Associaton__, __International Standards Organization (ISO)__, __International Telecommunications Union__, and more...
