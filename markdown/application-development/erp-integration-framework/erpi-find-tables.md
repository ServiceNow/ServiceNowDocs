---
title: View and edit ERP remote table details with Zero Copy Connector for ERP
description: View and edit details for ERP \(Enterprise Resource Planning\) remote tables in Zero Copy Connector for ERP, such as their attachment settings and short descriptions.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using ERP remote tables in Zero Copy Connector for ERP, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# View and edit ERP remote table details with Zero Copy Connector for ERP

View and edit details for ERP \(Enterprise Resource Planning\) remote tables in Zero Copy Connector for ERP, such as their attachment settings and short descriptions.

## Before you begin

Role required:

-   To modify remote tables: sn\_erp\_integration.erp\_admin
-   To read remote tables: sn\_erp\_integration.erp\_user

## About this task

To ensure data integrity, you can't create new remote tables in Zero Copy Connector for ERP, but you can clone existing ERP models and extend standard ERP remote tables to customize them. For more information, see [Clone an ERP model in Zero Copy Connector for ERP](erp-canvas-clone-data-model.md).

For information on adding and removing fields to and from remote tables, see [Customize fields for an ERP remote table in Zero Copy Connector for ERP](erp-canvas-build-remote-table.md).

ERP remote tables have a limit of 1,000 records. If you need a larger amount of data, use an ERP extraction table. For more information, see [Extracting and transforming data in Zero Copy Connector for ERP](../concept/erp-canvas-extraction-tables.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the Remote tables page by selecting the remote tables icon \(![remote tables navigation icon](../image/erpc-remote-table-icon.png)\) in the side panel.

    ![Remote tables list](../image/erpc-remote-tables-list.png)

3.  View the details for a remote table by selecting the remote table **Name**.

4.  Refresh the data stored in the remote table attachment outside of the scheduled cycle by selecting the **Refresh attachment data** button.

    The remote table attachment is the cached response from the ERP system. If the remote table **Attachment setting** field is set to **Use attachment**, Zero Copy Connector for ERP doesn't call the ERP system when someone fetches data from the remote table.

5.  Edit the remote table details as needed.

    For a description of the field values, see [Zero Copy Connector for ERP remote table form field descriptions](../reference/erp-canvas-remote-table-descriptions.md).

6.  View the fields in the remote table by selecting the **Remote table fields** tab.

7.  View the ERP remote table as a list on the ServiceNow AI Platform by selecting the **Open remote table list** button.

8.  Select **Save**.


**Parent Topic:**[Using ERP remote tables in Zero Copy Connector for ERP](../concept/erp-canvas-work-with-remote-tables.md)

