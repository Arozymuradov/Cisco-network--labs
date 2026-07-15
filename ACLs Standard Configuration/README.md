# Standard ACL Configuration Lab (and OSPFv2)

## Overview
This Packet Tracer lab demonstrates the implementation of **OSPFv2** for dynamic routing and **Standard Named Access Control Lists (ACLs)** for network traffic filtering. Two Cisco 2911 routers connect multiple LANs containing PCs and servers, providing full connectivity while enforcing network security policies.

## Objectives
- Configure OSPFv2 between R1 and R2.
- Advertise directly connected networks.
- Configure and apply Standard Named ACLs.
- Restrict access to server networks based on security requirements.
- Verify routing and ACL functionality using `ping` and Cisco IOS show commands.

## Network
- **Routers:** 2 × Cisco 2911
- **Switches:** 4 × Cisco 2960
- **End Devices:** 6 PCs, 2 Servers

### IPv4 Networks
- `192.168.1.0/24` – PC LAN 1
- `192.168.2.0/24` – PC LAN 2
- `192.168.3.0/30` – Router-to-Router Link
- `10.10.1.0/24` – Server LAN 1
- `10.10.2.0/24` – Server LAN 2

## Security Policies
- Only **PC1, PC2, and PC5** can access `10.10.2.0/24`.
- Hosts in `192.168.1.0/24` cannot access `10.10.1.0/24`.
- Hosts in `192.168.1.0/24` cannot access `192.168.2.0/24`.
- Hosts in `192.168.2.0/24` cannot access `192.168.1.0/24`.

## Skills Practiced
- OSPFv2 Configuration
- Dynamic Routing
- Standard Named ACLs
- ACL Placement and Verification
- Network Security
- Cisco IOS Troubleshooting

## Author
**Atajan Rozymuradov**
