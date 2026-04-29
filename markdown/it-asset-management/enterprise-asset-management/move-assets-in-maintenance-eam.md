---
title: Move enterprise assets to maintenance state
description: Move assets of a break fix or planned maintenance work order task to the In maintenance state to indicate that the assets are under maintenance.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a work order for an enterprise asset, Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Move enterprise assets to maintenance state

Move assets of a break fix or planned maintenance work order task to the In maintenance state to indicate that the assets are under maintenance.

## Before you begin

The break fix or planned maintenance work order task must be in the Work in progress state before you can move assets to the In maintenance state.

Only assets in the following states and substates can be moved to the In maintenance state:

-   In use
-   In use and Pending repair
-   In use and In repair
-   In use and Is shutdown

Role required: sn\_eam.asset\_technician

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Work management**.

2.  Select the **Work order tasks** tab.

3.  Select the work order task of the Break Fix or Planned Maintenance work type that has the assets that you want to move to maintenance.

4.  Select **Start Work**.

5.  Select the **Affected assets** tab.

6.  Select the assets that you want to mark as in maintenance, and then select **Move to maintenance**.

7.  In the Confirm asset state change dialog box, select **Confirm**.


## Result

The State of the assets changes to In maintenance.

