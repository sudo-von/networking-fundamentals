##### How TCP and UDP work?

When an application starts it uses a random source port from (1024 to 65535).
The important part is that this port number is not already in use on the device.

Random ports: 1024 - 65535
Well-known ports: 0 - 1023

Multiplexing is a way for one host to have several applications accesing the network at once.

##### 5 Tuple

Local IP | Remote IP | Local Port | Remote Port | Protocol
 172.16.0.1 | 10.0.0.1 |    80    |     34761   |   TCP

netstat -ano

##### TCP

Additional features.
TCP is connection oriented.
Error recovery.
Windowing (flow control).
Ordered data delivery.

* Source Port - Destination Port
*        Sequence Number
* Acknowledgement Number
* Data Offset - Reserved - Flags - Window
* Checksum                       - Urgent Pointer
* Options                               - Padding

##### UDP

Lightweight
UDP is connectionless.
Does not care about errors.
Does not care about order.
Great for voice or video applications (real time).

* Source Port - Destination Port
* Length      - Checksum

##### Quiz

Quiz # 1 Which Protocols use each of these headers? TCP & UDP
Quiz # 2 What is a socket used for? The sockets are used to identify which application to the network data belongs to. 
Quiz # 3 What detail contained in the socket? 5 tuple; Local IP; Remote IP; Local Port #; Remote port #; Protocol (TCP/UDP).
Quiz # 4 Why use UDP? It's used for real time applications like audio and video stream, where speed is much more important than reliability. The retransmission of voice e.g. would end up in a not understandable chaos, where else a lacking packet of UDP just causes a break of less than a second.