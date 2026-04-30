---
title: Bulk close asset repair tasks in the Enterprise Asset Workspace
description: Complete and close multiple repair tasks at one go to process a repair order with multiple repair order lines.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Fulfill repair orders in the Enterprise Asset Workspace, Manage repair of defective assets in your stockroom in the Enterprise Asset Workspace, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Bulk close asset repair tasks in the Enterprise Asset Workspace

Complete and close multiple repair tasks at one go to process a repair order with multiple repair order lines.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_technician

## About this task

You can bulk close only similar asset repair tasks that are in the Open state. However, you can't bulk close similar repair tasks for which the task result isn't the same. For example, you can't bulk close two Troubleshoot assets tasks, when one task has a repairable asset and the other has an unrepairable asset.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Inventory**.

2.  Select the **Repair orders** tab.

3.  Select a repair order with multiple open repair order lines for which you want to complete the asset repair tasks.

4.  Select the **Repair order lines** tab.

5.  Select the repair order line that you want to complete.

6.  Select the repair task that you want to close.

7.  On the Details form, select the task result.

    -   If you’re completing a Troubleshoot asset task, then select any of the following results in the **Troubleshoot result** field:
        -   **Repairable**
        -   **Unrepairable**
        -   **Redeployable**
    -   If you’re completing a Repair asset task, then select any of the following results in the **Repair result** field:
        -   **Repaired**
        -   **Unrepairable**
        -   **Redeployable**
    -   If you’re completing an Evaluate asset task, then select any of the following results in the **Evaluation result** field:
        -   **Redeployable**
        -   **To be disposed**
8.  Enter notes related to the task in the **Work notes** field.

9.  Select **Save**.

10. Select **Bulk Close**.

    The **Select Assets** dialog box with similar repair tasks is displayed.

11. Select the tasks that you want to close and select **Close Task**.


## Result

All the selected repair tasks are closed with the same task result and Work notes.

**Parent Topic:**[Fulfill repair orders in the Enterprise Asset Workspace](../concept/fulfill-eam-repair-orders-in-ws.md)

**Related topics**  


[View open repair orders for your stockroom in the Enterprise Asset Workspace](view-open-repair-orders-stockroom-eam.md)

[Troubleshoot assets requested for repair in the Enterprise Asset Workspace](troubleshoot-eam-assets-for-repair.md)

[Complete the repair asset task in the Enterprise Asset Workspace](repair-eam-assets-ws.md)

[Evaluate the repaired asset in the Enterprise Asset Workspace](evaluate-repaired-eam-asset-ws.md)

[Cancel a repair order in the Enterprise Asset Workspace](cancel-repair-orders-eam-ws.md)

[Cancel a repair order line in the Enterprise Asset Workspace](cancel-repair-order-line-eam-ws.md)

