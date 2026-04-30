---
title: Complete the repair asset task in the Enterprise Asset Workspace
description: Complete the repair of the asset and confirm if the asset is repaired, unrepairable, or redeployable.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Fulfill repair orders in the Enterprise Asset Workspace, Manage repair of defective assets in your stockroom in the Enterprise Asset Workspace, Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Complete the repair asset task in the Enterprise Asset Workspace

Complete the repair of the asset and confirm if the asset is repaired, unrepairable, or redeployable.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_technician

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Inventory**.

2.  Select the **Repair orders** tab.

3.  Select the repair order for which you want to complete the Repair asset task.

4.  Select the **Repair order lines** tab.

5.  Select the repair order line that's in the **Repair** stage.

6.  Select the **Repair asset tasks** tab.

7.  Select the **Repair asset** task that's in the Open state.

8.  Indicate that you have started working on the Repair asset task by selecting **Start Work**.

    The **Start Work** option changes to **Start Timer** and **Record Time** automatically.

9.  Record the time worked on the task.

    You can either use the timer or record the time manually. For more details, see [Record time worked on asset repair tasks in the Enterprise Asset Workspace](../concept/record-repair-time-eam-ws.md).

    An entry for the time you worked is created in the **Time Worked** tab of the Repair asset task.

10. Select the **Details** tab.

11. Select the repair result in the **Repair result** field.

    -   If the asset is repaired, select **Repaired**.
    -   If the asset couldn't be repaired, select **Unrepairable**.
    -   If the asset can be redeployed, select **Redeployable**.
12. In the **Failure code** field, select the code that corresponds to the reason for the asset failure.

    This field shows the failure code that you selected in the Troubleshoot task. However, you can update this field if the reason for the asset failure differs from what was identified in the Troubleshoot task. For more details on codes, see [Failure and resolution codes in Enterprise Asset Management](../concept/failure-resolution-codes-eam.md).

    **Note:** The Failure code field value that you selected is also displayed in the Evaluate Asset task and the repair order line.

13. In the **Resolution code** field, select the code that matches the solution that you applied to fix the asset failure.

    **Note:** The Resolution code field value that you selected is also displayed in the Evaluate Asset task and the repair order line.

14. Enter the issue identified with the asset during the repair process in the **Issue identified** field.

    This field is automatically populated with the value carried forward from the troubleshoot asset task if the issue is identified and a value is provided in the **Issue identified** field. Once the task is closed, this field can’t be modified.

    The value in the **Issue identified** field is carried forward to evaluate repaired asset task after the repair task is closed.

15. Enter notes related to the task in the **Work notes** field.

16. Select **Close task**.


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

[Evaluate the repaired asset in the Enterprise Asset Workspace](evaluate-repaired-eam-asset-ws.md).

**Parent Topic:**[Fulfill repair orders in the Enterprise Asset Workspace](../concept/fulfill-eam-repair-orders-in-ws.md)

**Related topics**  


[View open repair orders for your stockroom in the Enterprise Asset Workspace](view-open-repair-orders-stockroom-eam.md)

[Troubleshoot assets requested for repair in the Enterprise Asset Workspace](troubleshoot-eam-assets-for-repair.md)

[Evaluate the repaired asset in the Enterprise Asset Workspace](evaluate-repaired-eam-asset-ws.md)

[Bulk close asset repair tasks in the Enterprise Asset Workspace](bulk-close-repair-tasks-eam-ws.md)

[Cancel a repair order in the Enterprise Asset Workspace](cancel-repair-orders-eam-ws.md)

[Cancel a repair order line in the Enterprise Asset Workspace](cancel-repair-order-line-eam-ws.md)

