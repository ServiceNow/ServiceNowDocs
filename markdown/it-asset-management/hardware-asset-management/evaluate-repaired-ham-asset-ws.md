---
title: Evaluate the repaired asset in the Hardware Asset Workspace
description: Evaluate the repaired asset and confirm if the asset is redeployable or should be disposed of. The Repair flow completes after the repaired asset is evaluated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/evaluate-repaired-ham-asset-ws.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Fulfill repair orders manually, Repair order fulfillment in the Hardware Asset Workspace, Manage asset repair in stockrooms, Use, Hardware Asset Management, IT Asset Management]
---

# Evaluate the repaired asset in the Hardware Asset Workspace

Evaluate the repaired asset and confirm if the asset is redeployable or should be disposed of. The Repair flow completes after the repaired asset is evaluated.

## Before you begin

Role required: asset

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **Repair orders** tab.

3.  Select the repair order for which you want to evaluate the repaired asset.

4.  Select the **Repair order lines** tab.

5.  Select a repair order line that's in the Evaluate stage and Open state.

6.  Select the **Repair asset tasks** tab.

7.  Select the **Evaluate asset** task that's in the Open state.

8.  Indicate that you have started working on the Evaluate asset task by selecting **Start Work**.

    The **Start Work** option changes to **Start Timer** and **Record Time** automatically.

9.  Record the time worked on the task.

    You can either use the timer or record the time manually. For more details, see [Record time worked on asset repair tasks in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/record-repair-time-ham-ws.md).

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

**Parent Topic:**[Fulfill repair orders in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/fulfill-ham-repair-orders-ws.md)

**Related topics**  


[View open repair orders for your stockroom in the Hardware Asset Workspace]()

[Troubleshoot assets requested for repair in the Hardware Asset Workspace]()

[Complete the repair asset task in the Hardware Asset Workspace]()

[Bulk close asset repair tasks in the Hardware Asset Workspace]()

[Cancel a repair order in the Hardware Asset Workspace]()

[Cancel a repair order line in the Hardware Asset Workspace]()

