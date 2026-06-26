# Azure Regions

## What is an Azure Region?

It is a geographical area that contains one or more Azure datacenters connected through a high-speed, low-latency network.

Each region provides Azure services such as:

* Virtual Machines
* Storage Accounts
* Databases
* Networking
* Kubernetes Services
* AI Services

---

## What are Regions and Why is it Important?

Choosing the correct region affects:

* Latency
* Performance
* Cost
* Compliance
* Data Residency
* Service Availability
* Disaster Recovery

---

# Azure Geography

## What is an Azure Geography?

An Azure Geography is a collection of one or more Azure regions that preserve data residency, compliance, and legal boundaries.

Examples of Azure Geographies:

* India
* Europe
* United States
* Australia

Each geography helps organizations meet regulatory and compliance requirements.

---

# Azure Region Pair

## What is a Region Pair?

An Azure Region Pair is a pair of two Azure regions within the same geography.

Microsoft pairs regions to support:

* Disaster Recovery
* Data Replication
* Planned Maintenance
* Business Continuity

### Examples

* Central India ↔ South India
* East US ↔ West US
* West Europe ↔ North Europe

If one region experiences a major outage, services can fail over to its paired region.

---

# Availability Zone

## What is an Availability Zone?

An Availability Zone is a physically separate location within an Azure region.

Each Availability Zone has its own:

* Power supply
* Cooling system
* Network infrastructure
* Physical buildings (datacenters)

Because each zone is isolated, the failure of one zone does not affect the others.

---

## Why Availability Zones?

Suppose your VM is running in **Zone 1**.

If **Zone 1** experiences a power failure:

* VM in Zone 1 may stop.
* VM in Zone 2 continues running.
* VM in Zone 3 continues running.

---

## Region vs Availability Zone

| Region                           | Availability Zone                 |
| -------------------------------- | --------------------------------- |
| Geographic area                  | Physical location inside a region |
| Contains one or more datacenters | One or more isolated datacenters  |
| Used for Disaster Recovery       | Used for High Availability        |
| Example: Central India           | Zone 1, Zone 2, Zone 3            |

---

## Benefits

* High Availability
* Fault Isolation
* Improved Reliability
* Reduced Downtime

---

# Availability Sets

## What is an Availability Set?

An Availability Set is an Azure feature that distributes multiple virtual machines across different hardware to protect against hardware failures and planned maintenance.

Unlike Availability Zones, VMs remain within the same Azure datacenter.

---

## Why Availability Sets?

Imagine two VMs:

* VM1
* VM2

If both are hosted on the same physical server and that server fails, both VMs become unavailable.

With an Availability Set:

* VM1 is placed on one physical server.
* VM2 is placed on another physical server.
* If one server fails, the other VM remains available.

---

## Availability Set Uses

### Fault Domains (FD)

A Fault Domain represents a group of hardware that shares a common power source and network switch.

If one Fault Domain fails, VMs in other Fault Domains continue running.

---

### Update Domains (UD)

Azure periodically performs planned maintenance.

Update Domains ensure that Azure updates only one group of VMs at a time.

This prevents all VMs from restarting simultaneously.

---

# Azure Data Centers

## What is a Data Center?

A Data Center is a physical building where Microsoft installs and operates:

* Physical Servers
* Storage Systems
* Networking Equipment
* Power Systems
* Cooling Systems
* Security Infrastructure

Every Azure resource ultimately runs on hardware inside a data center.

---

# Azure Edge Zones

## What is an Edge Zone?

An Azure Edge Zone is a small extension of an Azure region placed closer to end users to provide ultra-low latency for applications.
