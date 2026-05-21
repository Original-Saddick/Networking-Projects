 Cisco Switch Configuration & IOS CLI Administration

## Project Overview

This lab focused on configuring and managing a Cisco switch using the Cisco IOS Command-Line Interface (CLI).

The objective was to simulate foundational enterprise switch administration tasks including hostname configuration, password security, management IP assignment, and configuration persistence.

---

# Devices Used

| Device Type | Quantity |
|---|---|
| Cisco 2960 Switch | 1 |
| PCs | 4 |

---

# Network Topology

All hosts were connected to a single Cisco 2960 switch using Copper Straight-Through cables.

---

# IP Addressing Scheme

| Device | IP Address |
|---|---|
| PC1 | 192.168.10.1 |
| PC2 | 192.168.10.2 |
| PC3 | 192.168.10.3 |
| PC4 | 192.168.10.4 |
| SW1 VLAN1 | 192.168.10.10 |

Subnet Mask:

```text
255.255.255.0
```

---

# Tasks Performed

- Configured switch hostname
- Configured console security
- Configured enable secret password
- Assigned switch management IP
- Verified interface status
- Tested connectivity
- Saved switch configuration

---

# Cisco IOS Configuration

## Hostname Configuration

```bash
hostname SW1
`

## Console Security

```bash
line console 0
password saddick
login
```

---

## Enable Secret Configuration

```bash
enable secret original
```

---

## Management Interface Configuration

```bash
interface vlan 1
ip address 192.168.10.10 255.255.255.0
no shutdown
```

---

# Verification Commands Used

```bash
show running-config
show interfaces status
show ip interface brief
```

---

# Connectivity Testing

ICMP ping testing was used to verify communication between hosts and the switch management interface.

## Example Command

```bash
ping 192.168.10.10
```

---

# Troubleshooting Performed

## Issue Encountered

Initial connectivity tests to the switch management IP failed.

---

## Root Cause

The VLAN 1 interface was administratively down.

---

## Troubleshooting Steps

- Verified interface status using:

```bash
show ip interface brief
```

- Identified VLAN 1 shutdown state
- Enabled interface using:

```bash
interface vlan 1
no shutdown
```

- Retested connectivity

---

## Resolution

Connectivity to the switch management interface was successfully restored.

---

# Enterprise Relevance

Switch administration is fundamental in enterprise environments because switches serve as the primary infrastructure for endpoint connectivity.

Proper switch configuration is essential for:
- Secure administrative access
- Remote device management
- Infrastructure monitoring
- Configuration consistency
- Operational reliability

Management IP addressing enables centralized administration and monitoring across enterprise networks.

---

# Key Concepts Demonstrated

- Cisco IOS CLI
- Switch Administration
- Management VLANs
- Console Security
- Enable Secret Authentication
- Interface Configuration
- Configuration Persistence

---

# Tools & Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- Cisco 2960 Switch
- ICMP Ping Testing

---

# Files Included

```text
Day04-Switch-Configuration/
├── README.md
├── Day04-Switch-Configuration.pkt
├── screenshots/
└── configs/
```

---

# Conclusion

This lab demonstrated foundational Cisco switch administration practices used in enterprise environments for device management, infrastructure security, and operational network maintenance.
