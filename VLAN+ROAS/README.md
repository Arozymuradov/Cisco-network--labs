# VLAN + Router-on-a-Stick (ROAS) with VLSM Subnetting

## Lab Overview

This lab demonstrates VLAN segmentation, trunking, Router-on-a-Stick inter-VLAN routing, and VLSM subnetting in Cisco Packet Tracer.

The network uses one main address block: 10.0.0.0/24

This address space was divided into smaller subnets using VLSM based on the number of hosts required for each VLAN.

## VLAN and Subnet Design

| VLAN | Department | Hosts Needed | Network Address | Subnet Mask | Usable IP Range | Broadcast |

| VLAN 10 | ADMINISTRATORS | 20 | 10.0.0.0/27 | 255.255.255.224 | 10.0.0.1 - 10.0.0.30 | 10.0.0.31 |
| VLAN 40 | HR | 12 | 10.0.0.32/28 | 255.255.255.240 | 10.0.0.33 - 10.0.0.46 | 10.0.0.47 |
| VLAN 30 | ENGINEERS | 10 | 10.0.0.48/28 | 255.255.255.240 | 10.0.0.49 - 10.0.0.62 | 10.0.0.63 |
| VLAN 20 | OFFICE | 4 | 10.0.0.64/29 | 255.255.255.248 | 10.0.0.65 - 10.0.0.70 | 10.0.0.71 |

## Default Gateway Addresses

The last usable IP address in each subnet was used as the default gateway.

| VLAN | Gateway |

| VLAN 10 | 10.0.0.30 |
| VLAN 20 | 10.0.0.70 |
| VLAN 30 | 10.0.0.62 |
| VLAN 40 | 10.0.0.46 |

After configuring VLANs, trunks, router subinterfaces, and default gateways, PCs from different VLANs were tested using the ping command.

Successful ping tests confirmed that inter-VLAN routing was working correctly through Router-on-a-Stick.
