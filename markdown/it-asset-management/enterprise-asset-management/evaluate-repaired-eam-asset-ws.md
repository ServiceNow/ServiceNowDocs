---
title: Evaluate the repaired asset in the Enterprise Asset Workspace
description: Evaluate the repaired asset and confirm if the asset is redeployable or should be disposed of. The Repair flow completes after the repaired asset is evaluated.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Fulfill repair orders in the Enterprise Asset Workspace, Manage repair of defective assets in your stockroom in the Enterprise Asset Workspace, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Evaluate the repaired asset in the Enterprise Asset Workspace

Evaluate the repaired asset and confirm if the asset is redeployable or should be disposed of. The Repair flow completes after the repaired asset is evaluated.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_technician

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Inventory**.

2.  Select the **Repair orders** tab.

3.  Select the repair order for which you want to evaluate the repaired asset.

4.  Select the **Repair order lines** tab.

5.  Select a repair order line that's in the Evaluate stage and Open state.

6.  Select the **Repair asset tasks** tab.

7.  Select the **Evaluate asset** task that's in the Open state.

8.  Indicate that you have started working on the Evaluate asset task by selecting **Start Work**.

    The **Start Work** option changes to **Start Timer** and **Record Time** automatically.

9.  Record the time worked on the task.

    You can either use the timer or record the time manually. For more details, see [Record time worked on asset repair tasks in the Enterprise Asset Workspace](../concept/record-repair-time-eam-ws.md).

    An entry for the time you worked is created in the **Time Worked** tab of the Evaluate asset task.

10. Select the **Details** tab.

11. Select the evaluation result in the **Evaluation result** field.

    -   If the asset is repaired and redeployable, select **Redeployable**.
    -   If the asset can't be used and should be disposed of, select **To be disposed**.
12. Enter the issue identified with the asset during the repair process in the **Issue identified** field.

    This field is automatically populated with the value carried forward from the repair asset task if the issue is identified and a value is provided in the **Issue identified** field. Once the task is closed, this field can’t be modified.

13. Enter notes related to the task in the **Work notes** field.

14. Select **Close task**.


## Result

-   If you had set the Evaluation result to **To be disposed**, the following changes happen on closure of the task:
    1.  The repair order and the repair order line are in the Completed stage.
    2.  The state of the asset changes to In stock and the substate changes to Pending disposal.
-   If you had set the Evaluation result to **Redeployable**, the following changes happen on closure of the task:
    1.  The repair order and the repair order line are in the Completed stage.
    2.  The state of the asset changes to In stock and the substate changes to Available.

**Parent Topic:**[Fulfill repair orders in the Enterprise Asset Workspace](../concept/fulfill-eam-repair-orders-in-ws.md)

**Related topics**  


[View open repair orders for your stockroom in the Enterprise Asset Workspace](view-open-repair-orders-stockroom-eam.md)

[Troubleshoot assets requested for repair in the Enterprise Asset Workspace](troubleshoot-eam-assets-for-repair.md)

[Complete the repair asset task in the Enterprise Asset Workspace](repair-eam-assets-ws.md)

[Bulk close asset repair tasks in the Enterprise Asset Workspace](bulk-close-repair-tasks-eam-ws.md)

[Cancel a repair order in the Enterprise Asset Workspace](cancel-repair-orders-eam-ws.md)

[Cancel a repair order line in the Enterprise Asset Workspace](cancel-repair-order-line-eam-ws.md)

