---
title: View and edit ERP remote table details with ERP Canvas
description: View and edit details for ERP \(Enterprise Resource Planning\) remote tables in ERP Canvas, such as their attachment settings and short descriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erpi-find-tables.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using ERP remote tables in ERP Canvas, Using ERP models, extraction tables, and remote tables, ERP Canvas, Building low-code applications, Developing your application, Building applications]
---

# View and edit ERP remote table details with ERP Canvas

View and edit details for ERP \(Enterprise Resource Planning\) remote tables in ERP Canvas, such as their attachment settings and short descriptions.

## Before you begin

Role required:

-   To modify remote tables: sn\_erp\_integration.erp\_admin
-   To read remote tables: sn\_erp\_integration.erp\_user

## About this task

To ensure data integrity, you can't create new remote tables in ERP Canvas, but you can clone existing ERP models and extend standard ERP remote tables to customize them. For more information, see [Clone an ERP model in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-clone-data-model.md).

For information on adding and removing fields to and from remote tables, see [Customize fields for an ERP remote table in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-build-remote-table.md).

ERP remote tables have a limit of 1,000 records. If you need a larger amount of data, use an ERP extraction table. For more information, see [Extracting and transforming data in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-extraction-tables.md).

## Procedure

1.  Navigate to **All** &gt; **ERP Canvas** &gt; **ERP Canvas Home**.

2.  Open the Remote tables page by selecting the remote tables icon \(\[Omitted image "erpc-remote-table-icon.png"\] Alt text: remote tables navigation icon\) in the side panel.

    \[Omitted image "erpc-remote-tables-list.png"\] Alt text: Remote tables list

3.  View the details for a remote table by selecting the remote table **Name**.

4.  Refresh the data stored in the remote table attachment outside of the scheduled cycle by selecting the **Refresh attachment data** button.

    The remote table attachment is the cached response from the ERP system. If the remote table **Attachment setting** field is set to **Use attachment**, ERP Canvas doesn't call the ERP system when someone fetches data from the remote table.

5.  Edit the remote table details as needed.

    For a description of the field values, see [ERP Canvas remote table form field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-remote-table-descriptions.md).

6.  View the fields in the remote table by selecting the **Remote table fields** tab.

7.  View the ERP remote table as a list on the ServiceNow AI Platform by selecting the **Open remote table list** button.

8.  Select **Save**.


**Parent Topic:**[Using ERP remote tables in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-work-with-remote-tables.md)

