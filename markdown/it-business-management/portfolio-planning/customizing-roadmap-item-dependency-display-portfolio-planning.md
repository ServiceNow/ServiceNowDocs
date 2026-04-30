---
title: Customizing roadmap item dependency display in Portfolio Planning Workspace
description: Improve the efficiency of identifying the relationships between your planning items by choosing how the dependencies are displayed on the roadmap view.
locale: en-US
release: xanadu
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace, roadmap]
breadcrumb: [Personalize roadmap view in Portfolio Planning Workspace, Plan roadmaps, Portfolio Planning, Strategic Portfolio Management]
---

# Customizing roadmap item dependency display in Portfolio Planning Workspace

Improve the efficiency of identifying the relationships between your planning items by choosing how the dependencies are displayed on the roadmap view.

The Personalize \(![Personalize icon.](../../alignment-planner-workspace/images/personalize-icon.png)\) side panel on the roadmap provides different toggles to personalize the display of dependencies on your roadmap.

-   For portfolio plan roadmaps, these toggles are always available.
-   For free-form roadmaps, these toggles are available only if the roadmap's source table is the Planning Item table \[sn\_align\_core\_planning\_item\] or one of its extensions.

![Dependencies toggle on the roadmap.](../../alignment-planner-workspace/images/dependencies-toggle.png)

<table id="table_cgz_jd3_2tb"><thead><tr><th>

Dependencies Toggle

</th><th>

Roadmap view

</th></tr></thead><tbody><tr><td>

**View dependencies**

 Indicates dependencies in the form of circles on either side of the planning item bars.

 These circles either contain a number inside them \(![Dependency circle.](../../alignment-planner-workspace/images/icon-dependency-circle.png)\), indicating the number of dependencies that item shares, or is colored red \(![Dependency error icon.](../../alignment-planner-workspace/images/icon-dependency-error.png)\) indicating a conflicting dependency.

 **Note:** This toggle must be enabled to use the other two toggles in the Dependencies section.

</td><td>

![Dependency circles on the roadmap.](../../alignment-planner-workspace/images/dependency-circles.png "Dependency circles on the roadmap")

</td></tr><tr><td>

**Dependency lines**

 Indicates dependencies using lines between the planning items.

 These lines are shown only if:

-   Both planning items of the dependency are within the same roadmap
-   Dependency is of the **Depends on** type

</td><td>

![Dependency lines between the planning items.](../../alignment-planner-workspace/images/dependency-lines.png "Dependency lines between the planning items")

</td></tr><tr><td>

**Only items with dependencies**

 Filters the roadmap to show only those planning items that have that have at-least one **Depends on** type of relationship.

 The items shown here can depend on items on or out of the current roadmap.

</td><td>

![Roadmap showing only items with dependencies.](../../alignment-planner-workspace/images/only-dependencies.png "Roadmap showing only items with dependencies")

</td></tr></tbody>
</table>**Parent Topic:**[Personalize roadmap view in Portfolio Planning Workspace](../task/personalize-roadmap-view-portfolio-planning.md)

