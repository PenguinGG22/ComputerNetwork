# ComputerNetwork
Data Communications and Networking with TCP/IP Protocol Suite

Data communication : the exchange of data between two devices via some form of transmission medium

CSMA/CD : Carrier Sense Multiple Access with Collision Detection
Detected energy double when there is a collison

CMSA/CA : Carrier Sense Multiple Access with Collision Avoidance
Detected energy 5~10% when there is a collison

LAN(Local Area Networks)

Data-link layer
LLC : Logical Link Control
flow control, error control, part of framming duties
PDU : Protocol Data Unit

MAC : Media Access Control (Access)

Pyhsical layer(Transmission media에 따라서 어떤 방식으로 통신을 할 것인지)

IEEE 802 Working Groups
802.1Q Virtual LANs
802.2 LLC
802.3 CMSA/CD
802.3aF PoE(Power Of Ethernet)
802.4 Token Bus(disabled)
802.5 Token Ring(disabled)
802.15 WPAN(Wireless Personal Area Network)
802.15.1 Bluetooth
802.15.4 ZigBee

Ethernet frame format
Phystical-Layer header(Sync)

Destination address(6 byte)
Source address(6 byte)
Type(2 byte)
- length field : define the length of data (data field < 1518) 
- type field : define the upper-layer protocol (data field > 1536) 
Data and padding(46 ~ 1500 byte)
CRC(4 byte)
Cyclic Redundancy Check : Mcontains error detection 

minimum frame length : 64 byte
- required for the correct operation of CSMA/CD
Maximum frame length : 1518 byte
- to reduce size of buffer
- to prevent monopolizing

Network Interface card (NIC)
MAC address, Ethernet address, Hardware address

Unicast 1:1 (Byte 1, LSB : 0)
Mulitcast 1:N (Byte 1, LSB : 1)
Broadcast 1:ALL (FF-FF-FF-FF-FF-FF)

1-persistent CSMA/CD
Collision can only occur during the first half of the slot time
Late collision : collision occurs after the first 512 bit time

MaxLength = Propagation Speed * SlotTime / 2
MaxLength = (2 * 10 ^ 8)*(5.12*10^-6/2) = 5120m
MaxLength = 2500m

Standard Ethernet common implementations <Speed, Method, Length>
10Base5: Bus <10Mbps, Baseband, 500m>
10Base2: Bus <10Mbps, Baseband, 185m>
10Base-T: Star <10Mbps, Baseband, 100m>
10Base-F: Star <10Mbps, Baseband, 2000m>

Bridge : devide the network 
Raising the bandwith
Separating collision domains

Swithing hub