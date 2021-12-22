#### IP addressing in depth

##### VLSM

VLSM creates subnets in different sizes.

#### Address types

##### Unicast traffic

Often devices only wantt to send traffic to one other device at time, this is called unicast traffic.

##### Broadcast traffic

Sometimes the device will want to send a message to every other device in the local network.

To broadcast to every device we have a special IP address, this is called the broadcast IP, it's the very last IP in the local network always.
The last IP address is the IP where all host bits are turned on.

172.16.2.255/24

255... = 1111 1111 = Broadcast

That's why you can never configure a device with the broadcast IP.

The network address is the opposite of the broadcast address.
It's when all the host bits are set to 0, so...

172.16.2.0/24

#### Example

172.16.200.0/30

* Network: 172.16.200.0
* First IP: 172.16.200.1 [USABLE IP]
* Last IP: 172.16.200.2 [USABLE IP]
* Broadcast: 172.16.200.3

#### Magic number method

10.42.37.12/22

1111 1111 - 1111 1111 - 1111 1100 - 0000 0000
   255    -    255    -    252    -     0

256 - 254 = 2
4, 8, 12, 16, 20, 24, 28, 32, [36, 40]

Network: 10.42.36.0
Next: 10.42.40.0
Broadcast: 10.42.39.255

10 Bits = 1022 usable ip's

#### Gateway

Special broadcast

255.255.255.255... I don't care what network you are on, send this traffic everywhere.

#### Multicast traffic

Multicast is a way for devices to opt-in to receiving certain traffic.
The viedo server sends traffic to a multicast IP and other hosts look for traffic sent to that IP,
routers also forward multicast so the traffic can reach the networks if it needs to.

#### Public and private

IANA assigns addresses to RIR's (Regional internet registries).

RIR's assign space to ISP's and large customers.

ISP's give addresses to smaller customers.

RFC 1918 - Private addresses
RFC's describes how certain internet technologies work.

10.0.0.0/8
172.16.0.0/12
192.168.0.0/16