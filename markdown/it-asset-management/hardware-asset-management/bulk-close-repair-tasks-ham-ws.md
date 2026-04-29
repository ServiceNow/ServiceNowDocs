---
title: Bulk close asset repair tasks in the Hardware Asset Workspace
description: Complete and close multiple repair tasks at one go to process a repair order with multiple repair order lines.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Fulfill repair orders in the Hardware Asset Workspace, Manage repair of defective assets in your stockroom in the Hardware Asset Workspace, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Bulk close asset repair tasks in the Hardware Asset Workspace

Complete and close multiple repair tasks at one go to process a repair order with multiple repair order lines.

## Before you begin

Role required: asset

## About this task

You can bulk close only similar asset repair tasks that are in the Open state. However, you can't bulk close similar repair tasks for which the task result isn't the same. For example, you can't bulk close two Troubleshoot assets tasks, when one task has a repairable asset and the other has an unrepairable asset.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

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

**Parent Topic:**[Fulfill repair orders in the Hardware Asset Workspace](../concept/fulfill-ham-repair-orders-ws.md)

**Related topics**  


[View open repair orders for your stockroom in the Hardware Asset Workspace](view-open-repair-orders-stockroom-ham.md)

[Troubleshoot assets requested for repair in the Hardware Asset Workspace](troubleshoot-ham-assets-for-repair.md)

[Complete the repair asset task in the Hardware Asset Workspace](repair-ham-assets-ws.md)

[Evaluate the repaired asset in the Hardware Asset Workspace](evaluate-repaired-ham-asset-ws.md)

[Cancel a repair order in the Hardware Asset Workspace](cancel-repair-orders-ham-ws.md)

[Cancel a repair order line in the Hardware Asset Workspace](cancel-repair-order-line-ham-ws.md)

