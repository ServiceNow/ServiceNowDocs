---
title: Microsoft Core License Optimization Reports fields
description: Field descriptions for the Microsoft Core License Optimization Reports \[samp\_ms\_optimization\_report\] table.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Microsoft Core License Optimization Reports fields

Field descriptions for the Microsoft Core License Optimization Reports \[samp\_ms\_optimization\_report\] table.

<table id="table_aly_wb4_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product

</td><td>

Microsoft software product that you are optimizing licensing for.

</td></tr><tr><td>

Cluster/Host Type

</td><td>

Indicates whether the recommended licensing optimization applies to a cluster or a standalone physical host.

</td></tr><tr><td>

Virtualization Technology

</td><td>

Virtualization technology that you are using to run virtual machines \(VMs\) within the cluster or on the standalone physical host.

</td></tr><tr><td>

Cluster/Host Reference

</td><td>

Cluster or standalone physical host that the recommended licensing optimization applies to.

</td></tr><tr><td>

Host Affinity Configured

</td><td>

Indicates if host affinity rules are configured for the cluster.**Note:** Host affinity rules are applicable to clusters only. If the **Cluster/Host Type** field is set to **Cluster**, this field can be set to either **true** or **false**. If the **Cluster/Host Type** field is set to **Standalone Host**, this field is automatically set to **false**.

</td></tr><tr><td>

Number of Hosts

</td><td>

Number of physical hosts. If the **Cluster/Host Type** field is set to **Standalone Host**, this field is set to **1**. If the **Cluster/Host Type** field is set to **Cluster**, this field is set to the total number of physical hosts within the cluster.

</td></tr><tr><td>

Host Cores

</td><td>

Number of cores within each CPU that is assigned to your physical hosts. If the **Cluster/Host Type** field is set to **Standalone Host**, this field is set to the number of cores within each CPU that is assigned to the standalone physical host. If the **Cluster/Host Type** field is set to **Cluster**, this field is set to the number of cores within each CPU that is assigned to a physical host within the cluster.

</td></tr><tr><td>

Number of VMs

</td><td>

Number of VMs within the cluster or on the standalone physical host.

</td></tr><tr><td>

VM Cores

</td><td>

Number of virtual cores within each virtual CPU \(vCPU\) that is assigned to your VMs. If the **Cluster/Host Type** field is set to **Standalone Host**, this field is set to the number of virtual cores within each vCPU that is assigned to the VMs on the standalone physical host. If the **Cluster/Host Type** field is set to **Cluster**, this field is set to the number of virtual cores within each vCPU that is assigned to the VMs within the cluster.

</td></tr><tr><td>

Number of VMs with software installations

</td><td>

Number of VMs that the Microsoft software product is installed on.

</td></tr><tr><td>

Host Core Licenses Required

</td><td>

Number of rights that are required for licensing either the physical hosts within the cluster or the standalone physical host.

</td></tr><tr><td>

VM Core Licenses Required

</td><td>

Number of rights that are required for licensing the VMs within the cluster or on the standalone physical host.

</td></tr><tr><td>

Current License Consumption

</td><td>

Type of license and total number of rights that you are currently consuming.

</td></tr><tr><td>

Current License Consumption Layer

</td><td>

Layer on which you are currently consuming rights. The options are **Physical**, **Virtual**, and **Physical/Virtual**.

</td></tr><tr><td>

Recommended License Consumption

</td><td>

Type of license and total number of rights that you are recommended to consume.

</td></tr><tr><td>

Recommended License Consumption Layer

</td><td>

Layer on which you are recommended to consume rights. The options are **Physical**, **Virtual**, and **Physical/Virtual**.

</td></tr><tr><td>

Conservative License Consumption

</td><td>

Conservative way to consume rights without applying any licensing optimizations. For example, you can consume rights for your Microsoft Windows Server Data Center or Microsoft SQL Server Enterprise licenses on the host layer.

</td></tr><tr><td>

Conservative License Cost

</td><td>

Total license cost based on the conservative license consumption.

</td></tr><tr><td>

Recommended License Cost

</td><td>

Total license cost based on the recommended license consumption and license consumption layer.

</td></tr><tr><td>

Current License Cost

</td><td>

Total license cost based on the current license consumption and license consumption layer.

</td></tr><tr><td>

Recommended License Applied

</td><td>

Indicates if the recommended licensing optimization has been implemented on the cluster or standalone physical host.

</td></tr><tr><td>

Licensing Status

</td><td>

Licensing status of the cluster or standalone physical host. The options are **Licensed** and **Unlicensed**.

</td></tr><tr><td>

Has Allocation

</td><td>

Indicates if you have enough rights to allocate to the cluster or standalone physical host.

</td></tr><tr><td>

Recommendation Details

</td><td>

Summary of the recommended licensing optimization.

</td></tr><tr><td>

Optimization Savings Achieved

</td><td>

Indicates if you have saved money by implementing the recommended licensing optimization.

</td></tr><tr><td>

Optimization Realized Savings

</td><td>

Amount of money that you have saved by implementing the recommended licensing optimization.

</td></tr><tr><td>

Potential Savings

</td><td>

Amount of money that you can save by implementing the recommended licensing optimization.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

