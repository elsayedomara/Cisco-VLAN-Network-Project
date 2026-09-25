# Cisco VLAN Network Project

A Cisco Packet Tracer network project demonstrating VLAN segmentation, access port configuration, 802.1Q trunking, IP addressing, and connectivity testing across two Cisco switches.

## Project Overview

This project was built using Cisco Packet Tracer to demonstrate basic Layer 2 network segmentation using VLANs.

The network consists of two Cisco 2960 switches and six PCs. Each switch connects three PCs, with the same VLAN structure configured across both switches.

The project focuses on:

- VLAN creation and configuration
- Access port assignment
- 802.1Q trunk configuration
- Allowed VLAN configuration
- IP addressing
- Inter-switch VLAN connectivity
- Connectivity verification using ICMP Ping

## Network Topology

- 2 × Cisco 2960 switches
- 6 × PCs
- 3 × VLANs
- 1 × Trunk link between the switches
- Trunk interface: Fa0/4

### Topology

![Network Topology](screenshots/01-topology.png)

## VLAN Configuration

| VLAN ID | VLAN Name | Access Port |
|---------|-----------|-------------|
| 10 | HR | Fa0/1 |
| 20 | IT | Fa0/2 |
| 30 | SALES | Fa0/3 |

The same VLAN configuration is implemented on both switches.

### Switch 1 VLAN Configuration

![Switch 1 VLAN Configuration](screenshots/02-switch1-vlans.png)

### Switch 2 VLAN Configuration

![Switch 2 VLAN Configuration](screenshots/03-switch2-vlans.png)

## Trunk Configuration

The switches are connected through FastEthernet 0/4.

The trunk uses IEEE 802.1Q encapsulation and allows VLANs 10, 20, and 30.

```text
Interface: Fa0/4
Mode: Trunk
Encapsulation: 802.1Q
Allowed VLANs: 10,20,30
Status: Trunking
