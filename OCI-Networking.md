
# OCI Networking

## What is OCI Networking?

OCI Networking provides secure communication between cloud resources, on-premises networks, and the internet.

---

# Virtual Cloud Network (VCN)

A Virtual Cloud Network (VCN) is a private, customizable virtual network in OCI.

Features:
- Regional resource
- User-defined IP address range (CIDR)
- Can contain multiple subnets
- Supports IPv4 and IPv6

---

# Subnets

A subnet is a subdivision of a VCN.

Types:
- Public Subnet
- Private Subnet

Public Subnet
- Resources can communicate with the internet.
- Uses an Internet Gateway.

Private Subnet
- No direct internet access.
- Uses a NAT Gateway for outbound traffic.

---

# CIDR Block

A CIDR block defines the IP address range for a VCN or subnet.

Example:
```
10.0.0.0/16
```

---

# Route Table

A Route Table determines where network traffic is sent.

Example Routes:

| Destination | Target |
|-------------|--------|
| 0.0.0.0/0 | Internet Gateway |
| On-Prem Network | DRG |

---

# Internet Gateway (IGW)

Allows communication between public OCI resources and the internet.

Use Case:
- Public web servers

---

# NAT Gateway

Allows private resources to access the internet without accepting inbound connections.

Use Cases:
- Software updates
- Downloading packages

---

# Service Gateway

Allows private access to Oracle Cloud services without using the public internet.

Example:
- Object Storage
- Autonomous Database

Benefits:
- Improved security
- Better performance

---

# Dynamic Routing Gateway (DRG)

A virtual router that connects a VCN to external networks.

Used for:
- Site-to-Site VPN
- FastConnect
- Remote Peering

---

# Local Peering Gateway (LPG)

Connects two VCNs within the same region.

---

# Remote Peering Connection (RPC)

Connects VCNs located in different OCI regions.

---

# FastConnect

Provides a dedicated private connection between an on-premises network and OCI.

Benefits:
- Low latency
- High bandwidth
- More reliable than internet-based connections

---

# Site-to-Site VPN

Creates an encrypted IPSec tunnel between on-premises infrastructure and OCI over the internet.

---

# Security Lists

A virtual firewall applied at the subnet level.

Characteristics:
- Stateful
- Defines ingress and egress rules

---

# Network Security Groups (NSGs)

A virtual firewall applied directly to individual resources.

Benefits:
- More granular security
- Easier management
- Independent of subnet

---

# Load Balancer

Distributes incoming traffic across multiple backend servers.

Benefits:
- High availability
- Scalability
- Fault tolerance

---

# DNS

OCI DNS resolves domain names into IP addresses.

Example:
```
www.example.com → 10.0.0.15
```

---

# High Availability

OCI networking achieves high availability through:
- Multiple Availability Domains
- Fault Domains
- Load Balancers
- Redundant gateways

---

# Best Practices

- Use private subnets whenever possible.
- Apply the principle of least privilege.
- Use NSGs for fine-grained security.
- Place internet-facing resources behind a Load Balancer.
- Monitor network traffic regularly.

---


OCI-Networking.md → VCN, Subnets, Gateways, Routing, Security, VPN, FastConnect, Load Balancer.

Together, these two files cover the majority of the core concepts expected in the OCI Foundations certification while keeping your repository clean and easy to navigate.
