---
title: Shut down enterprise assets for maintenance activities
description: Move enterprise assets of a shutdown work order task to the shutdown state to indicate that the assets are unavailable for use during maintenance.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-02-19"
reading_time_minutes: 1
keywords: [Shut down enterprise assets, Shutdown work type, Shut down work order task]
breadcrumb: [Create a work order for an enterprise asset, Manage work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Shut down enterprise assets for maintenance activities

Move enterprise assets of a shutdown work order task to the shutdown state to indicate that the assets are unavailable for use during maintenance.

## Before you begin

**Important:** The Affected assets tab, Shutdown work type, and **Shutdown** option are available with Enterprise Asset Management version 10.0 and later.

The shutdown work order task must be in the Work in progress state before you can shut down assets. The assets must be in the In use or In maintenance state.

Role required: sn\_eam.asset\_technician

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Work management**.

2.  Select the **Work order tasks** tab.

3.  Select the work order task of the Shutdown work type that has the assets that you want to shut down.

4.  Select **Start Work**.

5.  Select the **Affected assets** tab.

6.  Select the assets that you want to shut down, and then select **Shutdown**.

7.  In the Confirm asset state change dialog box, select **Confirm**.


## Result

The substate of the assets that are shut down changes to Is shutdown.

