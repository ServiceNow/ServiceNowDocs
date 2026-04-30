---
title: Cancel a repair order line in the Hardware Asset Workspace
description: Cancel a repair order line that no longer needs to be fulfilled.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Fulfill repair orders in the Hardware Asset Workspace, Manage repair of defective assets in your stockroom in the Hardware Asset Workspace, Use, Hardware Asset Management, IT Asset Management]
---

# Cancel a repair order line in the Hardware Asset Workspace

Cancel a repair order line that no longer needs to be fulfilled.

## Before you begin

Role required: asset

## About this task

You can only cancel a repair order line that is not in the Completed stage.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **Repair orders** tab.

3.  Select a repair order that's in the Draft or In Progress stage.

4.  Select the **Repair order lines** tab.

5.  Select the repair order line that you want to cancel.

6.  Select **Cancel**.


## Result

-   The stage of the repair order line changes to Cancelled and the state changes to Closed Incomplete.
-   The state of the associated repair asset tasks that were open changes to Closed Incomplete.
-   The stage of the repair order changes to Cancelled only if there aren't any other repair order lines that are in the Troubleshoot, Repair, Evaluate, or Completed stage.

**Parent Topic:**[Fulfill repair orders in the Hardware Asset Workspace](../concept/fulfill-ham-repair-orders-ws.md)

**Related topics**  


[View open repair orders for your stockroom in the Hardware Asset Workspace](view-open-repair-orders-stockroom-ham.md)

[Troubleshoot assets requested for repair in the Hardware Asset Workspace](troubleshoot-ham-assets-for-repair.md)

[Complete the repair asset task in the Hardware Asset Workspace](repair-ham-assets-ws.md)

[Evaluate the repaired asset in the Hardware Asset Workspace](evaluate-repaired-ham-asset-ws.md)

[Bulk close asset repair tasks in the Hardware Asset Workspace](bulk-close-repair-tasks-ham-ws.md)

[Cancel a repair order in the Hardware Asset Workspace](cancel-repair-orders-ham-ws.md)

