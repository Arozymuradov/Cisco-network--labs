# Enterprise LAN and WAN Network Design and Configuration

## Project Overview

This project demonstrates the design, configuration, and troubleshooting of a multi-site enterprise network using **Cisco Packet Tracer**.

The network connects two local area networks (LANs) through a wide area network (WAN), providing inter-VLAN communication, dynamic routing, DHCP services, network security, and IPv4/IPv6 connectivity.

## Technologies and Protocols

- **VLANs:** Network segmentation for different departments
- **Router-on-a-Stick (ROAS):** Inter-VLAN routing using router subinterfaces
- **OSPFv2:** Dynamic routing between routers
- **DHCP:** Automatic IPv4 address assignment
- **EtherChannel:** Link aggregation using LACP and PAgP
- **Extended ACLs:** Traffic filtering and access control
- **Static NAT:** Mapping a private server IP address to a public IP address
- **IPv4 and IPv6:** Dual-stack network addressing
- **WAN:** Serial connections between routers

## Network Design

The topology includes:

- Three routers (R1, R2, and ISP)
- Four Layer 2 switches (S1, S2, S3, and S4)
- Multiple PCs across different VLANs
- A web server
- WAN connections between routers

### VLAN Configuration

| VLAN | Department | Network |
|---|---|---|
| 10 | Accounting | 10.99.10.0/24 |
| 20 | Human Resources | 10.99.20.0/24 |
| 30 | Sales | 10.99.30.0/24 |
| 40 | IT | 10.99.40.0/24 |

## Network Security

An extended access control list (ACL) is configured to control access to the web server at `10.99.40.2`.

Static NAT maps the internal web server address to `209.165.200.102`.

## Configuration and Verification

The following Cisco IOS commands are used to verify network configuration and connectivity:

```cisco
show ip interface brief
show vlan brief
show interfaces trunk
show etherchannel summary
show ip ospf neighbor
show ip route
show ip dhcp binding
show access-lists
show ip nat translations
```

Additional testing includes `ping`, `traceroute`, and HTTP connectivity checks.

## Tools Used

- Cisco Packet Tracer
- Cisco IOS Command-Line Interface (CLI)

## Learning Outcomes

Through this project, I practiced:

- Designing a multi-site enterprise network topology
- Configuring VLANs and inter-VLAN routing
- Establishing OSPF routing between routers
- Implementing centralized DHCP services
- Configuring EtherChannel for link aggregation
- Applying ACLs to control network traffic
- Implementing static NAT
- Troubleshooting network connectivity

## Author

**Atajan Rozymuradov**  
Cybersecurity Student | Network Administration | Cisco Networking

*This project was developed for educational purposes and hands-on Cisco networking practice.*
