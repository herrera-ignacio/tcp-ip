# Transport layer (TCP & UDP)

> Process-to-Process delivery. _Segmentation_, dividing message content into packets. Makes sure the packets (_message_) arrive in order and intact using flow control and error control. The transport-layer protocol that performs all of these functions is __TCP__.

Getting a packet to the destination system is not quite the same as determining which process should receive the packet's content.

A system can be running file transfer, email, and other network processes all at the same time, and all over a single physical interface. Naturally, the destination process has to know on which process the sender originated the bits inside the packet in order to reply.

Also, systems cannot simply transfer a huge multimegabit file all in one packet. Many data units exceed the maximum allowable size of a packet. The process of dividing message content into packets is known as __segmentation__.

The Network layer forward each and every packet indepdently, and does not recognize any relationship between the packets (is this a file transfer or email packet?). In contrast, the Transport layer can __make sure the whole _message_, often strung out in a sequence of packets, arrives in order__ (packets can be delivered out of sequence) __and intact__ (there are no errors in the entire message). This function involves some method of __flow control__ and __error control__.

The transport-layer protocol that performs all of these functions is __TCP__.

In many cases, the content of the packet forms a complete unit all by itself, called a __datagram__. Self-contained datagrams are not concerned with sequencing or flow control, and these functions are absent in the __User Datagram Protocol (UDP)__ at the Transport layer.

So, there are two very popular protocol packages at the Transport layer:

* __TCP__: connection-oriented, "reliable" service thar provides ordered delivery of packet content.
* __UDP__: connectionless, "unreliable" service that does not provide ordered delivery of packet contents.

In TCP/IP, it is often said that the Network layer (IP itself) offers an "unreliable" service, while the Transport layer adds "reliability" in the form of flow and error control.

> The Network layer gets a single packet to the right system, and the Transport layer gets the entire message to the right process.

![transport layer](./images/transport.png)

![process-to-process](./iamges/p-to-p.png)

Some of the functions that the Transport layer, which in some protocols are defined in a "end-to-end" layer, might include the following:

* __Process/Port addressing and multiplexing__: also known as "_Service-Point Addressing_", decide which process originated the message and to which process the message must be delivered.
* __Segment handling__: in cases where each message is divided into segments, each segment has a sequence number used to put the message back together at the destination.
* __Connection control__: Transport layer can be _connectionless_ which treats every data unit as a self-contained, independent unit, or _connection-oriented_ which goes through a three-phase process every time there is data to send to a destination after an idle period. First, some control messages establish the connection, then the data to be sent, and finally the connection is closed. Generally, segments are conneciton-oriented data units, and datagrams are connectionless data units.
* __Flow control__: prevent senders from overwhelming receivers.
* __Error control__: communications links are not the only source of errors, which can occur inside a system as well.
