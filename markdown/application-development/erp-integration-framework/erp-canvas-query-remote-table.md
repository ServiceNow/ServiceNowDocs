---
title: Query a remote table using ERP Canvas
description: Query ERP \(Enterprise Resource Planning\) remote tables from a system of record directly from the All menu using ERP Canvas.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erp-canvas-query-remote-table.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using ERP remote tables in ERP Canvas, Using ERP models, extraction tables, and remote tables, ERP Canvas, Building low-code applications, Developing your application, Building applications]
---

# Query a remote table using ERP Canvas

Query ERP \(Enterprise Resource Planning\) remote tables from a system of record directly from the **All** menu using ERP Canvas.

## Before you begin

Role required: sn\_erp\_integration.erp\_user

## About this task

You can query the system of record to create an ERP model for your ERP processes. For more information, see [Building and managing ERP models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/work-with-erp-data-models.md).

**Note:** ERP Canvas doesn't replicate data into the ServiceNow AI Platform. It mirrors data that lives in the ERP system of record, and remains protected there.

## Procedure

1.  Navigate to **All** &gt; **ERP Canvas** &gt; **ERP Canvas Home**.

2.  Open the Remote tables page by selecting the remote tables icon \(\[Omitted image "erpc-remote-table-icon.png"\] Alt text: remote tables navigation icon\) in the side panel.

3.  Select the remote table from the navigation menu, such as **SAP Country**.

4.  Select **Open remote table list**.

5.  Query the remote table using Glide for SAP.

    For example, you can select and hold \(or right-click\) on a column, such as **Storage location**, and select **Show Matching** records.

    The SAP data is accessible for you to work with using standard ServiceNow AI Platform searching, sorting, and filtering, such as the condition builder. For more information, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/c_ConditionBuilder.md).

    \[Omitted image "erpi-sap-data-in-glide-record.png"\] Alt text: View and query data from the system of record inside a ServiceNow AI Platform table


**Parent Topic:**[Using ERP remote tables in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-work-with-remote-tables.md)

