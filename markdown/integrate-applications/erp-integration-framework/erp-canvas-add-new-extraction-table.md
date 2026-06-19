---
title: Add a new ERP extraction table in Zero Copy Connector for ERP
description: Create an ERP extraction table to capture large amounts of data from the system of record every day, and save the data to a transformation \(staging\) table. The data is then available on the ServiceNow AI Platform, and you can add the extracted data to an ERP model or remote table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/erp-canvas-add-new-extraction-table.html
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, extraction, table, data, transform]
breadcrumb: [Extracting and transforming data, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Add a new ERP extraction table in Zero Copy Connector for ERP

Create an ERP extraction table to capture large amounts of data from the system of record every day, and save the data to a transformation \(staging\) table. The data is then available on the ServiceNow AI Platform, and you can add the extracted data to an ERP model or remote table.

## Before you begin

You must first configure the source table, target table, and table transform map before those tables can be added to an ERP extraction table. For more information on creating table transform maps, see [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/system-import-sets/t_CreateATransformMap.md).

Role required: sn\_erp\_integration.erp\_admin

## About this task

Zero Copy Connector for ERP provides a number of standard extraction tables, which you can use as-is. If you must change a standard extraction table, copy the table and then update the copied version.

You can create multiple ERP extraction tables, and multiple extraction tables can use the same ERP model. For example, create separate extraction tables for sales contracts, sales inquires, and old sales orders.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP extraction tables page by selecting the extraction tables icon \[Omitted image "erpc-extraction-table-icon.png"\] Alt text: in the side panel.

3.  Select the **New** button.

    \[Omitted image "erpc-new-extraction-table.png"\] Alt text: New extraction table fields.

4.  On the form, fill in the fields.

    For a description of the field values, see [Zero Copy Connector for ERP extraction table field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-extraction-table-descriptions.md).

5.  Select **Save**.


**Parent Topic:**[Extracting and transforming data in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-extraction-tables.md)

