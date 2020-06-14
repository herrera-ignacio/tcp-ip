# Protocol Data Units

The names of the Protocol Data Units used at each TCP/IP layer is worth reviewing.

* __Network layer__: _frame_, inside of the frame is the data unit of IP, the _packet_.
* __Tranposrt layer__: _segment_ in TCP and _datagram_ in UDP, by definition is the content of the information-bearing packet.
* __Aplication layer__: applications exchange messages, segments and datagrams taken together form the messages that the applications are sending to each other.
