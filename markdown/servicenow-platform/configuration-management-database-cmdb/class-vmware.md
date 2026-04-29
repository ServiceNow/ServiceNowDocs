---
title: VMware vCenter Object \[cmdb\_ci\_vcenter\_object\] class
description: Attributes, identification rule, and other important schema structures for Virtual Machine related classes.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CMDB schema model, Explore, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# VMware vCenter Object \[cmdb\_ci\_vcenter\_object\] class

Attributes, identification rule, and other important schema structures for Virtual Machine related classes.

For descriptions of common CMDB tables in a base system, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

## Schema description​

ServiceNow® has an extensive modeling of virtual machines \(VMs\) environment, with classes such as:

-   VMware vCenter Cluster \[cmdb\_ci\_vcenter\_cluster\]
-   VMware vCenter datacenter \[cmdb\_ci\_vcenter\_datacenter\]
-   VMware Virtual Machine Instance \[cmdb\_ci\_vmware\_instance\]

Virtual machines are modeled just like any other server, but with the **IsVirtual** attribute set to **true**.

![Relationships and references in VMWare vCenter Instance schema.](../image/ClassVMWare.png "VMWare vCenter Instance schema structure")

In the diagram above, the 'Discovered' virtual server is referred to as the 'Guest' \(VM object\). Follow the preceding diagram for any further modeling of VMWare components.

## Key reference structures

The Guest has the following important key reference structures:

-   An Instantiates::InstantiatedBy relationship with the cmdb\_ci\_vmware\_instance \(which is the VM instance reported by Center\).
-   A Virtualizes::Virtualized by relationship with ESXi Server \(the hardware with the ESXi virtualization software installed\).
-   Guest \(Discovered, VMObject\) also has a HasRegistered::RegisteredOn relationship to ESXi Server.

## Identification rules

-   Guest operating system: Guest operating system is modeled as Server \(with **IsVirtual** set to **true**\) and therefore identification rules follow the rules for the Server class. In most operating systems, BIOS UUID is reported as serial number. It is essential that you follow proper VMware guidelines to ensure that BIOS UUID is not being reused. Having a cloned BIOS UUID causes issues with identification rules.
-   VM Instances: IRE uses instance MosRef ID as key identifier​.
-   ESX Server: Server is modeled as bare metal Server \(with **IsVirtual** set to **false**\) and therefore applies the Server class identification rules.

