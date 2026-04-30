---
title: Modify Script Includes for Prioritization page in Strategic Planning
description: Modify the Script Includes for List and Hierarchy views of the Prioritization page to change the columns to be highlighted in these views in the workspace.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Customizing highlighted fields, Prioritization display settings in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Modify Script Includes for Prioritization page in Strategic Planning

Modify the Script Includes for List and Hierarchy views of the Prioritization page to change the columns to be highlighted in these views in the workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  From the list, select one of the following:

    -   For List view, select APWBacklogConfigImpl
    -   For Hierarchy view, select APWGanttConfigImpl
3.  Update the column name in the **Script** field of the Script Include.

    In the **getColumnsForHighlightedValues** function, update the return value to the desired column.

    For example, if you want to highlight the Priority column, update the return value to `("planning_state", "state", "priority")`.

4.  Select **Update**.


## What to do next

[Create new highlighted values for Prioritization columns in Strategic Planning](customize-highlighted-fields-prioritzation-page-strategic-planning-workspace.md)

**Parent Topic:**[Customizing highlighted fields on Prioritization page of Strategic Planning Workspace](../concept/customizing-highlighted-fields-prioritization-page-strategic-planning.md)

