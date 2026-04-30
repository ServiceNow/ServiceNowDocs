---
title: Using ERP remote tables in ERP Data Hub
description: ERP \(Enterprise Resource Planning\) remote tables in ERP Data Hub enable you to view and query data from the ERP system of record on the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Using ERP remote tables in ERP Data Hub

ERP \(Enterprise Resource Planning\) remote tables in ERP Data Hub enable you to view and query data from the ERP system of record on the ServiceNow AI Platform.

**Note:** ERP Data Hub doesn't replicate data into the ServiceNow AI Platform. It mirrors data that lives in the ERP system of record, and remains protected there.

## Remote tables are linked to ERP models

Each ERP remote table is connected to one ERP model, which links the remote table to the ERP system and other related values. When you build a remote table, you can add any of the fields that ERP Data Hub finds when scanning the ERP system of record, which is connected through the ERP model. Scanning for and adding fields ensures that all necessary fields are available, such as when using the table as a data source when building an app.

The connected ERP model, which is defined on the remote table **Details** tab, controls the available fields on the remote table. If you change the ERP model for a remote table, the available fields change as well.

## Limitations of remote tables

To ensure data integrity, you can't create new remote tables in ERP Data Hub, but you can clone existing ERP models and extend standard ERP remote tables to customize them. For more information, see [Clone an ERP model in ERP Data Hub](../task/erp-canvas-clone-data-model.md).

ERP remote tables have a limit of 1,000 records. If you need a larger amount of data, use an ERP extraction table. For more information, see [Extracting and transforming data in ERP Data Hub](erp-canvas-extraction-tables.md).

-   **[View and edit ERP remote table details with ERP Data Hub](../task/erpi-find-tables.md)**  
View and edit details for ERP \(Enterprise Resource Planning\) remote tables in ERP Data Hub, such as their attachment settings and short descriptions.
-   **[Customize fields for an ERP remote table in ERP Data Hub](../task/erp-canvas-build-remote-table.md)**  
Add or remove columns in remote tables in ERP Data Hub to create your ERP \(Enterprise Resource Planning\) model. For example, remove fields with sensitive information, such as birthdays.
-   **[Query a remote table using ERP Data Hub](../task/erp-canvas-query-remote-table.md)**  
Query ERP \(Enterprise Resource Planning\) remote tables from a system of record directly from the **All** menu using ERP Data Hub.

**Parent Topic:**[Using ERP models, extraction tables, and remote tables](work-with-erp-systems-connections-and-remote-tables.md)

