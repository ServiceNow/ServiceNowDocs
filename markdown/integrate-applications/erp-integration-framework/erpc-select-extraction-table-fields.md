---
title: Select fields for an extraction table in Zero Copy Connector for ERP
description: Add or remove fields for an extraction table in Zero Copy Connector for ERP\(Enterprise Resource Planning\). For example, you may want to remove fields with sensitive information, such as birthdays.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, extraction, table, field, add, remove, delete]
breadcrumb: [Extracting and transforming data, Retrieving data, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Select fields for an extraction table in Zero Copy Connector for ERP

Add or remove fields for an extraction table in Zero Copy Connector for ERP\(Enterprise Resource Planning\). For example, you may want to remove fields with sensitive information, such as birthdays.

## Before you begin

If you don't see the fields that you want to add to the extraction table, you must first add them to the model. For more information, see [Choose output parameters for a model](erp-canvas-manage-outputs.md).

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP extraction tables page by selecting the extraction tables icon ![](../image/erpc-extraction-table-icon.png) in the side panel.

3.  Select an extraction table to work with by selecting the **Name**.

4.  Manage the columns to build the extraction table by selecting the arrow next to **Generate mapping** and then selecting **Select fields**.

    1.  In **Available columns**, find the field to add and select the check box \(if the list is long, use the search box to filter the list\).

    2.  In **Selected columns**, drag fields up and down to rearrange how they appear in the table.

    3.  After you're finished, select **OK**.

        The fields on the extraction table are updated.

5.  Confirm that the fields appear correctly as columns on the extraction table by selecting the **Extraction table fields** tab.


**Parent Topic:**[Extracting and transforming data in Zero Copy Connector for ERP](../concept/erp-canvas-extraction-tables.md)

