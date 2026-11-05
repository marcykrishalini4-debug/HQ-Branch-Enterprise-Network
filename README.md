# HQ–Branch Enterprise Network Design and Implementation

## Project Overview

This project demonstrates the design and implementation of an enterprise network connecting a Head Office (HQ) and a Branch Office using Cisco Packet Tracer.

The network provides communication between multiple departments through VLAN segmentation, inter-VLAN routing, DHCP, WAN connectivity, and static routing. Access Control Lists (ACLs) are also implemented to restrict Guest network access.

## Project Objectives

- Design an enterprise network connecting HQ and Branch offices.
- Divide departments into separate VLANs.
- Implement efficient IP addressing using VLSM.
- Configure inter-VLAN communication.
- Automate IP address allocation using DHCP.
- Establish WAN connectivity between two locations.
- Configure static routing.
- Improve network security using ACLs.
- Verify connectivity through network testing.

## Network Topology

The network consists of:

- 2 Cisco 2911 Routers
- 2 Cisco 2960 Switches
- 5 End Devices (PCs)
- 4 HQ Department VLANs
- 1 Branch LAN
- 1 WAN connection between HQ and Branch

## VLAN Configuration

| VLAN ID | Department | Network |
|---|---|---|
| VLAN 10 | Guest | 192.168.1.0/25 |
| VLAN 20 | Sales | 192.168.1.128/26 |
| VLAN 30 | IT | 192.168.1.192/27 |
| VLAN 40 | HR | 192.168.1.224/28 |

## IP Addressing

| Network | Network Address | Default Gateway |
|---|---|---|
| Guest | 192.168.1.0/25 | 192.168.1.1 |
| Sales | 192.168.1.128/26 | 192.168.1.129 |
| IT | 192.168.1.192/27 | 192.168.1.193 |
| HR | 192.168.1.224/28 | 192.168.1.225 |
| Branch | 192.168.1.240/29 | 192.168.1.241 |
| WAN | 192.168.1.248/30 | HQ: 192.168.1.249 / Branch: 192.168.1.250 |

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS Command Line Interface (CLI)
- VLAN Configuration
- VLSM Subnetting
- DHCP
- Router-on-a-Stick
- Inter-VLAN Routing
- WAN Configuration
- Static Routing
- Access Control Lists (ACLs)

## Key Implementations

### 1. VLAN Segmentation
Created separate VLANs for Guest, Sales, IT, and HR departments to logically separate network traffic.

### 2. VLSM Subnetting
Applied Variable Length Subnet Masking to allocate IP addresses efficiently based on network requirements.

### 3. Inter-VLAN Routing
Configured Router-on-a-Stick using router subinterfaces to enable communication between authorized VLANs.

### 4. DHCP Configuration
Configured DHCP pools to automatically assign IP addresses, subnet masks, and default gateways to client devices.

### 5. WAN Connectivity
Established a point-to-point WAN connection between the Head Office and Branch Office routers.

### 6. Static Routing
Configured static routes to enable communication between the HQ and Branch networks.

### 7. Network Security
Implemented an Extended Access Control List to restrict Guest VLAN access to internal department and Branch networks.

## Testing and Verification

The following tests were performed:

- Verified VLAN creation and port assignments.
- Verified trunk configuration.
- Checked router interface status.
- Verified DHCP address allocation.
- Tested inter-VLAN connectivity.
- Tested WAN connectivity.
- Verified HQ-to-Branch communication.
- Verified Branch-to-HQ communication.
- Tested Guest network access restrictions.

**Result:** Successful end-to-end communication between the HQ and Branch networks was verified, and Guest network restrictions were tested.

## Project Files

- `HQ-Branch-VLSM-Network.pkt` – Cisco Packet Tracer project file.
- `Screenshots/` – Configuration and connectivity evidence.
- `Documentation/` – Additional project documentation.

## Learning Outcomes

Through this project, I strengthened my practical understanding of enterprise network design, IP addressing, VLAN configuration, routing, network security, and troubleshooting using Cisco Packet Tracer.

## Author

Developed as a networking project for academic and practical learning.

## License

This project is available for educational and learning purposes.