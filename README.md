# Day 2 – IPv4 Addressing & School Network Design

## Project Overview

This lab focused on designing and implementing a structured IPv4 addressing scheme for a simulated school network environment using Cisco Packet Tracer.

The objective was to create separate departmental networks with organized IP allocation, proper subnetting structure, and scalable addressing practices commonly used in enterprise environments.

The network was segmented into multiple departments to improve manageability, simplify troubleshooting, and prepare the infrastructure for future routing and VLAN implementation.

---

# Network Topology

## Departments Implemented
- Administration Department
- ICT Laboratory
- Library

---

# Devices Used

| Device Type | Quantity |
|---|---|
| Cisco 2960 Switches | 3 |
| PCs | 10 |

---

# Network Design

Each department was assigned a dedicated private IPv4 network range using Class C addressing.

This approach improves:
- Network organization
- Scalability
- Address management
- Future routing implementation
- Troubleshooting efficiency

---

# IPv4 Addressing Scheme

## Administration Department

### Network Information

| Parameter | Value |
|---|---|
| Network Address | 192.168.10.0/24 |
| Subnet Mask | 255.255.255.0 |
| Available Hosts | 254 |

### Assigned Hosts

| Device | IP Address |
|---|---|
| Admin-PC1 | 192.168.10.1 |
| Admin-PC2 | 192.168.10.2 |
| Admin-PC3 | 192.168.10.3 |

---

## ICT Laboratory

### Network Information

| Parameter | Value |
|---|---|
| Network Address | 192.168.20.0/24 |
| Subnet Mask | 255.255.255.0 |
| Available Hosts | 254 |

### Assigned Hosts

| Device | IP Address |
|---|---|
| ICT-PC1 | 192.168.20.1 |
| ICT-PC2 | 192.168.20.2 |
| ICT-PC3 | 192.168.20.3 |
| ICT-PC4 | 192.168.20.4 |
| ICT-PC5 | 192.168.20.5 |

---

## Library Department

### Network Information

| Parameter | Value |
|---|---|
| Network Address | 192.168.30.0/24 |
| Subnet Mask | 255.255.255.0 |
| Available Hosts | 254 |

### Assigned Hosts

| Device | IP Address |
|---|---|
| Lib-PC1 | 192.168.30.1 |
| Lib-PC2 | 192.168.30.2 |

---

# Physical Connectivity

All PCs were connected to Cisco 2960 switches using Copper Straight-Through cables.

## Switch Connections

| Department | Switch |
|---|---|
| Administration | SW1 |
| ICT Lab | SW2 |
| Library | SW3 |

---

# Tasks Performed

The following configurations and validations were completed successfully:

- Designed departmental IPv4 network structure
- Assigned static IPv4 addresses
- Configured subnet masks
- Verified addressing consistency
- Tested host communication
- Documented network ranges
- Organized departmental segmentation

---

# Verification & Testing

## Connectivity Testing

ICMP ping testing was used to verify communication between hosts within the same departmental network.

### Tools Used
- Cisco Packet Tracer
- Command Prompt
- ping

### Example Verification Command

```bash
ping 192.168.10.2
```

---

# Troubleshooting Performed

## Issue Encountered

Some devices initially failed connectivity tests during implementation.

---

## Root Cause Analysis

The issue was caused by:
- Incorrect IP assignments
- Mismatched network addressing
- Incorrect subnet mask configuration

---

## Troubleshooting Process

The following steps were used to isolate and resolve the issue:

1. Verified IPv4 addressing on all hosts
2. Confirmed subnet masks matched network design
3. Checked network IDs and host IDs
4. Revalidated connectivity using ICMP ping testing

---

## Resolution

After correcting addressing inconsistencies, communication within each departmental network was successfully restored.

---

# Key Networking Concepts Demonstrated

- IPv4 Addressing
- Private IPv4 Networks
- Network IDs
- Host IDs
- Class C Addressing
- Static Addressing
- Subnet Masks
- Departmental Segmentation

---

# Enterprise Relevance

Structured IPv4 addressing is critical in enterprise environments because it:
- Simplifies network administration
- Reduces IP conflicts
- Improves scalability
- Supports routing implementation
- Enhances troubleshooting efficiency
- Enables structured network segmentation

Organizations rely on proper addressing schemes to maintain reliable and scalable network infrastructure.

---

# Files Included

```text
Day02-IPv4-Addressing/
├── README.md
├── Day02-IPv4-Addressing.pkt
├── screenshots/
└── configs/
```

---

# Tools & Technologies Used

- Cisco Packet Tracer
- Cisco 2960 Switches
- IPv4 Addressing
- ICMP Ping Testing

---

# Conclusion

This lab demonstrated the importance of structured IPv4 addressing and organized departmental network design in enterprise environments.

The implementation established a scalable foundation for future networking concepts including VLANs, routing, subnetting, and inter-network communication.
