---
title: Create a checklist for an Enterprise Asset Management work order or work order task
description: Create a checklist of all items that you must complete for your work order or work order task.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a work order for an enterprise asset, Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Create a checklist for an Enterprise Asset Management work order or work order task

Create a checklist of all items that you must complete for your work order or work order task.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager or wm\_agent

## Procedure

1.  From the Enterprise Asset Workspace, open the Work management view.

2.  Open the record for either the work order or work order task that you want to create a checklist for.

    -   To open a work order record, select the **Work orders** tab. From the list of available work orders, select the work order that you want to create a checklist for.
    -   To open a work order task record, select the **Work order tasks** tab. From the list of available work order tasks, select the work order task that you want to create a checklist for.
3.  On the work order or work order task record, select the **Checklist items** tab.

4.  Use one of the following options to create a checklist.

    -   Create a checklist by adding individual checklist items:
        1.  Select **New**.
        2.  On the Create New Checklist Item form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Name of the checklist item.|
            |Order|Order in which you must complete the checklist item. For example, a value of `1` indicates that the given checklist item is the first item you must complete within your checklist.|
            |Checklist|Checklist that the checklist item is included in.|
            |Complete|Option that indicates if the checklist item has been completed.|

        3.  Select **Save**.
        4.  Repeat steps a to c for every checklist item that you want to add to your checklist.
    -   Create a checklist by applying a checklist template:
        1.  Select **Apply template**.

            The Apply Template dialog box opens.

        2.  In the dialog box, select the checklist template that you want to apply to your work order or work order task.
        3.  Select **OK**.

            The dialog box closes and you return to the **Checklist items** tab.

        4.  Select the Refresh List icon \(![Refresh list icon.](../image/refresh-list-icon.png)\) to populate the list of checklist items that were added based on the selected checklist template.

