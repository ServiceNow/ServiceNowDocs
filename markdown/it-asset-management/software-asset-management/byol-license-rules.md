---
title: Licensing rules for BYOL and BYOS
description: View the bring your own license \(BYOL\) licensing rules for Microsoft and Oracle products in public cloud environments. In addition, view bring your own subscription \(BYOS\) licensing rules for Red Hat Enterprise Linux \(RHEL\) products in public cloud environments. Licensing rules can differ for virtual machines that reside on shared hosts or dedicated hosts across different cloud providers.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Licensing rules for BYOL and BYOS

View the bring your own license \(BYOL\) licensing rules for Microsoft and Oracle products in public cloud environments. In addition, view bring your own subscription \(BYOS\) licensing rules for Red Hat Enterprise Linux \(RHEL\) products in public cloud environments. Licensing rules can differ for virtual machines that reside on shared hosts or dedicated hosts across different cloud providers.

## Licensing rules for Microsoft Windows Server and Microsoft SQL Server

**Note:** The following tables list only a subset of rules for Windows Server and SQL Server BYOL. Refer to the official Windows Server and SQL Server websites for the complete list of licensing rules.

<table id="table_ifm_zzj_2nb"><thead><tr><th>

Cloud provider

</th><th>

Instance type

</th><th>

With software assurance

</th><th>

Without software assurance

</th></tr></thead><tbody><tr><td rowspan="2">

AWS for Windows Server

</td><td>

Shared host

</td><td>

BYOL isn’t supported because Windows Server doesn’t have license mobility rights.

</td><td>

BYOL isn’t supported.

</td></tr><tr><td>

Dedicated host

</td><td>

-   BYOL is supported for purchases or software releases only before October 1, 2019.
-   License by physical host.
-   Unlimited virtualization for Windows DC for purchases before October 1, 2019.

</td><td>

-   BYOL is supported for purchases or software releases only before October 1, 2019.
-   License by physical host.
-   Unlimited virtualization for Windows DC for purchases before October 1, 2019.

</td></tr><tr><td rowspan="2">

Microsoft Azure for Windows Server

</td><td>

Shared host

</td><td>

-   BYOL is supported using Microsoft Azure Hybrid Benefits \(AHB\).
-   Enough eligible core licenses must be allocated to cover all cores on the virtual machines \(VMs\) that are running.
-   Each processor license is equivalent to 16 core licenses.
-   A minimum of eight core licenses are allocated for using AHB.
-   Windows DC allows concurrent or dual use rights.

