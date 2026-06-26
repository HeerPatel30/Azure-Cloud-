# Basics of Cloud Computing

## 1. What is Cloud?

Cloud is a vast virtual environment where users can store files, run software, and access various services over the internet. It allows users to utilize resources without managing or maintaining the underlying physical servers and infrastructure.

---

## 2. What is Cloud Computing?

Cloud computing is a technology deployment model that involves the use of various computing services over the internet without owning and maintaining physical servers and infrastructure. Users can access and use resources, applications, and storage provided by either third-party service providers or their own organizations.

---

# Cloud Deployment Models

There are three types of cloud deployment models:

## 1. Public Cloud

The cloud infrastructure is owned and managed by a third-party cloud provider and shared among multiple consumers (tenants).

### Who Can Use It?
- Individuals
- Businesses
- Organizations

### What It's Like?
Imagine a giant shared computer space on the internet. It is like using applications, storing files, or performing tasks on the internet that anyone can access.

### Characteristics
- Low cost (Pay-as-you-go)
- Highly scalable
- No hardware maintenance
- Quick deployment

### Example
- Google Drive
- Amazon Web Services (AWS)

---

## 2. Private Cloud

The cloud infrastructure is dedicated to a single organization.

### Who Can Use It?
- A specific organization or business

### What It's Like?
Picture having your own personal private computer space. It is like a digital clubhouse where only you and your team have access. Others cannot access it.

### Characteristics
- High security
- Greater control
- Customizable
- More expensive

### Example
- A company using its own servers and infrastructure for all its digital needs

---

## 3. Hybrid Cloud

A hybrid cloud is a combination of public and private clouds. Some workloads remain in the private cloud, while others are hosted in the public cloud.

### Who Can Use It?
- Organizations that require both security and flexibility

### What It's Like?
It is like having your own private computer space while also using shared internet resources whenever needed.

### Characteristics
- Better flexibility
- Sensitive data stays private
- Scale workloads using the public cloud
- Cost optimization

### Example
- A business storing sensitive data in a private cloud while using the public cloud for additional storage or specific applications

---

## Quick Comparison

| Feature | Public Cloud | Private Cloud | Hybrid Cloud |
|----------|-------------|--------------|-------------|
| Ownership | Third-Party Provider | Single Organization | Combination of Both |
| Cost | Low | High | Medium |
| Security | Moderate | High | High |
| Scalability | High | Limited | High |
| Maintenance | Provider Managed | Organization Managed | Shared Responsibility |




# Virtualization

Virtualization is the process of creating multiple virtual machines on a single physical server using a hypervisor. Each VM operates as an independent computer with its own operating system and applications.

Before virtualization, organizations followed the **"One Server = One Application"** approach.

### For example:

* **Server 1** → Web Application
* **Server 2** → Database
* **Server 3** → Mail Server

Most of these servers used only **10–20%** of their CPU and memory, while the remaining resources stayed idle. This resulted in:

* High hardware costs
* Increased power consumption
* More physical space required
* Higher maintenance costs
* Underutilized resources

Virtualization solves this problem by allowing multiple virtual machines to share the same physical server.

---

# How it Works

A software layer called **Hypervisor** is installed on the physical server.

The Hypervisor creates and manages multiple VMs.

Each VM behaves like a completely independent computer with its own:

* Operating System
* CPU allocation
* Memory (RAM)
* Storage
* Network configuration
* Applications

Although all VMs share the same physical hardware, they are isolated from one another.

---

# Hypervisor

A Hypervisor is software that creates, manages, and allocates hardware resources to Virtual Machines.

It acts as a bridge between the physical hardware and the virtual machines.

---

# Types of Hypervisors

## Type 1 Hypervisor (Bare Metal)

A Type 1 Hypervisor runs directly on the physical hardware without requiring a host operating system.

```text
Applications
      ↓
Guest Operating System
      ↓
Hypervisor
      ↓
Physical Hardware
```

### Advantages

* High performance
* Better security
* Used in production environments
* Efficient resource utilization

---

## Type 2 Hypervisor (Hosted)

A Type 2 Hypervisor runs on top of an existing operating system.

```text
Applications
      ↓
Guest Operating System
      ↓
Hypervisor
      ↓
Host Operating System
      ↓
Physical Hardware
```

### Advantages

* Easy to install
* Suitable for learning and testing
* Ideal for personal computers

---

# Diagram of Virtualization

```text
               Physical Server
       +--------------------------+
       | CPU | RAM | Storage | NIC|
       +--------------------------+
                 |
            Hypervisor
                 |
   +-------------+-------------+
   |             |             |
+------+      +------+      +------+
| VM 1 |      | VM 2 |      | VM 3 |
+------+      +------+      +------+
|Ubuntu|      |Windows|     |CentOS|
|Apache|      |SQL DB |     |Jenkins|
+------+      +------+      +------+
```

---

# Advantages of Virtualization

* Better utilization of hardware resources
* Reduced infrastructure costs
* Faster server provisioning
* Easy backup and recovery
* Improved scalability
* Isolation between applications
* Simplified disaster recovery
* Lower power and cooling costs

---

# Disadvantages of Virtualization

* Initial setup can be complex
* Performance overhead compared to bare-metal systems
* Single hardware failure can affect multiple VMs if High Availability is not configured
* Requires skilled administrators

---

# Real-Life Example

Imagine you own a building with 10 empty apartments.

### Without virtualization:

You build 10 separate buildings for 10 families.

### With virtualization:

You build one large building and divide it into 10 apartments.

Each family has its own private apartment, but everyone shares the same building infrastructure.

Similarly:

* **Building** → Physical Server
* **Apartments** → Virtual Machines
* **Building Manager** → Hypervisor
* **Families** → Applications/Users

