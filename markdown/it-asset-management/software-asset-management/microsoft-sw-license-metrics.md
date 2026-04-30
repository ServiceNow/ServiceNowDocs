---
title: Microsoft Per Core licensing rules
description: The Per Core licensing model is used by many Microsoft server products, such as SQL Server and BizTalk Server. It's useful when counting users or devices connecting to the software is difficult, often for internet-facing software.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Software license maintenance, Explore, Software Asset Management, IT Asset Management]
---

# Microsoft Per Core licensing rules

The Per Core licensing model is used by many Microsoft server products, such as SQL Server and BizTalk Server. It's useful when counting users or devices connecting to the software is difficult, often for internet-facing software.

Therefore, the Per Core licensing model is commonly used for enterprise software like Microsoft SQL Server.

The licensing rules for on-premise installations of these products and the cloud installations are separate. The cloud licensing rules follow Bring Your Own License \(BYOL\). For more information, see [Licensing rules for BYOL and BYOS](../reference/byol-license-rules.md).

To license the on-premise installation of these products using the Per Core licensing model, consider the following two options.

-   Licensing by physical cores, also known as licensing by physical hosts
-   Licensing by individual virtual machines

**Note:** You can either allocate to individual hosts or individual virtual machines, not to cluster.

You can either allocate manually, or the Software Asset Management application can automatically select the most cost-effective licensing option based on optimization criteria. The number of core licenses required depends on whether you’re licensing the physical server based on its physical cores or licensing individual virtual machines.

For more information about how to perform allocation, see [Allocation management](https://www.servicenow.com/community/sam-blog/allocation-management-on-servicenow-sam-pro/ba-p/2649232) and how the Software Asset Management application performs automated optimization, see [View realized and potential cost-based licensing optimizations for Microsoft](../task/view-cost-based-licensing-optimizations-microsoft.md).

**Note:** Both options, whether licensing by physical cores or licensing by individual virtual machines, come with their own set of Microsoft rules that must be followed. For more information, see [SQL Server](https://www.microsoft.com/licensing/terms/productoffering/SQLServer/EAEAS).

Other licensing models, such as the Server CAL licensing model, are also available for these products.

## Licensing by physical cores

The Software Asset Management application supports licensing by physical core rules, introduced by Microsoft in 2016.

<table id="table_g5f_rzp_rbc"><thead><tr><th>

Rule

</th><th>

SQL Server Standard

</th><th>

SQL Server Enterprise

</th></tr></thead><tbody><tr><td>

Applicability

</td><td>

Not allowed**Note:** Only allowed to be licensed through individual virtual machines.

</td><td>

The number of licenses required equals the number of physical cores on the licensed server.The physical cores on servers are equal to `CPU count * Core count`.

</td></tr><tr><td>

Min licenses required

</td><td>

Not allowed**Note:** Only allowed to be licensed through individual virtual machines.

</td><td>

4 licenses per physical processor

</td></tr><tr><td>

Virtualization rights

</td><td>

Not allowed**Note:** Only allowed to be licensed through individual virtual machines.

</td><td>

-   Without software assurance or subscription licenses, run virtual machines equal to the number of core licenses assigned to the physical server.

**Note:** Each additional virtual machine would require an additional core license.

-   With active software assurance or subscription license, run an unlimited number of virtual machines if all physical cores on the server are fully licensed.

</td></tr><tr><td>

Failover rights

</td><td>

Not allowed**Note:** Only allowed to be licensed through individual virtual machines.

</td><td>

For each server operating system environment \(OSE\) licensed with SQL Server subscription licenses covered by active Software Assurance, you can use the following passive replicas ahead of a failover event:-   One passive failover replica for High Availability in a separate OSE
-   One passive failover replica for Disaster Recovery in a separate OSE
-   One passive failover replica for Disaster Recovery in a single virtual machine or instance on Azure

</td></tr><tr><td>

Components services licensing

</td><td>

Not allowed**Note:** Only allowed to be licensed through individual virtual machines.

</td><td>

The software components of a single SQL Server license can't be separated. An OSE running any of the licensed components of SQL Server requires its own license. For more information about SQL Server components, see [Editions and supported features of SQL Server 2022](https://learn.microsoft.com/en-us/sql/sql-server/editions-and-components-of-sql-server-2022?view=sql-server-ver16).

</td></tr></tbody>
</table>When deploying Microsoft products like Windows Server or System Center \(using the Per Core license model\) on cluster virtualization technologies such as VMware vSphere, Microsoft Hyper-V, or Nutanix Acropolis HyperVisor \(AHV\), the number of licenses required for the physical host depends on the virtual machines that could potentially migrate to it within the cluster.

Technologies like VMware vMotion, which enables live migration of virtual machines across all hosts, and host affinity, which helps lock virtual machines to hosts within a cluster, manage the movement of virtual machines across hosts. To understand more about cluster virtualization technology and its support on the Software Asset Management application, see [Understanding your cluster infrastructure](understand-sam-cluster.md).

According to Microsoft licensing rules, if a virtual machine with a Microsoft product like Windows Server installed is hosted on one server but can potentially migrate to another, the destination server must be licensed as if the virtual machine is already running on it.

**Tip:** As only the Enterprise edition license can be used for this option and you must license the physical host based on the number of virtual machines that can run on it, this licensing option can be more costly.

## Licensing by virtual machines

The Software Asset Management application supports licensing by individual virtual machines rules, introduced by Microsoft in 2022.

**Note:** This licensing option is the only option available for SQL Server Standard Edition when using the Per Core licensing model.

<table id="table_gpd_tbq_rbc"><thead><tr><th>

Rule

</th><th>

SQL Server Standard and SQL Server Enterprise

</th></tr></thead><tbody><tr><td>

Required number of licenses

</td><td>

Equals the number of virtual cores on the virtual machineThe virtual cores on servers are equal to `CPU count * Core count * CPU thread count`.

</td></tr><tr><td>

Min licenses required

</td><td>

4 licenses per virtual machine

</td></tr><tr><td>

Software assurance or subscription license**Note:** The option to license by virtual machine is only available with software assurance or a subscription license.

</td><td>

Required

</td></tr><tr><td>

License mobility within Server farms \(Software assurance benefit\)**Note:** Licenses can be reassigned within the same server farm as often as needed. The 90-day rule applies only when moving to another server farm or cloud provider.

</td><td>

Supported

</td></tr><tr><td>

Component services licensing

</td><td>

The software components of a single SQL Server license can't be separated. An OSE running any of the licensed components of SQL Server requires its own license. For more information about SQL Server components, see [Editions and supported features of SQL Server 2022](https://learn.microsoft.com/en-us/sql/sql-server/editions-and-components-of-sql-server-2022?view=sql-server-ver16).

</td></tr><tr><td>

Failover rights

</td><td>

For each server OSE licensed with SQL Server subscription licenses or licenses covered by active software assurance, use the following passive replicas ahead of a failover event:-   One passive failover replica for High Availability in a separate OSE
-   One passive failover replica for Disaster Recovery in a separate OSE
-   One passive failover replica for Disaster Recovery in a single virtual machine or instance on Azure

</td></tr></tbody>
</table>**Parent Topic:**[Software license maintenance](software-license-maintenance.md)

