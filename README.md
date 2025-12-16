# Secure Virtual Enterprise Network using pfSense

## Overview
This project demonstrates the design, implementation, and validation of a secure virtual enterprise network using pfSense as a perimeter firewall and routing platform. The environment simulates a real-world corporate LAN/WAN setup with network segmentation, access control, and traffic inspection.

The project focuses on enforcing least-privilege network access and validating security controls using packet-level analysis.

---

## Architecture Summary
The network is deployed in a virtualized environment using Oracle VirtualBox and consists of:

- pfSense firewall (gateway, DHCP, DNS, and firewall enforcement)
- Ubuntu Server acting as an internal service host
- Client systems used to generate and analyze traffic
- Segmented network zones using VLANs and subnets

Refer to the `architecture/` directory for topology diagrams.

---

## Network Segmentation
The enterprise network is segmented into isolated VLANs to reduce attack surface and prevent lateral movement:

| VLAN | Purpose | Subnet |
|-----|--------|--------|
| HR | Human Resources | 192.168.10.0/24 |
| IT | IT Administration | 192.168.20.0/24 |
| Guest | Untrusted users | 192.168.30.0/24 |

Inter-VLAN traffic is restricted by default and explicitly allowed only where required.

---

## Security Controls Implemented
- Stateful firewall rules enforcing least privilege
- Inter-VLAN traffic filtering
- WAN-to-LAN ICMP blocking
- Controlled DNS and DHCP services
- NAT configuration for secure internet access
  

---

## Validation and Evidence
All security controls were validated using packet capture analysis and firewall rule verification.

Evidence includes:
- DHCP DORA packet captures
- DNS resolution captures
- ICMP blocking validation
- Firewall rule screenshots

See:
- `/pcaps/`
- `/validation/`
- `/screenshots/`

---

## Tools & Technologies
- pfSense
- VirtualBox
- Ubuntu Server
- Kali Linux
- pfSense packet capture
- Git & GitHub

---

## Key Learning Outcomes
- Enterprise firewall configuration
- Network segmentation and Zero Trust concepts
- Packet-level traffic analysis
- Security documentation and evidence handling
- Version-controlled security projects

---

## Author
Omoboriowo Oluwagbotemi Yinka
Cybersecurity / IT Support Engineer
