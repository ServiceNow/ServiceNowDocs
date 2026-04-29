---
title: Microsoft Server Infrastructure and License Consumption report
description: Get a unified overview of your Microsoft server products, including their infrastructure, license usage, and exemptions, with detailed justifications for exemptions.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Microsoft Server Infrastructure and License Consumption report

Get a unified overview of your Microsoft server products, including their infrastructure, license usage, and exemptions, with detailed justifications for exemptions.

## Overview of Microsoft Server Infrastructure and License Consumption report

The Microsoft Server Infrastructure and License Consumption report is a single report that gives you insights into Microsoft server product deployments and license usage across various metrics. This comprehensive report includes detailed infrastructure information, covering cloud, on-premise, and standalone environments, as well as license usage and exemptions, complete with detailed justifications for the exemptions.

The report is updated weekly through the scheduled job **SAM - Generate Microsoft Infra Licensing Report**.

To view this report in the Software Asset Workspace, navigate to **License usage** &gt; **Reports** and select the report titled **Microsoft Server Infrastructure and License Consumption**.

## Benefits of the Microsoft Server Infrastructure and License Consumption report

The Microsoft Server Infrastructure and License Consumption report helps in effectively managing Microsoft server licenses across complex hybrid IT environments.

Organizations frequently struggle with the following problems:

-   Fragmented visibility: License data is scattered across various tools and spreadsheets.
-   Complex topologies: Intricate setups such as clusters, virtual machines \(VMs\), cloud instances create challenging licensing scenarios.
-   Compliance risk: Difficulty demonstrating license compliance during audits.
-   Cost optimization: Missed opportunities to identify over-licensing or optimize costs.
-   Cloud migration: Uncertainty regarding license portability and cloud-specific advantages.

This report helps solve these problems by providing a single, authoritative view of your Microsoft server licensing, empowering you to make informed decisions on license procurement, allocation, and optimization.

## Supported license metrics

The following license metrics are considered for all Microsoft server products:

-   Per Core
-   Per Core \(with CAL\)
-   Server \(Per Server\)
-   Server \(Per Instance\)
-   Per Processor

## Layout of the Microsoft Server Infrastructure and License consumption report

The Microsoft Server Infrastructure and License Consumption report follows a hierarchical structure designed to provide clarity and ease of navigation. The report uses a parent-child relationship where infrastructure components are nested under their logical containers:

-   Clusters: Clusters are presented first, containing multiple hosts and VMs, each with different software models installed. Based on how the installation is licensed, either on a host or on a VM, the required licenses are shown on the corresponding host or VM record.
-   Cloud installations:
    -   Cloud installations on hosts or VMs are displayed, including AWS, Microsoft Azure, and Google Cloud Platform.
    -   Cloud-specific licensing information is provided, such as: License Type such as BYOL or License Included, Dual Use Rights, such as Azure-specific benefits for Windows Server, and Edition Flexibility such as Azure benefits for Windows Server and SQL Server.
-   Standalone installations are on-premise devices that aren’t part of any cluster. These include individual physical servers and individual VMs without cluster context.
-   Cross-licensed products: Microsoft products that are licensed by other license metrics are displayed separately. For example, Visual Studio Professional \(Per User metric\) licensing Windows Server.
-   Unlicensed installations: Installations that are either ignored or require action are displayed last, with detailed reasons for their unlicensed status.

To access all the information on the report, scroll all the way to the right of the report. For enhanced usability, you can also export the entire report to an Excel format, facilitating easier review and analysis.

![Microsoft Infrastructure and License Consumption report](../image/microsoft-infrastructure-report.png)

## Understanding licensing layers

<table id="table_yzd_crv_3hc"><thead><tr><th>

Licensing layer

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Physical layer

</td><td>

-   Software is installed only on the physical host.
-   Licenses are assigned at the physical server level.

</td><td>

Windows Server installed on bare metal hardware.

</td></tr><tr><td>

Virtual layer

</td><td>

-   Software is installed only on VMs.
-   Licenses are assigned at the VM level.

</td><td>

SQL Server installed on VMs, with each VM requiring separate licenses.

</td></tr><tr><td>

Mixed layer \(physical/virtual\)

</td><td>

-   Software is installed on both the physical host and VMs.
-   Licenses cover both the host and VMs.
-   Special Handling: For Hyper-V environments, the report shows comprehensive licensing across the host and all VMs.

</td><td>

Windows Server on a Hyper-V host with VMs running Windows Server.

</td></tr></tbody>
</table>## Description of selected metrics in the Microsoft Server Infrastructure and License consumption report

While the full report includes numerous metrics, the metrics that need detailed explanation are mentioned in the table:

|Metric|Description|
|------|-----------|
|Deployment Type|Indicates whether the installation is on-premise, cloud, or standalone.|
|Cluster FQDN|A unique domain name that identifies an entire distributed system, or cluster, to clients and other nodes within the cluster.|
|Host processor count|Number of CPUs that are assigned to the physical host.|
|Host core count|Number of cores within each CPU that is assigned to the physical host.|
|Virtualization technology|Virtualization technology that you’re using to deploy and manage your physical hosts and VMs such as VMware, Hyper-V, RHV, Nutanix.|
|VM movement details|The details with regard to the movement of a VM within or across physical hosts or cloud environments.|
|VM CPU thread count|Maximum number of threads a virtual machine can run concurrently.|
|Software mode licensing|The software model used to license the installation.|
|Product|List of products installed on this device.|
|Server product|Microsoft server products specifically identified for licensing.|
|Software Install|List of software installations related to this licensing requirement.|
|Dual user rights applied|Indicates if Microsoft Azure dual use rights for Windows Server are applied \(Yes, No, or N/A\).|
|Edition flexibility applied|Indicates if Microsoft Azure edition flexibility benefits for Windows Server and SQL Server are applied \(Yes, No, or N/A\)|
|Unlicensed reason|Mentions the reason why an unlicensed installation has been ignored or requires action.|
|Additional notes|Provides details on assessment of all available licensing options. Additionally, explanation of rights that refer to how your rights are calculated and consumed post the reconciliation process is also mentioned.|
|Licensing layer|Indicates where the component is licensed: physical, virtual, or mixed \(physical/virtual\).|
|Licensing status|Status of the installation: Licensed, Unlicensed, Ignored, or Requires Action.|

## Use cases covered in the report

The following use cases are supported by the report:

-   Component installations licensed by suite license.
-   Component installs licensed by suite license but some devices have only one component installed.
-   Component installs licensed by component devices.
-   The product is also licensed by other license metrics.
-   Dual Usage Rights.
-   Licensing at the host layer.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

