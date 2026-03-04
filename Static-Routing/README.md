This folder contains Cisco Static Routing configuration files, topology, and ping test results.

Full description:
# Static Routing Lab
This project demonstrates a Cisco static routing configuration using a square network topology.  
The network consists of four routers, four switches, and four PCs connected across four different LAN segments. :contentReference[oaicite:0]{index=0}

## Network Topology
The topology connects four routers in a square configuration to allow routing between four LAN networks.  
Each router is connected to a switch, which connects to a local PC. The network uses static routing to allow communication between all LAN segments. :contentReference[oaicite:1]{index=1}

## Devices
Routers: R1, R2, R3, R4  
Switches: SW1, SW2, SW3, SW4  
PCs: PC1, PC2, PC3, PC4  

## LAN Networks

| Network       | Connected Device |
| 192.168.100.0 | PC1 LAN |
| 192.168.101.0 | PC2 LAN |
| 192.168.102.0 | PC3 LAN |
| 192.168.103.0 | PC4 LAN |

## Router Interconnections

| Link    | Network |
| R1 ↔ R2 | 10.10.10.0 |
| R2 ↔ R3 | 10.10.11.0 |
| R3 ↔ R4 | 10.10.12.0 |
| R4 ↔ R1 | 10.10.13.0 |

## Technologies Used

- Cisco Packet Tracer
- Static Routing
- IPv4 addressing
- LAN and WAN network segmentation

## Result

All LAN networks are able to communicate with each other through static routing configured on the routers.
