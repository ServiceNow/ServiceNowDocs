---
title: Item dependency errors in Strategic Planning Workspace
description: Learn about the scenarios when the planning item dependencies on the portfolio plan roadmap or free-form roadmap in Strategic Planning and Portfolio Planning can be in an error state.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Item dependency errors in Strategic Planning Workspace

Learn about the scenarios when the planning item dependencies on the portfolio plan roadmap or free-form roadmap in Strategic Planning and Portfolio Planning can be in an error state.

A dependency between two planning items can be in an error state when a scheduling conflict exists between the items. In a linear \(Depends on\) dependency, the items are scheduled in a way that starting the work on one item requires completing the work on another item.

**Note:** Error states are displayed for only if the planning items have a **Depends on** type of relationship.

In the sample roadmap shown here, starting work on **Employee onboarding process improvement** is dependent on the completion of **Specific onboarding path for new hire**. This relation is considered a linear dependency. Here, **Employee onboarding process improvement** is scheduled to start before the end date of **Specific onboarding path for new hire**. This conflict is indicated on the roadmap with an error icon \(![Dependency error icon.](../images/icon-dependency-error.png)\), and is also mentioned in the Dependencies tab of the Item details side panel.

To resolve such errors, review the scope of the planning items and update the start or end dates to adjust their scheduling accordingly.

![planning item dependency conflicts.](../images/dependency-conflict.png)

**Parent Topic:**[Strategic Planning Workspace reference](alignment-planner-workspace-reference.md)

**Related topics**  


[Add dependencies for roadmap items in Strategic Planning Workspace](../../spw-roadmap/task/create-planning-item-dependencies-in-a-roadmap.md)

[Update roadmap item dependencies in Strategic Planning Workspace](../../spw-roadmap/task/manage-planning-item-dependencies-apw.md)

