---
title: Using ERP remote tables in Zero Copy Connector for ERP
description: Remote tables in Zero Copy Connector for ERP \(Enterprise Resource Planning\) enable you to view and query data from the ERP system of record on the ServiceNow AI Platform.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, remote, table, remote table]
breadcrumb: [Retrieving data, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Using ERP remote tables in Zero Copy Connector for ERP

Remote tables in Zero Copy Connector for ERP \(Enterprise Resource Planning\) enable you to view and query data from the ERP system of record on the ServiceNow AI Platform.

**Note:** Zero Copy Connector for ERP doesn't replicate data into the ServiceNow AI Platform. It mirrors data that lives in the ERP system of record, and remains protected there.

For general information about remote tables in the ServiceNow AI Platform, see [Remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/remote-tables.md).

## Remote tables are linked to ERP models

Each ERP remote table is connected to one ERP model, which links the remote table to the ERP system and other related values. When building a remote table, you can add any of the fields that Zero Copy Connector for ERP finds when scanning the ERP system of record, which is connected through the ERP model. Scanning for and adding fields confirms that all necessary fields are available, such as when using the table as a data source when building an app.

The connected model, which is defined on the remote table **Details** tab, controls the available fields on the remote table. If you change the model for a remote table, the available fields change as well.

## Limitations of remote tables

To promote data integrity, you can't create new remote tables in Zero Copy Connector for ERP, but you can clone existing models and extend standard ERP remote tables to customize them. For more information, see [Clone an ERP model in Zero Copy Connector for ERP](../task/erp-canvas-clone-data-model.md).

ERP remote tables have a limit of 1,000 records. If you need a larger amount of data, use an ERP extraction table.

-   **[View and edit ERP remote table details with Zero Copy Connector for ERP](../task/erpi-find-tables.md)**  
View and edit details for ERP \(Enterprise Resource Planning\) remote tables in Zero Copy Connector for ERP, such as their attachment settings and short descriptions.
-   **[Customize fields for an ERP remote table in Zero Copy Connector for ERP](../task/erp-canvas-build-remote-table.md)**  
Add or remove columns in remote tables in Zero Copy Connector for ERP \(Enterprise Resource Planning\) to create your ERP model. For example, remove fields with sensitive information, such as birthdays.
-   **[Query a remote table using Zero Copy Connector for ERP](../task/erp-canvas-query-remote-table.md)**  
Query ERP \(Enterprise Resource Planning\) remote tables from a system of record directly from the **All** menu using Zero Copy Connector for ERP.

**Parent Topic:**[Retrieving data](erp-retrieving-data.md)