**Note:** Microsoft Windows Server Data Center provides the option of dual use rights, enabling you to utilize your Windows Server licenses simultaneously on Microsoft Azure and on licensed servers within your data centers. This feature, Azure Hybrid Benefit is only available on Microsoft Azure. For more information, see [Azure Hybrid Benefit for Windows Server](https://learn.microsoft.com/en-us/windows-server/get-started/azure-hybrid-benefit?tabs=azure).

-   Edition flexibility: Windows Standard can license Windows DC.

</td><td>

BYOL isn't supported.

</td></tr><tr><td>

Dedicated host

</td><td>

-   BYOL is supported using Microsoft Azure Hybrid Benefits \(AHB\).
-   License by virtual machine or available cores. Only for Windows DC.
-   Unlimited virtualization for Windows DC if licensing available cores.
-   Windows DC allows concurrent or dual use rights for virtual machines only.

**Note:** Microsoft Windows Server Data Center provides the option of dual use rights, enabling you to utilize your Windows Server licenses simultaneously on Microsoft Azure and on licensed servers within your data centers. This feature, Azure Hybrid Benefit is only available on Microsoft Azure. For more information, see [Azure Hybrid Benefit for Windows Server](https://learn.microsoft.com/en-us/windows-server/get-started/azure-hybrid-benefit?tabs=azure).


</td><td>

-   BYOL is supported for purchases or software releases only before October 1, 2019.
-   License for total physical cores for purchases before October 1, 2019.
-   Unlimited virtualization for Windows DC for purchases before October 1, 2019.

</td></tr><tr><td rowspan="2">

GCP for Windows Server

</td><td>

Shared host

</td><td>

BYOL isn't supported because Windows Server doesn't have license mobility rights.

</td><td>

BYOL isn't supported.

</td></tr><tr><td>

Dedicated host

</td><td>

BYOL isn't supported.

</td><td>

BYOL isn't supported.

</td></tr></tbody>
</table><table id="table_ytw_53k_2nb"><thead><tr><th>

Cloud provider

</th><th>

Instance type

</th><th>

With software assurance

</th><th>

Without software assurance

</th></tr></thead><tbody><tr><td rowspan="2">

AWS for SQL Server

</td><td>

Shared host

</td><td>

-   BYOL is supported via license mobility rights.
-   License virtual cores \(vCPU\) - minimum of four cores per virtual machine.

</td><td>

BYOL isn't supported.

</td></tr><tr><td>

Dedicated host

</td><td>

-   BYOL is supported via License Mobility rights.
-   License by physical host.
-   Unlimited virtualization \(SQL Server Enterprise\) for purchases before October 1, 2019.

</td><td>

-   BYOL is supported for purchases or software releases only before October 1, 2019.
-   License by total physical cores for purchases before October 1, 2019.
-   Unlimited virtualization for Windows DC for purchases before October 1, 2019.

</td></tr><tr><td rowspan="2">

Microsoft Azure for SQL Server

</td><td>

Shared host

</td><td>

-   BYOL is supported using Microsoft Azure Hybrid Benefits \(AHB\).
-   Edition flexibility: 1 SQL Enterprise license on-premise can cover 4 SQL Server Standard cores. Similarly, 4 SQL Server standard licenses on-premise can cover 1 SQL Server Enterprise.
-   License virtual cores \(vCPU\) - minimum of four cores per virtual machine.

</td><td>

BYOL isn’t supported.

</td></tr><tr><td>

Dedicated host

</td><td>

-   BYOL is supported using Microsoft Azure Hybrid Benefits \(AHB\).
-   License by virtual machine or available cores \(SQL Server Enterprise\).
-   License by virtual machine or total cores \(SQL Server Standard\).
-   Unlimited virtualization \(SQL Server Enterprise\) if licensing available cores.

</td><td>

-   BYOL is supported for purchases or software releases only before October 1, 2019.
-   License by total physical cores for purchases before October 1, 2019.

</td></tr><tr><td rowspan="2">

GCP for SQL Server

</td><td>

Shared host

</td><td>

-   BYOL is supported via license mobility rights.
-   License virtual cores \(vCPU\) - minimum of four cores per virtual machine.

</td><td>

BYOL isn’t supported.

</td></tr><tr><td>

Dedicated host

</td><td>

BYOL isn’t supported.

</td><td>

BYOL isn’t supported.

</td></tr></tbody>
</table>## Licensing rules for Oracle Database and Oracle WebLogic Server

**Note:** The following tables list only a subset of rules for Oracle Database and Oracle WebLogic Server BYOL. Refer to the official Oracle Database and Oracle WebLogic Server websites for the complete list of licensing rules.

**Note:** Unless otherwise specified, licensing rules are the same for both AWS and Microsoft Azure.

<table id="table_h23_spl_spb"><thead><tr><th>

Licensing type

</th><th>

Licensing rule

</th></tr></thead><tbody><tr><td>

Per Processor licensing

</td><td>

Licensing is based on the number of vCPUs that the Oracle database is installed or running on. Different licensing rules are applied based on the Oracle Database version that is installed or running.**Note:** The Oracle Processor Core Factor Table is not applicable in cloud environments.

 -   **Oracle Database Standard Edition, Standard Edition One, and Standard Edition 2**

Four vCPUs are equivalent to one socket, and one socket requires one license.

The number of vCPUs is rounded up to the nearest multiple of four. For example, an Oracle database that is running on 10 vCPUs requires a total of three licenses.

-   **Oracle Database Enterprise Edition**

If hyper-threading is enabled, one license is required for every two vCPUs on which you install or run an Oracle database. If hyper-threading isn’t enabled, one license is required for every vCPU on which you install or run an Oracle database.


</td></tr><tr><td>

Named User licensing

</td><td>

One license is required for every user or physical device that accesses an Oracle database.Different licensing minimums are applied based on the Oracle Database edition that your users and devices are accessing:

-   **Oracle Database Standard Edition and Standard Edition One**

These database editions don’t have any licensing minimums.

-   **Oracle Database Standard Edition 2**

You must have a minimum of 10 licenses per eight vCPUs.

-   **Oracle Database Enterprise Edition**

You must have a minimum of either 25 licenses per vCPU or the total number of users and devices that are accessing this database edition. The licensing minimum is set to the larger of the two values.


</td></tr><tr><td>

Oracle Database option and management pack licensing

</td><td>

Database options and management packs must be licensed separately from database servers.The following database options and management packs aren’t supported in cloud environments:

-   Oracle Real Application Clusters \(RAC\)
-   Oracle Data Mining
-   Oracle Change Management Pack
-   Oracle Provisioning and Patch Automation Pack for Database

</td></tr><tr><td>

Oracle Database option licensing for Active Data Guard

</td><td>

If you’re using the Oracle Active Data Guard option on an Oracle Enterprise Edition database, the primary database instance and read replicas that are associated with that database each require one Oracle Database Enterprise Edition license and one Oracle Active Data Guard license.**Note:** The Active Data Guard option is available only on Oracle Database Enterprise Edition.

</td></tr><tr><td>

Unlimited License Agreement \(ULA\) licensing

</td><td>

Licenses that are acquired through an Unlimited License Agreement \(ULA\) are supported in authorized cloud environments. However, certification of these licenses isn’t required at the end of the ULA term.

</td></tr><tr><td>

High availability \(Multi-AZ\) licensing

</td><td>

High availability, or Multi-AZ, deployments require twice the number of licenses as Single-AZ deployments so that they can account for standby Oracle Database instances.

</td></tr></tbody>
</table>In addition to these Oracle Database licensing rules, consider the following vCPU size limitations when you’re setting up an Oracle deployment in the cloud. These size limitations can help you determine the maximum number of licenses that are supported on your cloud instances.

**Note:** The vCPU size limitations are the same for both AWS and Microsoft Azure

|Oracle Database edition|vCPU size limitation|
|-----------------------|--------------------|
|Oracle Database Standard Edition|Oracle Database Standard Edition is supported only on cloud instances that have a maximum of 16 vCPUs.|
|Oracle Database Standard Edition One and Standard Edition 2|Oracle Database Standard Edition One and Standard Edition 2 are supported only on cloud instances that have a maximum of eight vCPUs.|
|Oracle Database Enterprise Edition|Oracle Database Enterprise Edition is supported on all cloud instances, regardless of the vCPU count.|

<table id="table_zd2_yzf_lvb"><thead><tr><th>

Licensing type

</th><th>

Licensing rule

</th></tr></thead><tbody><tr><td>

Per Processor licensing

</td><td>

Licensing is based on the number of vCPUs that the Oracle WebLogic server is installed or running on. Different licensing rules are applied based on the Oracle WebLogic Server version that is installed or running.**Note:** The Oracle Processor Core Factor Table is not applicable in cloud environments.

 -   **Oracle WebLogic Server Standard Edition**

Four vCPUs are equivalent to one socket, and one socket requires one license.

The number of vCPUs is rounded up to the nearest multiple of four. For example, an Oracle WebLogic server that is running on seven vCPUs requires a total of two licenses.

-   **Oracle WebLogic Server Enterprise and Suite Edition**

If hyper-threading is enabled, one license is required for every two vCPUs on which you install or run an Oracle WebLogic Server. If hyper-threading isn’t enabled, one license is required for every vCPU on which you install or run an Oracle WebLogic server.


</td></tr><tr><td>

Named User licensing

</td><td>

One license is required for every user or physical device that accesses an Oracle WebLogic server.Different licensing minimums are applied based on the Oracle WebLogic Server edition that your users and devices are accessing:

-   **Oracle WebLogic Server Standard Edition**

You must have a minimum of either 10 licenses per eight vCPUs or the total number of users and devices that are accessing this WebLogic Server version. The licensing minimum is set to the larger of the two values.

-   **Oracle WebLogic Server Enterprise and Suite Edition**

If hyper-threading is enabled, you must have a minimum of either 10 licenses per two vCPUs or the total number of users and devices that are accessing this WebLogic Server edition.

If hyper-threading isn’t enabled, you must have a minimum of either 10 licenses per vCPU or the total number of users and devices that are accessing this WebLogic Server edition.

The licensing minimum is set to the larger of the two values.


</td></tr></tbody>
</table>## Licensing rule for Red Hat Enterprise Linux Server

One on-premise subscription license is required for every two cloud-based virtual machines \(VMs\) on which you install and run Red Hat Enterprise Linux Server.

**Note:** This rule is only one of the licensing rules for Red Hat Enterprise Linux Server BYOS. Refer to the official Red Hat Enterprise Linux website for the complete list of licensing rules.

**Parent Topic:**[Software Asset Management references](references.md)

