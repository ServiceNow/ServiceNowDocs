---
title: Export Zero Copy Connector for ERP transaction data
description: Export Zero Copy Connector for ERP transaction information such as failures and usage. Filter the data as needed and then export to Excel, CSV, JSON, or PDF format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/monitor-export-telemetry-data.html
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, export, transaction, information, failure, excel, csv, json, pdf]
breadcrumb: [Monitor transactions, Extracting and transforming data, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Export Zero Copy Connector for ERP transaction data

Export Zero Copy Connector for ERP transaction information such as failures and usage. Filter the data as needed and then export to Excel, CSV, JSON, or PDF format.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP monitor page by selecting the monitor icon \[Omitted image "erp-monitor-icon-sidebar.png"\] in the side panel.

3.  Select the **Asynchronous transactions** or **Synchronous transactions** tab.

4.  Point to a column heading, select the filter icon \[Omitted image "ellipsis-vertical-fill-24.svg"\] Alt text:, specify filter options, and select **Apply**.

    For example, filter the **Status** column to only show errors. You can apply filters to multiple columns.

    \[Omitted image "erp-export-transaction-data1.png"\] Alt text: Status column filter with error selected.

5.  Select **Export**.

6.  Specify a **File Type**: Excel, CSV, JSON, or PDF.

7.  Select a **Delivery Type**: Download or Email.

8.  Select **Export**.


**Parent Topic:**[Monitor Zero Copy Connector for ERP transactions and logged errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/monitor-erp-data-hub-logged-extraction-and-remote-lookup-transactions.md)

