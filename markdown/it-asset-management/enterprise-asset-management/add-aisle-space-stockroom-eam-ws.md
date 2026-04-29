---
title: Add aisles and spaces to a stockroom in the Enterprise Asset Workspace
description: Add details of aisles and spaces in a stockroom to provide granular location details of an asset in that stockroom. The aisle and space details enable you to locate and pick an asset in the stockroom.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage enterprise asset picking, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Add aisles and spaces to a stockroom in the Enterprise Asset Workspace

Add details of aisles and spaces in a stockroom to provide granular location details of an asset in that stockroom. The aisle and space details enable you to locate and pick an asset in the stockroom.

## Before you begin

Role required: inventory\_user

## About this task

A space is associated with an aisle in the stockroom. You can add a space only after you have added a minimum of one aisle to the stockroom.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Inventory**.

2.  Select the **All stockrooms** tab.

3.  Select a stockroom.

4.  Select the **Aisle and spaces** tab.

    The list of existing aisles and spaces in that stockroom is displayed.

5.  Add aisles to the selected stockroom.

    1.  Select **Add aisle**.

        The **Add aisle** dialog box is displayed.

    2.  In the **Aisle** field, enter a unique identifier for the aisle.

        You can enter any string value in this field. For example, `aisle_0001`.

    3.  To add more aisles, select the Add icon ![](../../hardware-asset-management/image/add-aisle-icon.png) and enter a unique identifier for the aisle in the **Aisle** field.

    4.  Select **OK**.

    The aisle is added to the list in the Aisle and spaces tab.

6.  Add a space to an aisle in the stockroom.

    1.  Select **Add space**.

        The **Add space** dialog box is displayed.

    2.  In the **Aisle** field, select the aisle for which you want to add a space.

    3.  In the **Space** field, enter a unique identifier for the space.

        You can enter any string value in this field. For example, `space_0001`.

    4.  To add more spaces, select the Add icon ![](../../hardware-asset-management/image/add-aisle-icon.png) and enter a unique identifier for the space in the **Space** field.

    5.  Select **OK**.

    -   The space is added to the list in the Aisle and spaces tab.
    -   The display name of the space is automatically set based on the **Aisle** and **Space** fields. For example, the display name of the space whose aisle is aisle\_001 and space is space\_001 is **aisle\_001 - space\_001**.

**Parent Topic:**[Manage enterprise asset picking within your stockrooms](../concept/manage-asset-picking-stockroom-eam-ws.md)

**Related topics**  


[Enable the Asset pick task for your stockroom in the Enterprise Asset Workspace](enable-pick-task-for-stockroom-eam.md)

[View the open enterprise asset pick tasks for your stockroom](view-open-pick-tasks-eam.md)

