---
title: Query a remote table using Zero Copy Connector for ERP
description: Query ERP \(Enterprise Resource Planning\) remote tables from a system of record directly from the All menu using Zero Copy Connector for ERP.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, query, remote, table, model, glide]
breadcrumb: [Using remote tables, Retrieving data, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Query a remote table using Zero Copy Connector for ERP

Query ERP \(Enterprise Resource Planning\) remote tables from a system of record directly from the **All** menu using Zero Copy Connector for ERP.

## Before you begin

Role required: sn\_erp\_integration.erp\_user

## About this task

You can query the system of record to create an ERP model for your ERP processes. For more information, see [Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md).

**Note:** Zero Copy Connector for ERP doesn't replicate data into the ServiceNow AI Platform. It mirrors data that lives in the ERP system of record, and remains protected there.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the Remote tables page by selecting the remote tables icon ![](../image/erpc-remote-table-icon.png) in the side panel.

3.  Select the remote table in the **Name** column, such as **SAP Country**.

4.  Select **Open remote table list**.

5.  Query the remote table using Glide for SAP.

    For example, you can select and hold \(or right-click\) on a column, such as **Storage location**, and select **Show Matching** records.

    The SAP data is accessible for you to work with using standard ServiceNow AI Platform searching, sorting, and filtering, such as the condition builder. For more information, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md).


**Parent Topic:**[Using ERP remote tables in Zero Copy Connector for ERP](../concept/erp-canvas-work-with-remote-tables.md)

