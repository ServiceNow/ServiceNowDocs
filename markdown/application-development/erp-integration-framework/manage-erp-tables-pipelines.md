---
title: Managing ERP development pipelines in ERP Data Hub
description: Move your ERP \(Enterprise Resource Planning\) systems, ERP models, tables, operations, and flows from a development instance to a production environment when they're ready.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Managing ERP development pipelines in ERP Data Hub

Move your ERP \(Enterprise Resource Planning\) systems, ERP models, tables, operations, and flows from a development instance to a production environment when they're ready.

Changes that you could promote from a development instance to a production instance include adding:

-   Fields to tables
-   Tables or BAPIs \(Business Application Programming Interface\) to ERP models
-   Table joins and fields to link tables
-   Read and update operations
-   Flows built with the **Use ERP Data** action to query and update the system of record

**Note:** You should do your development on a non-production instance. If you make changes on a production instance, and then promote changes from a non-production instance to the production instance, any changes you previously made on the production instance are overwritten.

There are several ways to move changes to your production instance on the ServiceNow AI Platform:

1.  Use System Update Sets to transfer changes from a development instance to a non-production and then production instance. For more information, see [System update sets](../../system-update-sets/concept/system-update-sets.md).
2.  Add the changes to the ServiceNow Store and use the **Share with others** option to install the updates on the production instance. For more information, see [Publish an application to an Update Set](../../applications/task/t_PublishApplicationsToAnUpdateSet.md).

For more information on ways to publish your ERP updates, see [Application sharing](../../applications/concept/c_SharingApplications.md).

**Parent Topic:**[Using ERP models, extraction tables, and remote tables](work-with-erp-systems-connections-and-remote-tables.md)

