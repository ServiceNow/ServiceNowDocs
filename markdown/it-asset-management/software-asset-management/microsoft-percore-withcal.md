---
title: Microsoft Per Core \(with CAL\) licensing rules
description: The Per Core \(with CAL\) metric licensing model is followed by various Microsoft Server products such as Windows Server, System Center, and Core Infrastructure Server Suite. The number of licenses depends on the number of installations and operating system environments \(OSE\).
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Software license maintenance, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Microsoft Per Core \(with CAL\) licensing rules

The Per Core \(with CAL\) metric licensing model is followed by various Microsoft Server products such as Windows Server, System Center, and Core Infrastructure Server Suite. The number of licenses depends on the number of installations and operating system environments \(OSE\).

The licensing rules for on-premise installations of these products and the cloud installations are separate. The cloud licensing rules follow Bring Your Own License \(BYOL\). For more information, see [Licensing rules for BYOL and BYOS](../reference/byol-license-rules.md).

To license the on-premise installation of these products using the Per Core \(with CAL\) licensing model, consider the following two options.

-   Licensing by physical cores, also known as licensing by physical hosts
-   Licensing by individual virtual machines

**Note:** You can either allocate to individual hosts or individual virtual machines, not to cluster.

You can either allocate manually, or the Software Asset Management application can automatically select the most cost-effective licensing option based on optimization criteria. For more information about how to perform allocation, see [Allocation management](https://www.servicenow.com/community/sam-blog/allocation-management-on-servicenow-sam-pro/ba-p/2649232) and how the Software Asset Management application performs automated optimization, see [View realized and potential cost-based licensing optimizations for Microsoft](../task/view-cost-based-licensing-optimizations-microsoft.md).

**Note:** Both options, whether licensing by physical cores or licensing by individual virtual machines, come with their own set of Microsoft rules that must be followed. For more information, see [Windows Server Standard, Datacenter, and Essentials](https://www.microsoft.com/licensing/terms/productoffering/WindowsServerStandardDatacenterEssentials/EAEAS).

## Licensing by physical cores

The Software Asset Management application supports licensing by physical core rules, introduced by Microsoft in 2016.

<table id="table_g5f_rzp_rbc"><thead><tr><th>

Rule

</th><th>

Windows Server Standard

</th><th>

Windows Server Data Center

</th></tr></thead><tbody><tr><td>

Required number of licenses

</td><td colspan="2">

Equals the number of physical cores on the licensed serverThe physical cores on servers are equal to `CPU count * Core count`.

</td></tr><tr><td>

Min licenses required

</td><td colspan="2">

-   8 per physical processor
-   16 licenses per server

</td></tr><tr><td>

CAL requirement

</td><td colspan="2">

Device or user CALs are required for users or devices accessing the server

</td></tr><tr><td>

Virtualization rights

</td><td>

Rights to use 2 virtual machines if all cores of the host are licensed with the option for license stacking**Note:** You must license the host again to get rights to use 2 additional virtual machines.

</td><td>

Rights to run unlimited virtual machines when all cores of the host are licensed

</td></tr><tr><td>

License mobility within Server Farms \(Software assurance benefit\)**Note:** License mobility isn't available for Windows Server. Licenses can be reassigned to servers as often as every 90 days.

</td><td colspan="2">

Not supported

</td></tr></tbody>
</table>When deploying Microsoft products like Windows Server or System Center \(using the core with CAL license model\) on cluster virtualization technologies such as VMware vSphere, Microsoft Hyper-V, or Nutanix AHV, the number of licenses required for the physical host depends on the virtual machines that could potentially migrate to it within the cluster.

Technologies like VMware vMotion, which enables live migration of virtual machines across all hosts, and host affinity, which helps lock virtual machines to hosts within a cluster, manage the movement of virtual machines across hosts. To understand more about cluster virtualization technology and its support on the Software Asset Management application, see [Understanding your cluster infrastructure](understand-sam-cluster.md).

According to Microsoft licensing rules, if a virtual machine with a Microsoft product like Windows Server installed is hosted on one server but can potentially migrate to another, the destination server must be licensed as if the virtual machine is already running on it.

## Licensing by virtual machines

The Software Asset Management application supports licensing by individual virtual machines rules, introduced by Microsoft in 2022.

<table id="table_gpd_tbq_rbc"><thead><tr><th>

Rule

</th><th colspan="2">

Windows Server Standard and Windows Server Data Center

</th></tr></thead><tbody><tr><td>

Required number of licenses

</td><td colspan="2">

Equals the number of virtual cores on the virtual machineThe virtual cores on servers are equal to `CPU count * Core count * CPU thread count`.

</td></tr><tr><td>

Min licenses required

</td><td colspan="2">

8 licenses per virtual machine

</td></tr><tr><td>

Software assurance or subscription license**Note:** The option to license by virtual machine is only available with software assurance or a subscription license.

</td><td colspan="2">

Required

</td></tr><tr><td>

License mobility within Server farms \(Software assurance benefit\)**Note:** Licenses can be reassigned within the same server farm as often as needed. The 90-day rule applies only when moving to another server farm or cloud provider.

</td><td colspan="2">

Supported

</td></tr></tbody>
</table>**Parent Topic:**[Software license maintenance](software-license-maintenance.md)

