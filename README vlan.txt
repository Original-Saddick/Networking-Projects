# Day 5 – VLAN Segmentation & Switch Port Configuration

## Project Overview

This lab focused on implementing VLAN-based network segmentation using a Cisco 2960 switch in Cisco Packet Tracer.

The objective was to logically separate departments within the same physical switch infrastructure while maintaining organized traffic isolation and reducing unnecessary broadcast traffic.

---

# Devices Used

| Device Type | Quantity |
|---|---|
| Cisco 2960 Switch | 1 |
| PCs | 6 |

---

# Departments Implemented

- HR Department
- Finance Department
- IT Department

---

# VLAN Design

| VLAN ID | Department | Network |
|---|---|---|
| 10 | HR | 192.168.10.0/24 |
| 20 | FINANCE | 192.168.20.0/24 |
| 30 | IT | 192.168.30.0/24 |

---

# Physical Port Assignments

| Switch Port | Device | VLAN |
|---|---|---|
| Fa0/1 | HR-PC1 | VLAN 10 |
| Fa0/2 | HR-PC2 | VLAN 10 |
| Fa0/3 | FIN-PC1 | VLAN 20 |
| Fa0/4 | FIN-PC2 | VLAN 20 |
| Fa0/5 | IT-PC1 | VLAN 30 |
| Fa0/6 | IT-PC2 | VLAN 30 |

---

# IP Addressing Scheme

## HR VLAN

| Device | IP Address |
|---|---|
| HR-PC1 | 192.168.10.1 |
| HR-PC2 | 192.168.10.2 |

---

## FINANCE VLAN

| Device | IP Address |
|---|---|
| FIN-PC1 | 192.168.20.1 |
| FIN-PC2 | 192.168.20.2 |

---

## IT VLAN

| Device | IP Address |
|---|---|
| IT-PC1 | 192.168.30.1 |
| IT-PC2 | 192.168.30.2 |

---

# Subnet Mask

```text
255.255.255.0
```

---

# Tasks Performed

- Created VLANs
- Assigned switch ports to VLANs
- Configured endpoint IPv4 addressing
- Verified VLAN isolation
- Tested intra-VLAN communication
- Validated switch port assignments

---

# Cisco IOS Configuration

## VLAN Creation

```bash
vlan 10
name HR

vlan 20
name FINANCE

vlan 30
name IT
```

---

## Access Port Assignment

```bash
interface range fa0/1-2
switchport mode access
switchport access vlan 10

interface range fa0/3-4
switchport mode access
switchport access vlan 20

interface range fa0/5-6
switchport mode access
switchport access vlan 30
```

---

# Verification Commands Used

```bash
show vlan brief
show interfaces status
show running-config
```

---

# Connectivity Testing

## Successful Tests

Devices within the same VLAN communicated successfully using ICMP ping testing.

Examples:
- HR-PC1 ↔ HR-PC2
- FIN-PC1 ↔ FIN-PC2
- IT-PC1 ↔ IT-PC2

---

## Expected Failed Tests

Inter-VLAN communication failed because Layer 3 routing had not yet been configured.

Examples:
- HR-PC1 ↔ FIN-PC1
- FIN-PC1 ↔ IT-PC1

This verified successful VLAN isolation.

---

# Troubleshooting Performed

## Issue Encountered

One device initially failed communication within its VLAN.

---

## Root Cause

The switch port had been assigned to the wrong VLAN.

---

## Troubleshooting Process

- Verified VLAN assignments using:

```bash
show vlan brief
```

- Checked interface status
- Corrected VLAN membership
- Retested connectivity using ICMP ping testing

---

## Resolution

Connectivity was restored successfully after correcting the VLAN assignment.

---

# Enterprise Relevance

VLANs are essential in enterprise networking because they:
- Improve network segmentation
- Enhance security
- Reduce broadcast traffic
- Simplify administration
- Support scalable infrastructure

Organizations commonly use VLANs to separate:
- HR systems
- Finance systems
- Server environments
- Voice networks
- Guest networks

---

# Key Concepts Demonstrated

- VLANs
- Broadcast Domains
- Switch Port Configuration
- Access Ports
- Logical Segmentation
- Traffic Isolation

---

# Tools & Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- Cisco 2960 Switch
- ICMP Ping Testing

---

# Files Included

```text
Day05-VLANs/
├── README.md
├── Day05-VLANs.pkt
├── screenshots/
└── configs/
```

---

# Conclusion

This lab demonstrated how VLANs logically segment departments within shared switch infrastructure while improving traffic management, scalability, and enterprise network organization.