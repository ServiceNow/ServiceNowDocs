---
title: Query a remote table using ERP Data Hub
description: Query ERP \(Enterprise Resource Planning\) remote tables from a system of record directly from the All menu using ERP Data Hub.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using ERP remote tables in ERP Data Hub, Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Query a remote table using ERP Data Hub

Query ERP \(Enterprise Resource Planning\) remote tables from a system of record directly from the **All** menu using ERP Data Hub.

## Before you begin

Role required: sn\_erp\_integration.erp\_user

## About this task

You can query the system of record to create an ERP model for your ERP processes. For more information, see [Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md).

**Note:** ERP Data Hub doesn't replicate data into the ServiceNow AI Platform. It mirrors data that lives in the ERP system of record, and remains protected there.

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub** &gt; **ERP Data Hub Home**.

2.  Open the Remote tables page by selecting the remote tables icon \(![remote tables navigation icon](../image/erpc-remote-table-icon.png)\) in the side panel.

3.  Select the remote table from the navigation menu, such as **SAP Material Stock**.

4.  Query the remote table using Glide for SAP.

    For example, you can select and hold \(or right-click\) on a column, such as **Storage location**, and select **Show Matching** records.

    The SAP data is accessible for you to work with using standard ServiceNow AI Platform searching, sorting, and filtering, such as the condition builder. For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    ![View and query data from the system of record inside a ServiceNow AI Platform table](../image/erpi-sap-data-in-glide-record.png "View data from the system of record in a ServiceNow table")


**Parent Topic:**[Using ERP remote tables in ERP Data Hub](../concept/erp-canvas-work-with-remote-tables.md)

