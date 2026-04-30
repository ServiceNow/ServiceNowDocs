---
title: Troubleshoot assets requested for repair in the Hardware Asset Workspace
description: Complete the troubleshooting task to assess the issues with the defective asset. Based on your observations, you can confirm whether the asset can be repaired, redeployed, or should be disposed of.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Fulfill repair orders in the Hardware Asset Workspace, Manage repair of defective assets in your stockroom in the Hardware Asset Workspace, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Troubleshoot assets requested for repair in the Hardware Asset Workspace

Complete the troubleshooting task to assess the issues with the defective asset. Based on your observations, you can confirm whether the asset can be repaired, redeployed, or should be disposed of.

## Before you begin

Role required: asset

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **Repair orders** tab.

3.  Select a repair order that's in the Draft or In Progress stage.

4.  Select the **Repair order lines** tab.

5.  Select a repair order line that's in the Troubleshoot stage and Open state.

6.  Select the **Repair asset tasks** tab.

7.  Select the **Troubleshoot asset** task that's in the Open state.

8.  Indicate that you have started working on the Troubleshoot task by selecting **Start Work**.

    The **Start Work** option changes to **Start Timer** and **Record Time** automatically.

9.  Record the time worked on the task.

    You can either use the timer or record the time manually. For more details, see [Record time worked on asset repair tasks in the Hardware Asset Workspace](../concept/record-repair-time-ham-ws.md).

    An entry for the time you worked is created in the **Time Worked** tab of the Troubleshoot asset task.

10. Select the **Details** tab.

11. Select the troubleshooting result in the **Troubleshoot result** field.

    -   If the asset is repairable, select **Repairable**.
    -   If the asset is unrepairable, select **Unrepairable**.
    -   If the asset can be redeployed, select **Redeployable**.
12. Enter the issue identified with the asset during the repair process in the **Issue identified** field.

    Once the task is closed, this field can't be modified.

    The value in the **Issue identified** field is carried forward to the repair asset task after the troubleshooting task is closed.

13. Enter notes related to the task in the **Work notes** field.

14. Select **Close task**.


## Result

-   If you had set the Troubleshooting result to **Unrepairable**, the following changes happen on closure of the task:
    1.  The repair order and the repair order line are in the Completed stage.
    2.  The state of the asset changes to In stock and substate changes to Pending disposal.
-   If you had set the Troubleshooting result to **Redeployable**, the following changes happen on closure of the task:
    1.  The repair order and the repair order line are in the Completed stage.
    2.  The state of the asset changes to In stock and the substate changes to Available.
-   If you had set the Troubleshooting result to **Repairable**, the following changes happen on closure of the task:
    1.  The stage of the repair order line changes to Repair.
    2.  The state of the asset changes to In stock and the substate changes to Pending repair.
    3.  Repair asset task is created.

## What to do next

[Complete the repair asset task in the Hardware Asset Workspace](repair-ham-assets-ws.md).

**Parent Topic:**[Fulfill repair orders in the Hardware Asset Workspace](../concept/fulfill-ham-repair-orders-ws.md)

**Related topics**  


[View open repair orders for your stockroom in the Hardware Asset Workspace](view-open-repair-orders-stockroom-ham.md)

[Complete the repair asset task in the Hardware Asset Workspace](repair-ham-assets-ws.md)

[Evaluate the repaired asset in the Hardware Asset Workspace](evaluate-repaired-ham-asset-ws.md)

[Bulk close asset repair tasks in the Hardware Asset Workspace](bulk-close-repair-tasks-ham-ws.md)

[Cancel a repair order in the Hardware Asset Workspace](cancel-repair-orders-ham-ws.md)

[Cancel a repair order line in the Hardware Asset Workspace](cancel-repair-order-line-ham-ws.md)

