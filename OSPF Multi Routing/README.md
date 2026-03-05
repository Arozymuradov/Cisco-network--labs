Cisco Networking Labs – OSPF Multi-Router Topology

The goal of this project is to practice dynamic routing using OSPF and build a scalable multi-router network.

The topology was built and tested using Cisco Packet Tracer.

Network Topology
This lab includes:
6 Cisco routers (2911)
6 LAN networks
6 switches
Multiple PCs

OSPF dynamic routing

Each router connects to:
neighboring routers using 10.10.x.x networks
a local LAN using 192.168.x.x networks

This design allows all networks to communicate through OSPF routing protocol.

LAN Networks
Router	LAN             Network	Gateway
P1	    192.168.10.0/24	192.168.10.1
P2	    192.168.20.0/24	192.168.20.1
P3	    192.168.30.0/24	192.168.30.1
P4	    192.168.40.0/24	192.168.40.1
P5	    192.168.50.0/24	192.168.50.1
P6	    192.168.60.0/24	192.168.60.1

Routers communicate using the following networks:

R1 ↔ R2 10.10.10.0
R2 ↔ R3 10.10.20.0
R3 ↔ R4 10.10.30.0
R4 ↔ R5 10.10.40.0
R5 ↔ R6 10.10.50.0
R6 ↔ R1 10.10.60.0

OSPF Configuration
OSPF process 1 is used on all routers.

Example configuration:
#router ospf 1
#network 10.10.0.0 0.0.255.255 area 0
#network 192.168.0.0 0.0.255.255 area 0

This enables OSPF on all router interfaces participating in the network.

Verification Commands

The following commands were used to verify connectivity:

#show ip ospf neighbor
#show ip route
#ping 192.168.x.x

Successful pings between PCs confirm that OSPF routing tables were built correctly.

Skills Practiced
OSPF dynamic routing
Multi-router network design
IP addressing and subnetting
Network troubleshooting

Tools Used
Cisco Packet Tracer
Cisco IOS CLI

GitHub for documentation
Atajan Rozymuradov
IT – Cybersecurity
