# City Hospital Enterprise Network

## Overview
A complex enterprise network topology designed and simulated using
Huawei eNSP for City Hospital, implementing 11 networking technologies
across 5 departments.

## Departments
| Department | Technologies |
|---|---|
| Patient Registration | DHCP, VLSM |
| Administration | VLANs, Router on Stick, STP, Eth-Trunk |
| Pharmacy | VLANs, Router on Stick |
| Emergency & ICU | VLANs, Router on Stick, ACL |
| Radiology | Static Routing |
| FTP Server | FTP (3 servers — Primary, Backup, Archive) |

## Technologies Implemented
- VLSM (Variable Length Subnet Masking)
- DHCP — dynamic IP for admission terminals
- VLANs — logical segmentation per department
- Router on a Stick — inter-VLAN routing
- STP — loop prevention in Admin switch triangle
- Eth-Trunk — link aggregation for redundancy
- Static Routing — Radiology imaging paths
- RIP v2 — dynamic backbone routing
- ACL — ICU protection from General Ward
- FTP — 3-server medical records infrastructure
- Telnet — centralised remote management


## IP Addressing Summary
| Department | Network | Subnet |
|---|---|---|
| Patient Registration | 192.168.1.0 | /29 per floor |
| Administration VLAN 10 | 192.168.10.0 | /29 |
| Administration VLAN 20 | 192.168.10.8 | /29 |
| Pharmacy VLAN 10 | 192.168.20.0 | /29 |
| Pharmacy VLAN 20 | 192.168.20.8 | /29 |
| Emergency ICU | 192.168.30.0 | /29 |
| Emergency Ward | 192.168.30.8 | /29 |
| Radiology Wing A | 172.16.10.0 | /29 |
| Radiology Wing B | 172.16.11.0 | /29 |
| FTP Servers | 1.1.1.0-1.1.3.0 | /30 each |
| Backbone links | 10.0.1.0-10.0.6.0 | /30 each |

## Tool
Huawei eNSP Simulator
