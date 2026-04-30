---
title: Planning item reorder errors in Portfolio Planning
description: Review the scenarios when the reordering of items can fail in the List view of Prioritization in Portfolio Planning Workspace.
locale: en-US
release: xanadu
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Portfolio Planning, Strategic Portfolio Management]
---

# Planning item reorder errors in Portfolio Planning

Review the scenarios when the reordering of items can fail in the List view of Prioritization in Portfolio Planning Workspace.

To update the rank of the planning items in the work pipeline of your portfolio plan, you can reorder the items from the List view of the Prioritization page. While doing so, the reorder can fail due to an error in the ranking configuration. Following are the scenarios where reordering of planning items can fail:

-   **Scenario 1: Global ranking plugin is not active**

    Check if the Global Ranking Application plugin \(com.snc.sdlc.ranking\) is active in your ServiceNow instance. If not, contact your admin to activate it.

-   **Scenario 2: Planning item doesn't have a rank configuration**

    Check if all the planning items that you are reordering have a rank configuration. If not, contact your admin to update rank configuration for these planning item types.

-   **Scenario 3: Target row doesn't have a global rank**

    Check if the planning item before or after your target position to reorder has a global rank. If not, contact your system admin to generate a global rank for them.


**Parent Topic:**[Portfolio Planning reference](../concept/portfolio-planning-reference.md)

**Related topics**  


[Rank planning items in Portfolio Planning Workspace](../task/rank-and-prioritize-work-portfolio-planning-workspace.md)

