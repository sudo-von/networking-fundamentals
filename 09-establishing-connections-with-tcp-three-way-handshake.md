##### Establishing connections with TCP's three way handshake

Flags in the TCP header are bits that may be turned on or off.

* URG.
* ACK.
* PSH.
* RST.
* SYN.
* FIN.

The devices starts the conversation (client) sending a segment to the server, only headers, no payload.
In the TCP header the SYN flag is turned on, this is short for syncrhonized, this tells the server that we want to start a new connection and we need to aggree on a few details.

Source and destinations ports...
The source port will be random and the destination will be a well known number.
Then the initial sequence number or SYN is also set. This helps both devices to keep track of which order the segment's should be proccessed in. This usually starts as a randomized value but that's usually done for security.
A window value is also set.
If the server has an application listening on port 80, then it will agree to this conversation so it will responde by sending an empty TCP segment. The TCP header of the source and destination ports will switch. 
The sequence number will go up by one as in the next message in the conversation and finally the SYN and AKF flags are bot set.
I have seen your request for a conversation and i agree to it (ACK flag).
The client sends an empty TCP segment with the ACK fieldset and the sequence number is incremented again. This is the client confirming that it received the service last message.
The SYN, SYN/ACK and ACK are tge tgree way handshake that TCP uses to build a connection.

To close the connection there is another path:

FIN (Finished).

1.- First pair of messages to start the process.
2.- The application is notified, which may take a while.
3.- The second pair finish the process.

- FIN/ACK
ACK -

FIN/ACK -
- ACK

RST (Reset)
RST messages help with troubleshooting.