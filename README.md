# ComputerNetwork
Data Communications and Networking with TCP/IP Protocol Suite

Data communication : the exchange of data between two devices via some form of transmission medium

CSMA/CD : Carrier Sense Multiple Access with Collision Detection
Detected energy double when there is a collison

CMSA/CA : Carrier Sense Multiple Access with Collision Avoidance
Detected energy 5~10% when there is a collison

LAN : Local Area Network

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

