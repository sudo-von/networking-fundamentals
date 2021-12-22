#### How the OSI model works?

Remember... <small>Please Do Not Throw Sausage Pizza Away...</small>

* Application
  * Applications acces the network
    * Web browsing.
    * Email.
    * File transfers.
    * Management sessions (SSH, Telnet, RTP).
* Presentation
  * Data conversion and formatting
    * This conversion may also include services like encryption and compression.
    * File formats also live here including images and video files.
* Session
  * Creates a session between applications
* Transport
  * Transports data between processors on to endpoints.
  * TCP and UDP are the most common protocols used in this layer
  * Breaks data into segments. Generally we call this block of data a segment, technically if you are using TCP each block is called a segment but if you are using UDP each block is called a datagram.
  * This layer adds a header with the src and destination ports.
* Network
  * Adds network addresses.
  * Adds routing.
  * This layer adds another header in the case of IP this includes the source and destination addresses, once this is done the block of data is now called a packet.
* Data Link
  * Creates a logical link between devices.
  * Adds another layer with the local addresses. In the case of ethernet includes the source and destination mac's.
  * Trailer may also be added with error correction information.
  * Once the header and trailer are added this block is now called a frame.
  * Contains LLC and MAC sublayers.
* Physical
  * Manages physical network components.
  * Encodes data into physical signals.