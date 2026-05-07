---
title: Add a new ERP extraction table in Zero Copy Connector for ERP
description: Create an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record every day, and save the data to a transformation \(staging\) table. The data is then available on the ServiceNow AI Platform, and you can add the extracted data to an ERP model or remote table.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, extraction, table, data, transform]
breadcrumb: [Extracting and transforming data, Retrieving data, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Add a new ERP extraction table in Zero Copy Connector for ERP

Create an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record every day, and save the data to a transformation \(staging\) table. The data is then available on the ServiceNow AI Platform, and you can add the extracted data to an ERP model or remote table.

## Before you begin

You must first configure the source table, target table, and table transform map before those tables can be added to an ERP extraction table. For more information on creating table transform maps, see [Create a transform map](../../../script/server-scripting/task/t_CreateATransformMap.md).

Role required: sn\_erp\_integration.erp\_admin

## About this task

Zero Copy Connector for ERP provides a number of standard extraction tables, which you can use as-is. If you must change a standard extraction table, copy the table and then update the copied version.

You can create multiple ERP extraction tables, and multiple extraction tables can use the same ERP model. For example, create separate extraction tables for sales contracts, sales inquires, and old sales orders.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP extraction tables page by selecting the extraction tables icon ![](../image/erpc-extraction-table-icon.png) in the side panel.

3.  Select the **New** button.

    ![New extraction table fields.](../image/erpc-new-extraction-table.png)

4.  On the form, fill in the fields.

    For a description of the field values, see [Zero Copy Connector for ERP extraction table field descriptions](../reference/erp-canvas-extraction-table-descriptions.md).

5.  Select **Save**.


**Parent Topic:**[Extracting and transforming data in Zero Copy Connector for ERP](../concept/erp-canvas-extraction-tables.md)

