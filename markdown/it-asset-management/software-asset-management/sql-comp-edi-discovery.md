---
title: Optimizing license consumption for Microsoft SQL Server databases and components
description: You can optimize the license consumption for your Microsoft SQL Server databases and components based on the component editions that are identified through ITOM Discovery.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Optimizing license consumption for Microsoft SQL Server databases and components

You can optimize the license consumption for your Microsoft SQL Server databases and components based on the component editions that are identified through ITOM Discovery.

**Note:** To identify the editions of your Microsoft SQL Server components through ITOM Discovery, you must request and install version 1.7.0 or later of the Discovery and Service Mapping Patterns application from the [ServiceNow Store](https://store.servicenow.com/).

**Note:** Both Microsoft SQL Server databases and components consume licenses against the associated Microsoft SQL Server edition. For Microsoft SQL Server components, the ServiceNow® Content Service team automatically associates each component with an appropriate Microsoft SQL Server edition based on the edition of the component. By optimizing the license consumption for your databases and components, you are optimizing licensing for Microsoft SQL Server and its component editions.

ITOM Discovery locates and identifies the Microsoft SQL Server databases and components across your deployment. When it locates and identifies your Microsoft SQL Server components, it also identifies the edition of each component. The Software Asset Management application then creates a software installation record for each of your components based on the identified component edition. The Software Asset Management application also create a software installation record for each of your Microsoft SQL Server databases. You can use these software installation records to reconcile your components and databases based on both the associated Microsoft SQL Server edition and the following Microsoft SQL Server licensing rules:

-   If your Microsoft SQL Server database and components are deployed on the same device, only one license must be consumed on the device.
-   If your Microsoft SQL Server database and components are deployed on different devices, separate licenses must be consumed on each device.

For more information on Microsoft SQL Server component edition discovery, see [MSSQL server discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/mssql-data-collected-pattern.md).

## Reconciling Microsoft SQL Server components based on the discovered component editions

You can reconcile Microsoft SQL Server components based on the discovered component editions so that licenses are optimally consumed against the appropriate Microsoft SQL Server editions.

When you create software models for your various Microsoft SQL Server editions, such as Microsoft SQL Server Standard or Enterprise edition, your Microsoft SQL Server components are automatically associated with an appropriate model based on mappings that are provided by the ServiceNow® Content Service team. Mappings between your Microsoft SQL Server software models and components are based on the edition of each component. The Content Service team provides these mappings through predefined discovery maps \(DMAPs\) in the software library, which is a centralized repository of software content that you can use to normalize your discovered data. Each DMAP associates a software model with relevant software content, such as software model suite relationships and software product lifecycles. For more information on the Content Service and software library, see [Software Asset Management Content Service](c_SAMContentService.md).

The Software Asset Management application considers software model suites during reconciliation so that you can accurately count your software rights and optimize your licenses, as child components are licensed against the parent software model and not the component itself. Reconciliation runs automatically as a scheduled job. However, you can also run reconciliation on-demand between scheduled jobs. For more information on software model suites, see [Software Asset Management software suites](software-suites.md). For instructions on how to run reconciliation manually through the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md). For instructions on how to run reconciliation manually through the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

**Parent Topic:**[Software Asset Management publisher pack for Microsoft](microsoft-publisher-pack.md)

