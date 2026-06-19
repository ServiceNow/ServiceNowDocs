---
title: Managing ERP development pipelines in Zero Copy Connector for ERP
description: Move your ERP \(Enterprise Resource Planning\) systems, ERP models, tables, operations, and flows from a development instance to a production environment when they're ready.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/manage-erp-tables-pipelines.html
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

1.  Use System Update Sets to transfer changes from a development instance to a non-production and then production instance. For more information, see .
2.  Add the changes to the ServiceNow Store and use the **Share with others** option to install the updates on the production instance. For more information, see .

For more information on ways to publish your ERP updates, see .

**Parent Topic:**[Using Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/work-with-erp-systems-connections-and-remote-tables.md)

