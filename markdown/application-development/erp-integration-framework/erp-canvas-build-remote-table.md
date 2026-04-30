---
title: Customize fields for an ERP remote table in ERP Data Hub
description: Add or remove columns in remote tables in ERP Data Hub to create your ERP \(Enterprise Resource Planning\) model. For example, remove fields with sensitive information, such as birthdays.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using ERP remote tables in ERP Data Hub, Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Customize fields for an ERP remote table in ERP Data Hub

Add or remove columns in remote tables in ERP Data Hub to create your ERP \(Enterprise Resource Planning\) model. For example, remove fields with sensitive information, such as birthdays.

## Before you begin

Role required:

-   To modify remote tables: sn\_erp\_integration.erp\_admin
-   To read remote tables: sn\_erp\_integration.erp\_user

## About this task

ERP Data Hub scans the system of record for the ERP model to find all available fields that you can add to a remote table. You can view all available fields from the ERP system in the ERP model. Using the **Manage fields** modal to add available columns from the ERP system to a remote table automatically creates them in the remote table.

If you don't see the fields that you want to add to the remote table, you must first add them to the model. For more information, see [Choose output parameters for an ERP model](erp-canvas-manage-outputs.md).

The connected ERP model, which is defined on the remote table **Details** tab, controls the available fields on the remote table. If you change the ERP model for a remote table, the available fields change as well.

**Note:** You can't edit field names in remote tables, but you can add a new label for a field.

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub** &gt; **ERP Data Hub Home**.

2.  Open the Remote tables page by selecting the remote tables icon \(![remote tables navigation icon](../image/erpc-remote-table-icon.png)\) in the side panel.

3.  Select a table to work with by selecting the **Name**.

4.  Manage the columns to build the remote table by selecting the **Manage fields** button.

    1.  On the modal, find and select the field that you want to add to the remote table using the search box.

    2.  Select the button to move the field from the **Available fields** list to the **Selected fields** list.

    3.  Drag to rearrange how fields appear in the table.

    4.  After you finish adding all the fields, select **OK** to save your changes.

        The ServiceNow AI Platform updates the fields on the remote table with your changes.

    ![Manage fields to customize the remote table](../image/erpc-manage-fields-remote-tables.png "ERP Data Hub customizing the remote table")

5.  Confirm that the fields appear correctly as columns on the remote table by selecting the **Remote table fields** tab.


**Parent Topic:**[Using ERP remote tables in ERP Data Hub](../concept/erp-canvas-work-with-remote-tables.md)

