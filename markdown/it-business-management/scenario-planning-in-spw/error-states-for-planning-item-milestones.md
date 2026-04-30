---
title: Item milestone errors in Strategic Planning Workspace
description: Learn about the scenarios when the planning item milestones on the portfolio plan roadmap or free-form roadmap can be in an error state in Strategic Planning Workspace.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Item milestone errors in Strategic Planning Workspace

Learn about the scenarios when the planning item milestones on the portfolio plan roadmap or free-form roadmap can be in an error state in Strategic Planning Workspace.

An item milestone can fall out of the approved start or end dates of the item when you reschedule the existing planning item.

When you reschedule a planning item on the roadmap, the due dates of its milestones don’t change. So, if the due date of a milestone is falls outside the item’s date range, the indicator for that out-of-range milestone is hidden and moved to an error state. Indicators for milestones that are still within the item's date range are visible.![Milestone out of item's date range.](../images/milestone-out-of-range.gif)

The milestones that are out of sync with the item's schedule can be viewed from the Milestones tab on the side panel. From the side panel, you can edit and adjust the due date of the milestone to reflect the change of plans. See [Update roadmap item milestones in Strategic Planning Workspace](../../spw-roadmap/task/manage-planning-item-milestones.md).![Item milestone out of date range.](../images/milestone-out-of-range.gif)

**Note:** You can’t update a project milestone from the roadmap view. Updating project milestones may impact the associated cost and resource plans of the project. So, it’s recommended to update project milestones using Project Workspace in Project Portfolio Management \(PPM\).

**Parent Topic:**[Strategic Planning Workspace reference](../reference/alignment-planner-workspace-reference.md)

**Related topics**  


[Add dependencies for roadmap items in Strategic Planning Workspace](../../spw-roadmap/task/create-planning-item-dependencies-in-a-roadmap.md)

[Update roadmap item dependencies in Strategic Planning Workspace](../../spw-roadmap/task/manage-planning-item-dependencies-apw.md)

[Customizing the dependencies display on the roadmap in Strategic Planning Workspace](customizing-dependencies-display-on-roadmap.md)

