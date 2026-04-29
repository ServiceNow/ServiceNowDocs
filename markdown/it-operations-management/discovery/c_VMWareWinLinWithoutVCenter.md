---
title: VMware Workstation
description: In the basic VMware system, the VMware Workstation runs on a Windows or Linux host machine, but not managed directly thorugh vCenter.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [VMware workstation, VMware system]
breadcrumb: [Discovery for VMware virtualization, Discovery for data-center virtualization, Discovery, ITOM Visibility, IT Operations Management]
---

# VMware Workstation

In the basic VMware system, the VMware Workstation runs on a Windows or Linux host machine, but not managed directly thorugh vCenter.

This system clones instances from templates, but can't be automated. The relationships between VMware components for this type of installation are in the following diagram:

![VMware Workstation relationships](../image/VMWareNoVCenterDiagram.png "VMware Workstation relationships")

<table id="table_VMwareComponentRelationshipsOnWindowsOrLinuxWithoutVCenter"><thead><tr><th>

Component

</th><th>

Relationships

</th></tr></thead><tbody><tr><td>

Windows or Linux Server

</td><td>

Runs the VMware application

</td></tr><tr><td>

VMware application

</td><td>

-   Runs on a Windows or Linux host machine
-   Has registered VM instances
-   Virtualizes virtual machines

</td></tr><tr><td>

VM Instances \(including images and templates\)

</td><td>

-   Registers on the VMware application
-   Instantiated by individual virtual machines

</td></tr><tr><td>

Virtual machines

</td><td>

-   Instantiates VM instances
-   Virtualized by VMware application

</td></tr></tbody>
</table>