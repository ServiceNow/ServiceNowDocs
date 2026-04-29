---
title: Cost-based licensing optimization for Microsoft
description: The cost-based licensing optimization for Microsoft helps you determine the most optimal way to license your Microsoft software products across hybrid infrastructures. With this optimization, you can automatically balance license compliance with cost effectiveness to maximize cost savings.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Cost-based licensing optimization for Microsoft

The cost-based licensing optimization for Microsoft helps you determine the most optimal way to license your Microsoft software products across hybrid infrastructures. With this optimization, you can automatically balance license compliance with cost effectiveness to maximize cost savings.

**Note:** This licensing optimization is automatically included in the Software Asset Management Professional \(com.snc.samp\) plugin, meaning that you do not have to optimize and manage allocations for your Microsoft software rights manually. However, you can choose to manage your allocations manually if the recommended licensing optimizations do not follow your organization's licensing strategy. See [Allocation Management on ServiecNow SAM Pro](https://www.servicenow.com/community/sam-blog/allocation-management-on-servicenow-sam-pro/ba-p/2649232) for more details on manual allocation management.

**Note:** You can bypass this licensing optimization in your hypervisor clusters by applying preferred licensing assignments to the Microsoft software products that are deployed on those clusters. For more information on preferred licensing assignments, see [Create preferred licensing assignments for Microsoft software products deployed on clusters](../task/apply-preferred-licensing-assignments-microsoft-clusters.md).

This licensing optimization is supported by the following Microsoft license types:

-   Per core licenses for Microsoft SQL Server and Microsoft BizTalk Server
-   Per core \(with CAL\) licenses for Microsoft Windows Server, Microsoft Core Infrastructure Server, and Microsoft System Center

See [Supported Microsoft license types](../reference/supported-microsoft-license-types.md) for more information on per core and per core \(with CAL\) licenses.

## Licensing optimization benefits

This licensing optimization provides the following benefits:

-   Helps you determine the cost savings that you have already achieved through your current software entitlement and infrastructure setup.
-   Helps you determine if you can achieve further cost savings by following recommended licensing optimizations.
-   Helps you gain insight into each of the recommended licensing optimizations so that you can understand the reasoning behind them and determine if you want to follow or ignore them.

## Licensing optimization for Microsoft Server products deployed on Microsoft Hyper-V virtualization technology

For Microsoft Windows Server Standard deployments on Microsoft Hyper-V virtualization technology, the Software Asset Management application supports a specialized licensing optimization that can help you achieve better cost efficiency. With this licensing optimization, the Software Asset Management application first licenses the physical hosts that contain Microsoft Windows Server Standard installations. It then licenses the individual VMs that contain Microsoft Windows Server Standard installations. This optimization strategy combines licensing at both the physical host layer and virtual layer, which can help reduce licensing requirements and costs.

## Understanding your licensing optimizations

You can view and gain insight into your recommended licensing optimizations by using the following tables and views:

-   To view in-depth details about each of your recommended licensing optimizations, including the recommended license type and recommend license consumption layer, use the Microsoft Core License Optimization Reports \[samp\_ms\_optimization\_report\] table. See [View realized and potential cost-based licensing optimizations for Microsoft](../task/view-cost-based-licensing-optimizations-microsoft.md) for more details on this table.
-   To view all recommended licensing optimizations for a specific Microsoft cluster, use the SAM Cluster 360º view. See [Understanding your cluster infrastructure](understand-sam-cluster.md) for more information on this view.
-   To view the potential cost savings that you can achieve through your recommended licensing optimizations, use the On-Premises potential savings by optimizing licenses report in the Optimization and savings dashboard of the Software Asset Workspace. See [Optimization and savings dashboard in workspace](../reference/optimization-dashboard-workspace.md) for more information on the dashboard. See [Publisher optimizations for Microsoft](../reference/pub-opt-microsoft.md) for more information on the report.
-   To view the actual cost savings that you have already achieved through your current software entitlement and infrastructure setup, use the On-Premise optimization realized savings report in the Optimization and savings dashboard of the Software Asset Workspace. See [Optimization and savings dashboard in workspace](../reference/optimization-dashboard-workspace.md) for more information on the dashboard. See [Publisher optimizations for Microsoft](../reference/pub-opt-microsoft.md) for more information on the report.

-   **[Microsoft cost-based licensing optimization example](../reference/microsoft-cost-based-licensing-optimization-example.md)**  
This example demonstrates how a software asset manager can optimize Microsoft SQL Server licensing in a cluster deployment.
-   **[View realized and potential cost-based licensing optimizations for Microsoft](../task/view-cost-based-licensing-optimizations-microsoft.md)**  
View the realized and potential cost-based licensing optimizations for your Microsoft software products. Gain an in-depth understanding of each licensing optimization so that you can maximize cost savings across your Microsoft deployments.

**Parent Topic:**[Software Asset Management publisher pack for Microsoft](microsoft-publisher-pack.md)

