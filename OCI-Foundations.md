#OCI-Foundations.md
# Oracle Cloud Infrastructure (OCI) Foundations

## What is OCI?

Oracle Cloud Infrastructure (OCI) is Oracle's cloud platform that provides compute, storage, networking, databases, security, and many other cloud services. It enables organizations to build, migrate, and manage applications securely and efficiently.

---

## Key Benefits of OCI

- High performance infrastructure
- Built-in security
- High availability and fault tolerance
- Global cloud regions
- Flexible pricing
- Supports hybrid and multi-cloud deployments

---

## OCI Global Infrastructure

### Region
A Region is a geographical location where Oracle has one or more data centers.

Examples:
- India Central (Hyderabad)
- India South (Mumbai)
- US East (Ashburn)

---

### Availability Domain (AD)

- An isolated data center within a region.
- Each region has one or more Availability Domains.
- Connected through low-latency, high-bandwidth networks.
- Failure in one AD does not impact the others.

Purpose:
- High Availability
- Disaster Recovery

---

### Fault Domain (FD)

A Fault Domain is a logical grouping of hardware within an Availability Domain.

Purpose:
- Protects against planned maintenance
- Reduces impact of hardware failures
- Improves application availability

---

## Compartments

Compartments are logical containers used to organize OCI resources.

Benefits:
- Better resource organization
- Access control using IAM
- Cost tracking
- Easier administration

---

## Identity and Access Management (IAM)

IAM controls who can access OCI resources.

Main Components:
- Users
- Groups
- Policies
- Dynamic Groups
- Compartments

Example Policy:

```
Allow group NetworkAdmins to manage virtual-network-family in compartment Production
```

---

## Compute

Compute instances are virtual machines used to run applications.

Types:
- Virtual Machines (VM)
- Bare Metal
- Container Instances

Common Use Cases:
- Web servers
- Application servers
- Development environments

---

## Storage

OCI provides multiple storage options.

### Block Storage
Persistent storage attached to compute instances.

### Object Storage
Stores files, backups, images, videos, and logs.

### File Storage
Shared storage accessed by multiple compute instances.

---

## Database Services

OCI offers managed databases including:

- Autonomous Database
- Oracle Database Service
- MySQL HeatWave

Benefits:
- Automated backups
- Automatic patching
- High availability

---

## Load Balancer

Distributes incoming traffic across multiple servers.

Advantages:
- High availability
- Improved scalability
- Better application performance

---

## Monitoring

OCI Monitoring helps track resource health and performance.

Features:
- Metrics
- Alarms
- Notifications

---

## Security

OCI provides multiple security features:

- IAM
- Security Lists
- Network Security Groups (NSGs)
- Encryption at Rest
- Encryption in Transit
- Cloud Guard
- Vault Service

---

## High Availability

OCI achieves high availability using:

- Multiple Availability Domains
- Fault Domains
- Load Balancers
- Redundant networking

---

## Shared Responsibility Model

Oracle is responsible for:
- Physical data centers
- Hardware
- Networking infrastructure
- Hypervisor

Customers are responsible for:
- IAM configuration
- Applications
- Operating systems
- Data
- Network configuration

---

## Certification Tips

- A Region contains one or more Availability Domains.
- Fault Domains exist inside an Availability Domain.
- Compartments help organize resources.
- IAM controls authentication and authorization.
- VCN is OCI's virtual network.
- Security Lists and NSGs act as virtual firewalls.
- Object Storage is highly durable.
- Load Balancers improve availability.
- OCI follows the Shared Responsibility Model.

---
