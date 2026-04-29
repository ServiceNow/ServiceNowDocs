---
title: Planning item reorder errors in Strategic Planning Workspace
description: Review the scenarios when the reordering of items can fail in the List view of Prioritization in Strategic Planning Workspace.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Planning item reorder errors in Strategic Planning Workspace

Review the scenarios when the reordering of items can fail in the List view of Prioritization in Strategic Planning Workspace.

To update the rank of the planning items in the work pipeline of your portfolio plan, you can reorder the items from the List view of the Prioritization page. While doing so, the reorder can fail due to an error in the ranking configuration. Following are the scenarios where reordering of planning items can fail:

-   **Scenario 1: Global ranking plugin is not active**

    Check if the Global Ranking Application plugin \(com.snc.sdlc.ranking\) is active in your ServiceNow instance. If not, contact your admin to activate it.

-   **Scenario 2: Planning item doesn't have a rank configuration**

    Check if all the planning items that you are reordering have a rank configuration. If not, contact your admin to update rank configuration for these planning item types.

-   **Scenario 3: Target row doesn't have a global rank**

    Check if the planning item before or after your target position to reorder has a global rank. If not, contact your system admin to generate a global rank for them.


**Parent Topic:**[Strategic Planning Workspace reference](alignment-planner-workspace-reference.md)

**Related topics**  


[Rank planning items](../../spw-prioritization/task/rank-and-prioritize-backlog-alignment-planner-workspace.md)

