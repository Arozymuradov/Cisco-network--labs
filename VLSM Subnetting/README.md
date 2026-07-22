# VLSM Subnetting and Static Routing Lab

## Overview

This Cisco Packet Tracer project demonstrates the implementation of **Variable Length Subnet Masking (VLSM)** and **Static Routing** to efficiently subnet the **192.168.15.0/24** network based on different LAN host requirements. The network consists of four LANs connected by two Cisco 2911 routers through a point-to-point WAN link.

---

## Objectives

- Design an efficient VLSM addressing scheme.
- Subnet the given **192.168.15.0/24** network according to host requirements.
- Configure IPv4 addressing on routers and end devices.
- Configure a point-to-point WAN connection.
- Implement static routing between routers.
- Verify full network connectivity.

---

## Network Topology

### Base Network
- **192.168.15.0/24**

### LAN Requirements

| LAN | Host Requirement | Allocated Subnet |
|-----|-----------------:|------------------|
| LAN 1 | 70 Hosts | 192.168.15.0/25 |
| LAN 2 | 3 Hosts | 192.168.15.224/29 |
| LAN 3 | 28 Hosts | 192.168.15.192/27 |
| LAN 4 | 37 Hosts | 192.168.15.128/26 |
| WAN Link | Point-to-Point | 192.168.15.232/30 |

---

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- IPv4 Addressing
- Variable Length Subnet Masking (VLSM)
- Static Routing

---

## Configuration Summary

- Designed the VLSM addressing plan based on LAN host requirements.
- Assigned usable IP addresses to all PCs.
- Configured the **last usable IP address** in each subnet as the router's gateway interface.
- Configured router interfaces with the appropriate IP addresses.
- Configured static routes on both routers.
- Verified end-to-end connectivity between all LANs using ICMP (ping).

---

## Skills Demonstrated

- VLSM subnet planning
- IPv4 subnetting
- Cisco router configuration
- Static routing
- Point-to-point WAN configuration
- Network verification and troubleshooting
- Cisco IOS command-line configuration

---

## Verification

The following tests were successfully completed:

- ✅ All router interfaces configured correctly.
- ✅ All PCs assigned valid IP addresses.
- ✅ Default gateways configured correctly.
- ✅ Static routes installed on both routers.
- ✅ Successful ping between every LAN.

---

## Author

**Atajan Rozymuradov**

Cybersecurity Student | Cisco CCNA Candidate
