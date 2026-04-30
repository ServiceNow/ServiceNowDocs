---
title: Select fields for an extraction table in Zero Copy Connector for ERP
description: Add or remove fields for an extraction table in Zero Copy Connector for ERP. For example, you may want to remove fields with sensitive information, such as birthdays.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Extracting and transforming data in Zero Copy Connector for ERP, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Select fields for an extraction table in Zero Copy Connector for ERP

Add or remove fields for an extraction table in Zero Copy Connector for ERP. For example, you may want to remove fields with sensitive information, such as birthdays.

## Before you begin

If you don't see the fields that you want to add to the extraction table, you must first add them to the model. For more information, see [Choose output parameters for an ERP model](erp-canvas-manage-outputs.md).

Role required:

-   To modify extraction tables: sn\_erp\_integration.erp\_admin
-   To read extraction tables: sn\_erp\_integration.erp\_user

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP extraction tables page by selecting the ERP extraction tables icon \(![ERP extraction tables navigation icon](../image/erpc-extraction-table-icon.png)\) in the side panel.

3.  Select an extraction table to work with by selecting the **Name**.

4.  Manage the columns to build the extraction table by selecting the arrow next to **Generate mapping** and then selecting **Select fields**.

    1.  In **Available columns**, find and select the field that you want to add to the extraction table using the search box.

    2.  Select the button to move the field from the **Available columns** list to the **Selected columns** list.

    3.  Drag to rearrange how fields appear in the table.

    4.  After you finish adding all the fields, select **OK** to save your changes.

        The fields on the extraction table are updated.

5.  Confirm that the fields appear correctly as columns on the extraction table by selecting the **Extraction table fields** tab.


**Parent Topic:**[Extracting and transforming data in Zero Copy Connector for ERP](../concept/erp-canvas-extraction-tables.md)

