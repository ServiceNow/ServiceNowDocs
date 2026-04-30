---
title: Start up enterprise assets after maintenance activities
description: Move assets of a startup work order task to the In use state to indicate that the assets are available for use after maintenance.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-02-19"
reading_time_minutes: 1
keywords: [Startup work type, Start up work order task]
breadcrumb: [Create a work order for an enterprise asset, Manage work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Start up enterprise assets after maintenance activities

Move assets of a startup work order task to the In use state to indicate that the assets are available for use after maintenance.

## Before you begin

**Important:** The Affected assets tab, Startup work type, and**Start up** option are available with Enterprise Asset Management version 10.0 and later.

The startup work order task must be in the Work in progress state before you can start up assets.

Role required: sn\_eam.asset\_technician

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Work management**.

2.  Select the **Work order tasks** tab.

3.  Select the work order task of the Startup work type that has the assets that you want to start up.

4.  Select **Start Work**.

5.  Select the **Affected assets** tab.

    The State and Substate of the assets are In use and Is shutdown.

6.  Select the assets that you want to start up, and then select **Start up**.

7.  In the Confirm asset state change dialog box, select **Confirm**.


## Result

The Substate of the asset is empty and the asset is back in use.

