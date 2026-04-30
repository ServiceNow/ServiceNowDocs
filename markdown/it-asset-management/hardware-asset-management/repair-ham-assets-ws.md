---
title: Complete the repair asset task in the Hardware Asset Workspace
description: Complete the repair of the defective asset and confirm if the asset is repaired, unrepairable, or redeployable.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Fulfill repair orders in the Hardware Asset Workspace, Manage repair of defective assets in your stockroom in the Hardware Asset Workspace, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Complete the repair asset task in the Hardware Asset Workspace

Complete the repair of the defective asset and confirm if the asset is repaired, unrepairable, or redeployable.

## Before you begin

Role required: asset

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **Repair orders** tab.

3.  Select the repair order for which you want to complete the Repair asset task.

4.  Select the **Repair order lines** tab.

5.  Select the repair order line that's in the Repair stage.

6.  Select the **Repair asset tasks** tab.

7.  Select the **Repair asset** task that's in the Open state.

8.  Indicate that you have started working on the Repair asset task by selecting **Start Work**.

    The **Start Work** option changes to **Start Timer** and **Record Time** automatically.

9.  Record the time worked on the task.

    You can either use the timer or record the time manually. For more details, see [Record time worked on asset repair tasks in the Hardware Asset Workspace](../concept/record-repair-time-ham-ws.md).

    An entry for the time you worked is created in the **Time Worked** tab of the Repair asset task.

10. Select the **Details** tab.

11. Select the repair result in the **Repair result** field.

    -   If the asset is repaired, select **Repaired**.
    -   If the asset couldn't be repaired, select **Unrepairable**.
    -   If the asset can be redeployed, select **Redeployable**.
12. Enter the issue identified with the asset during the repair process in the **Issue identified** field.

    This field is automatically populated with the value carried forward from the troubleshoot asset task if the issue is identified and a value is provided in the **Issue identified** field. Once the task is closed, this field can’t be modified.

    The value in the **Issue identified** field is carried forward to evaluate repaired asset task after the repair task is closed.

13. Enter notes related to the task in the **Work notes** field.

14. Select **Close task**.


## Result

-   If you had set the Repair result to **Unrepairable**, the following changes happen on closure of the task:
    1.  The repair order and the repair order line are in the Completed stage.
    2.  The state of the asset changes to In stock and the substate changes to Pending disposal.
-   If you had set the Repair result to **Redeployable**, the following changes happen on closure of the task:
    1.  The repair order and the repair order line are in the Completed stage.
    2.  The state of the asset changes to In stock and the substate changes to Available.
-   If you had set the Repair result to **Repairable**, the following changes happen on closure of the task:
    1.  The stage of the repair order line changes to Evaluate.
    2.  The state of the asset changes to In stock and the substate changes to Pending evaluation.
    3.  Evaluate asset task is created.

## What to do next

[Evaluate the repaired asset in the Hardware Asset Workspace](evaluate-repaired-ham-asset-ws.md).

**Parent Topic:**[Fulfill repair orders in the Hardware Asset Workspace](../concept/fulfill-ham-repair-orders-ws.md)

**Related topics**  


[View open repair orders for your stockroom in the Hardware Asset Workspace](view-open-repair-orders-stockroom-ham.md)

[Troubleshoot assets requested for repair in the Hardware Asset Workspace](troubleshoot-ham-assets-for-repair.md)

[Evaluate the repaired asset in the Hardware Asset Workspace](evaluate-repaired-ham-asset-ws.md)

[Bulk close asset repair tasks in the Hardware Asset Workspace](bulk-close-repair-tasks-ham-ws.md)

[Cancel a repair order in the Hardware Asset Workspace](cancel-repair-orders-ham-ws.md)

[Cancel a repair order line in the Hardware Asset Workspace](cancel-repair-order-line-ham-ws.md)

