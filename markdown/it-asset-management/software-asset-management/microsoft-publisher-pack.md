---
title: Software Asset Management publisher pack for Microsoft
description: The Software Asset Management publisher pack for Microsoft helps you track your license compliance position using Microsoft licensing metrics.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Asset Management publisher pack for Microsoft

The Software Asset Management publisher pack for Microsoft helps you track your license compliance position using Microsoft licensing metrics.

**Important:** To use the publisher pack, activate the Software Asset Management Professional for Microsoft plugin \(com.snc.samp.microsoft\).

Microsoft offers a wide variety of products that span from database servers to subscription services. Each Microsoft product follows its own licensing model, which can make it hard to track your license compliance position. With the Software Asset Management publisher pack for Microsoft, you can accurately track your license compliance position for Microsoft products. Reconciliation identifies licenses that are out of compliance and provides a list of remediation options. For more information, see [Software reconciliation for compliance](c_SAMReconciliation.md).

To learn more about Microsoft licensing models, see [Microsoft licensing](https://www.microsoft.com/en-us/Licensing).

Set up ServiceNow Discovery to identify Microsoft installations on your network. For more information, see [Data collected by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/data-collected-by-itom-visibility.md).

## Licensing models

The Software Asset Management publisher pack for Microsoft supports the following licensing models.

-   Per User
-   Per Device
-   Per Core
-   Per Core \(with CAL\)
-   User CAL
-   Device CAL
-   Server \(per instance\)
-   Server \(per server\)
-   Per Processor
-   User Subscription
-   Software Assurance

For more information, see [Supported Microsoft license types](../reference/supported-microsoft-license-types.md).

If a PPN with a P+SA license type lacks a version assignment, a software model with the exact version is automatically applied. This automatic version assignment occurs both when creating an entitlement and when importing entitlements from a Microsoft License Statement \(MLS\). This automatic action correctly applies Microsoft assurance benefits to an entitlement. For details on the upgrade history of an entitlement, navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations** &gt; **Software entitlements** &gt; **Upgrade history**.

The **SAMP - Update generic PSA entitlements** fix script automatically updates the existing P+SA entitlements with version as anything, with the specific version, and applies the appropriate licensing terms.

## Permission types

The Software Asset Management publisher pack for Microsoft supports the following permission types to access data through Microsoft APIs. You can select the appropriate type of permission for your application to access data correctly and securely.

-   **Delegated type permission**

    These permissions enable the application to access data on behalf of a signed-in user, which means the application can access only the data that a signed-in user has access to.

-   **Application type permission**

    These permissions enable the application to access data without a signed-in user. The application can access any data that the permission is associated with.


-   **[Microsoft SQL Server licensing in container deployments](microsoft-licensing-software-containers.md)**  
The Software Asset Management publisher pack for Microsoft supports licensing rules for Microsoft SQL Server products that are deployed across both on-premise and cloud environments using Docker containers.
-   **[Microsoft Server licensing on Microsoft Hyper-V virtualization technology](microsoft-server-licensing-hyper-v-virtualization-technology.md)**  
The Software Asset Management publisher pack for Microsoft supports licensing rules for Microsoft Server products, such as Microsoft Windows Server, that are deployed on Microsoft Hyper-V virtualization technology.
-   **[Microsoft SQL Server licensing in high availability configurations](microsoft-sql-server-ha-configurations.md)**  
The Software Asset Management publisher pack for Microsoft supports licensing rules for Microsoft SQL Server deployed through high availability and disaster recovery solutions, such as Always On availability groups.
-   **[Manage licenses for Microsoft Visual Studio](../task/manage-visual-studio-licenses.md)**  
Manage your Visual Studio subscriptions with the Software Asset Management publisher pack for Microsoft. Verify license compliance and detect unlicensed installations. Reduce licensing costs by identifying subscriptions that are allocated but aren’t being used.
-   **[Cost-based licensing optimization for Microsoft](cost-based-microsoft-cluster-licensing.md)**  
The cost-based licensing optimization for Microsoft helps you determine the most optimal way to license your Microsoft software products across hybrid infrastructures. With this optimization, you can automatically balance license compliance with cost effectiveness to maximize cost savings.
-   **[Create preferred licensing assignments for Microsoft software products deployed on clusters](../task/apply-preferred-licensing-assignments-microsoft-clusters.md)**  
Create and define preferred licensing assignments for the Microsoft software products that are deployed on your hypervisor clusters. Use these assignments to specify whether you want to license each software product at either the physical host layer or virtual layer.
-   **[Optimizing license consumption for Microsoft SQL Server databases and components](sql-comp-edi-discovery.md)**  
You can optimize the license consumption for your Microsoft SQL Server databases and components based on the component editions that are identified through ITOM Discovery.
-   **[Importing Microsoft entitlements from a Microsoft License Statement \(MLS\)](importing-mls-entitlements.md)**  
You can import entitlements from an MLS to automatically define the license details and license agreements that are matched to your Microsoft software models.
-   **[Windows and SQL Server Infrastructure report](../reference/windows-sql-server-infrastructure-report.md)**  
You can use the Windows and SQL Server Infrastructure report to gain visibility into the infrastructure details for all physical hosts and virtual machines \(VMs\) that are running Microsoft Windows Server or Microsoft SQL Server across your on-premise and public cloud environments, such as AWS and Microsoft Azure.
-   **[Microsoft dashboards in Software Asset Management classic](../reference/dashboard-microsoft.md)**  
View installations, cost, and compliance for Microsoft software such as SQL Server in the Software Asset Management classic application. View subscription use, cost, and compliance for Microsoft 365.
-   **[Publisher overview for Microsoft in the Software Asset Workspace](../reference/publisher-overview-microsoft.md)**  
View license usage information related to Microsoft in the publisher overview for Microsoft in the Software Asset Workspace.
-   **[Supported Microsoft license types](../reference/supported-microsoft-license-types.md)**  
The Software Asset Management publisher pack for Microsoft adds license metrics that are specific to Microsoft.

**Parent Topic:**[Supported software publisher licenses](sam-publisher-packs.md)

**Related topics**  


[Software license maintenance](software-license-maintenance.md)

[License metrics for Microsoft products](../reference/mapping-ms-license-metrics.md)

[Microsoft Per Core licensing rules](microsoft-sw-license-metrics.md)

[Microsoft Per Core \(with CAL\) licensing rules](microsoft-percore-withcal.md)

[Microsoft 365 integration](microsoft-o365.md)

