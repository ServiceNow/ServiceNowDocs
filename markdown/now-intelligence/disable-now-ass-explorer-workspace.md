---
title: Remove data visualization links to AI Data Explorer in a specific workspace
description: If you don't want data visualizations in a specific workspace to have an entry point for AI Data Explorer, add the workspace to the PAAI Canvas Workspace Configs table.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-08-18"
reading_time_minutes: 1
breadcrumb: [Configure, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Remove data visualization links to AI Data Explorer in a specific workspace

If you don't want data visualizations in a specific workspace to have an entry point for AI Data Explorer, add the workspace to the PAAI Canvas Workspace Configs table.

## Before you begin

Role required: now\_assist\_explorer\_admin or higher

## Procedure

1.  Navigate to **All** and search for paai\_canvas\_workspace\_config\_list.do.

2.  Select **New**.

3.  In the new PAAI Canvas Workspace Config record, select the workspace or experience from the **Experience** list.

    ![Expanded list for selecting an experience or workspace for the Experience field.](../image/nowass-select-restricted-workspace.png)

4.  Turn on **Disabled in workspace**.

    ![Disable in Workspace selector in PAAI Canvas Workspace Config record.](../image/nowass-disable-workspace.png)

5.  Select **Submit**.


**Parent Topic:**[Configure AI Data Explorer](configure-now-ass-explorer.md)

