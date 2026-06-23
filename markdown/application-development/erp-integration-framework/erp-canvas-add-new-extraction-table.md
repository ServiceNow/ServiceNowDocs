---
title: Add a new ERP extraction table in ERP Data Hub
description: Create an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record every day, and save the data to a transformation \(staging\) table. The data is then available on the ServiceNow AI Platform, and you can add the extracted data to an ERP model or remote table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/erp-integration-framework/erp-canvas-add-new-extraction-table.html
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Extracting and transforming data in ERP Data Hub, Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Add a new ERP extraction table in ERP Data Hub

Create an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record every day, and save the data to a transformation \(staging\) table. The data is then available on the ServiceNow AI Platform, and you can add the extracted data to an ERP model or remote table.

## Before you begin

You must first configure the source table, target table, and table transform map before those tables can be added to an ERP extraction table. For more information on creating table transform maps, see [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md).

Role required:

-   To modify extraction tables: sn\_erp\_integration.erp\_admin
-   To read extraction tables: sn\_erp\_integration.erp\_user

## About this task

ERP Data Hub provides a number of standard extraction tables, which you can use as-is. If you must change a standard extraction table, copy the table and then update the copied version.

You can create multiple ERP extraction tables, and multiple extraction tables can use the same ERP model. For example, create separate extraction tables for sales contracts, sales inquires, and old sales orders.

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub** &gt; **ERP Data Hub Home**.

2.  Open the ERP extraction tables page by selecting the ERP extraction tables icon \(\[Omitted image "erpc-extraction-table-icon.png"\] Alt text: ERP extraction tables navigation icon\) in the side panel.

3.  Select the **New** button.

    \[Omitted image "erpc-new-extraction-table.png"\] Alt text: New extraction table fields.

4.  On the form, fill in the fields.

    For a description of the field values, see [ERP Data Hub extraction table field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-integration-framework/erp-canvas-extraction-table-descriptions.md).

5.  Select **Save**.


**Parent Topic:**[Extracting and transforming data in ERP Data Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-integration-framework/erp-canvas-extraction-tables.md)

