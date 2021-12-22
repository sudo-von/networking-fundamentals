#### How IP addresses work?

IPv4: 192.168.0.100
IPv6: FD3B:F15C:C672:34B8::100

Each of these numbers (IPv4) is called an octet as each number is an 8 bit value and 8 bits means that these numbers can be in a range from 0 to 255.

* 0000 0000 = 0
* 1111 1111 = 255

##### IP addresses are two addresses in one

1.- Host address.
2.- Network address.

Example: 
172.16.0.1

172.16 = Network.
0.1 = Host address.

You are probably wondering... is it always the first half of the address that represents the network?
Short answer, no.

#### Classful Networks

1.2.3.4

1 = Network, 0-255 = 256 networks.
2.3.4 = Host, 24 bits = 16,777,215 hosts.

### Five classes

A: Devices
B: Devices
C: Devices
D: Multicast
E: Reserver

Class A: 1.2.3.4
1 = Network, 0000 0001, however the first bit of the network is always 0, that leaves seven bits for us to allocate to our networks.
2.3.4 = Host

Class B: 129.2.3.4
129.2 = Network, 1000 0001, the first two bits of the network are always 10 which leaves 14 bits or 16384 networks.
3.4 = Host

Class C:
130.2.3.4
130.2.3 = Network, the first three bits are always 110 leaving 21 network bits or a little over 2 million networks.
4 = Host

#### Resume

* Class A: One octet minus 1 bit
* Class B: Two octets minus 2 bits
* Class C: Three octets minus 3 bits

Networks = 2^n

9.4.3.47 = 0000 1001 = 9 Class A
203.42.62.1 = 1100 1011 = 203 Class C
103.88.77.22 = 0110 0111 = 103 Class A
151.10.13.55 = 1001 0111 = 151 Class B
222.127.16.4 = 1101 1110 = 222 Class C

A = 0-127
B = 128-191
C = 192-223
D = 224-239
E = 240-255

#### Classless networks and subnets

##### Subnet mask

172.16.3.4

255.255.0.0

For the bits set to 1 tell us which part of the IP address is the network, the 0 bits are used for hosts.
It's important to notice that all the 1 go to the left and all the 0 go to the right.

* Class A
  * 4.3.2.1
  * 255.0.0.0
* Class B
  * 183.6.22.9
  * 255.255.0.0
* Class C
  * 203.4.9.6
  * 255.255.255.0

CIDR Notation

172.16.1.0/24

/24 = 255.255.255.0