##### How TCP handles errors and uses windows

There can be data lost for many reasons.
These errors are generally detected by the datalink protocol like Ethernet
which will drop bad frames.
TCP and UDP can detect corruption by using the value in the checksum field but only TCP is considered reliable, UDP is considered unreliable, this is because TCP will manage retransmission of the lost data.

Windowing allows the sender to send a certain amount of data usually over multiple segments
and the receiver can send one single ack to cover all of them.

PC[1] --------- Bytes 100-199, 200-299, 300-399, ?, 500-599, 600-699, 700-799
Bytes 400-499 are missing...
The server sends an ack with 400 number and every frame from 400 bytes is resend
but there are other methods...

Selective acknowledgement.