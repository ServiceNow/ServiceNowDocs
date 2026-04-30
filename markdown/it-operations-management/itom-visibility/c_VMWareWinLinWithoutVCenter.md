---
title: VMware Workstation - Legacy
description: In the basic VMware system, the VMware Workstation runs on a Windows or Linux host machine.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-12-02"
reading_time_minutes: 1
keywords: [Vmware workstation, Vmware system]
breadcrumb: [Discovery for VMware virtual machines, Discovery for VMware virtualization, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# VMware Workstation - Legacy

In the basic VMware system, the VMware Workstation runs on a Windows or Linux host machine.

This system can clone instances from templates, but cannot be automated. The relationships between VMware components for this type of installation are shown in the following diagram:

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
</table>**Parent Topic:**[Discovery for VMware virtual machines](c_VMwareVirtualMachines.md)

