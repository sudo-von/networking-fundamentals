#### TCP/IP Model

##### Original

* Application.
* Transport.
* Internet.
* Link.

##### Current

* Application.
  * Defines communications between applications on two hosts.
* Transport
  * Maintains conversations between application processors on hosts. They use port numbers to track sessions.
* Network.
  * Data it's broken into packets which are manageable chuncks of data.
    * Source IP: 10.0.1.1 - Destination IP: 10.0.2.1
    * src: 7268, dst: 80
    * HTTP Data
    * ------------------------------------------------------
    * Source IP: 10.0.1.1 - Destination IP: 10.0.2.1
    * src: 7268, dst: 80
    * HTTP Data
  * The point of this layer is to make sure that data from one host can find its way to another host.
* Data link.
  * This layer is responsible for delivery traffic on a single network segment or LAN.
    * Source MAC: 02:1A:23:91:4B:C6 - Destination MAC: 02:54:28:DC:5A:12
    * Source IP: 10.0.1.1 - Destination IP: 10.0.2.1
    * Source Port: 7268, Destination Port: 80
    * HTTP Data, GET http://webserver.com
    * Ethernet trailer
  * If they are in different subnets we need a router, that means that the destination MAC will be the MAC of the router, and then the router will use the IP header, sets its own MAC as the source and then the next device as the destination.
  * If there are several routers, the frame will be rewritten several times along the way.
* Physical.
  * Physically transmitting and receiving data. There are many ways to do this, electrical, radio, light signals, etc. In any case the data is encoded and the bits are transmitted over the medium.