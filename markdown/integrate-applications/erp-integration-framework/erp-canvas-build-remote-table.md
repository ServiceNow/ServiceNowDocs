---
title: Customize fields for an ERP remote table in Zero Copy Connector for ERP
description: Add or remove columns in remote tables in Zero Copy Connector for ERP to create your ERP \(Enterprise Resource Planning\) model. For example, remove fields with sensitive information, such as birthdays.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, column, remote, table, model]
breadcrumb: [Using remote tables, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Customize fields for an ERP remote table in Zero Copy Connector for ERP

Add or remove columns in remote tables in Zero Copy Connector for ERP to create your ERP \(Enterprise Resource Planning\) model. For example, remove fields with sensitive information, such as birthdays.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## About this task

Zero Copy Connector for ERP scans the system of record for the ERP model to find all available fields that you can add to a remote table. You can view all available fields from the ERP system in the ERP model. Using the **Manage fields** modal to add available columns from the ERP system to a remote table automatically creates them in the remote table.

If you don't see the fields that you want to add to the remote table, you must first add them to the model. For more information, see [Choose output parameters for a model](erp-canvas-manage-outputs.md).

The connected model, which is defined on the remote table **Details** tab, controls the available fields on the remote table. If you change the model for a remote table, the available fields change as well.

**Note:** You can't edit field names in remote tables, but you can add a new label for a field.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the Remote tables page by selecting the remote tables icon ![](../image/erpc-remote-table-icon.png) in the side panel.

3.  Select a table to work with by selecting the **Name**.

4.  Manage the columns to build the remote table by selecting the **Manage fields** button.

    1.  In **Available fields**, find the field to add and select the check box \(if the list is long, use the search box to filter the list\).

    2.  In **Selected fields**, drag fields up and down to rearrange how they appear in the table.

    3.  After you're finished, select **OK**.

        The fields on the remote table are updated.

5.  Confirm that the fields appear correctly by selecting the **Remote table fields** tab.


**Parent Topic:**[Using ERP remote tables in Zero Copy Connector for ERP](../concept/erp-canvas-work-with-remote-tables.md)

