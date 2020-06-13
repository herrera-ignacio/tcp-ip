# TCP/IP Protocol Suite

The Internet Protocol Suite is usually called TCP/IP after two of its most prominent protocols, but there are other protocols as well.

## Five Layers

TCP/IP _model_ is based on a __five-layer model for networking__. The stack is _open_, which means that there are no "secrets" as to how it works. Two compatible end-system applications can communicate regardless of their underlying architectures, although the connections between layers are not defined.

From botton (the link) to top (the user application), these are:

* Physical layer
* Link layer
* Network layer
* Transport layer
* Application layer

Not all layers are completely defined by the model, so these layers are "filled in" by external standard and protocols.

## Modules

TCP/IP stack is __comprised of modules__. Each mudle provides a specific function, but they are fairly independent.

TCP/IP layers contain relatively independent protocols that can be used depending on the needs of the system to provide whatever function is desired. Each giher layer protocol is supported by lower layer protocols. The whole collection of protocols forms a type of hourglass shape, with IP in the middle.

## OSI Reference Model

The __Open Standard Interconnection__ (OSI) reference model is a __seven-layer model__ that loosely maps into the five layers of TCP/IP. Until the Web became widely popular in the 1990s, the OSI reference model was proposed as the standard model for all communication networks. Today, is often used as a learning tool to introduce the functions of TCP/IP.

## Layers in Detail

Internet Protocol Suite assumes that a layer is there and available, so TCP/IP does not define the layers themselves. The stack consist of protocols, not implementations, so describing a layer or protocols says almost nothing about how these things should actually be built.

* Physical layer
* Link layer
* Network layer
* Transport layer
* Application layer

Not all systems on a network need to implement all five layers. Devices using the TCP/IP protocol stack fall into two general categories, a __host__ or __end system__, and an __intermediate node/system__. The intermediate nodes usually involve the first three layers.

Each implemented layer has an _interface_ with the layer above and below it, and provides its defined service to the layer above and obtain services from the layer below. In other words, there is a __service interface__ between each layer.

Services are provided to the layer above after the higher layer provides the lower layer with the command, data, and necessary parameters for the lower layer to carry out the task.

Layers on the same system provide and obtain services to and from adjacent layers. However, a __peer-to-peer protocol process__ allows the same layers on different systems to communicate. The term _peer_ means every implementation of some layer is essentially equal to all others. There is no "master" system at the protocol level. Communications between peer layers on different systems use the defined protocols appropriate to the given layer.

In other words:

* __Services__ refer to communication between layers within the same process.
* __Protocols__ refer to communications between processes.

## Protocols & Interfaces

It is important to note that __when layers of TCP/IP are on different systems, they are _only_ connected at the physical layer__. Direct peer-to-peer communication between all other layers is impossible. This means that all data from an application have to flow "down" through all five layers at the sender, and "up" all five layers at the receiver to reach the correct process on the other system. These streams of data are sometimes called a __Service Data Unit (SDU)__.

Each layer on the sending system adds information to the data it receives from the layer above and passes it all to the layer below, except for the Physical layer, that actually has to send the bits in a form appropriate for the communications link used.

Likewise, each layer on the receiving system unwraps the received message, often called a __Protocol Data Unit (PDU)__, with each layer examining, using, and stripping off the information it needs to complete its task, and passing the remainder up to the next layer, except for the Application layer, which passes what's left off to the application program itself.
