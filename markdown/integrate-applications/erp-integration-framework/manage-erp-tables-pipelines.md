---
title: Managing ERP development pipelines in Zero Copy Connector for ERP
description: Move your ERP \(Enterprise Resource Planning\) systems, ERP models, tables, operations, and flows from a development instance to a production environment when they're ready.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, prod, sub-prod, non-prod, development, move, update, update set]
breadcrumb: [Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Managing ERP development pipelines in Zero Copy Connector for ERP

Move your ERP \(Enterprise Resource Planning\) systems, ERP models, tables, operations, and flows from a development instance to a production environment when they're ready.

Changes that you could promote from a development instance to a production instance include adding:

-   Fields to tables
-   Tables or BAPIs \(Business Application Programming Interface\) to ERP models
-   Table joins and fields to link tables
-   Create, read, and update operations
-   Flows built with the **Use ERP Data** action to query and update the system of record

**Note:** You should do your development on a non-production instance. If you make changes on a production instance, then promote changes from a non-production instance to the production instance, changes previously made on the production instance are overwritten.

There are several ways to move changes to your production instance on the ServiceNow AI Platform:

1.  Use System Update Sets to transfer changes from a development instance to a non-production and then production instance. For more information, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=zurich&pubname=zurich-application-development&ft:locale=en-US).
2.  Add the changes to the ServiceNow Store and use the **Share with others** option to install the updates on the production instance. For more information, see [Publish an application to an Update Set](https://www.servicenow.com/docs/access?context=t_PublishApplicationsToAnUpdateSet&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

For more information on ways to publish your ERP updates, see [Application sharing](https://www.servicenow.com/docs/access?context=c_SharingApplications&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

**Parent Topic:**[Using Zero Copy Connector for ERP](work-with-erp-systems-connections-and-remote-tables.md)

