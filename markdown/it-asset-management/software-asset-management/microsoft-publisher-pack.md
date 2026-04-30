---
title: Software Asset Management publisher pack for Microsoft
description: Use the Software Asset Management publisher pack for Microsoft to track your license compliance position using Microsoft licensing metrics.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Asset Management publisher pack for Microsoft

Use the Software Asset Management publisher pack for Microsoft to track your license compliance position using Microsoft licensing metrics.

**Note:** To use the publisher pack, activate the Software Asset Management Professional for Microsoft plugin \(com.snc.samp.microsoft\).

Microsoft offers a wide variety of products that span from database servers to subscription services. Each Microsoft product follows its own licensing model, which can make it hard to track your license compliance position. With the Software Asset Management publisher pack for Microsoft, you can accurately track your license compliance position for Microsoft products. Reconciliation identifies licenses that are out of compliance and provides a list of remediation options. For more information, see [Software reconciliation for compliance](c_SAMReconciliation.md).

To learn more about Microsoft licensing models, see [Microsoft licensing](https://www.microsoft.com/en-us/Licensing).

Set up ServiceNow Discovery to identify Microsoft installations on your network. For more information, see [Data collected by ITOM Visibility](https://www.servicenow.com/docs/access?context=data-collected-by-itom-visibility&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

The Software Asset Management publisher pack for Microsoft supports the following licensing models.

-   Per user
-   Per device
-   Per core
-   Per core \(with CAL\)
-   User CAL
-   Device CAL
-   Server \(per instance\)
-   Server \(per server\)
-   Per processor
-   User subscription
-   Software Assurance

For more information, see [Supported Microsoft license types](../reference/supported-microsoft-license-types.md).

If a PPN with P+SA license type doesn't have a version assigned, a software model with the exact version is automatically set on a new entitlement and while importing entitlements from a Microsoft License Statement \(MLS\). This automatic action correctly applies Microsoft assurance benefits to an entitlement. For details on the upgrade history of an entitlement, navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations** &gt; **Software entitlements** &gt; **Upgrade history**.

The **SAMP - Update generic PSA entitlements** fix script automatically updates the existing P+SA entitlements with version as anything, with the specific version, and applies the appropriate licensing terms.

-   **[Microsoft 365 integration](microsoft-o365.md)**  
Create an integration with Microsoft 365 to download subscription information that is compared with software installations for compliance.
-   **[Microsoft SQL Server licensing in container deployments](microsoft-licensing-software-containers.md)**  
The Software Asset Management publisher pack for Microsoft supports licensing rules for Microsoft SQL Server products that are deployed across both on-premise and cloud environments using Docker containers.
-   **[Manage licenses for Microsoft Visual Studio](../task/manage-visual-studio-licenses.md)**  
Manage your Visual Studio subscriptions with the Software Asset Management publisher pack for Microsoft. Verify license compliance and detect unlicensed installations. Reduce licensing costs by identifying subscriptions that are allocated but aren’t being used.
-   **[Cost-based licensing optimization for Microsoft](cost-based-microsoft-cluster-licensing.md)**  
The cost-based licensing optimization for Microsoft helps you determine the most optimal way to license your Microsoft software products across hybrid infrastructures. With this optimization, you can automatically balance license compliance with cost effectiveness to maximize cost savings.
-   **[Optimizing Microsoft SQL Server database and component license consumption](sql-comp-edi-discovery.md)**  
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

