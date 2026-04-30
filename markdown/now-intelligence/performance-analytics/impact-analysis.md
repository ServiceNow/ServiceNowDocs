---
title: Dependency Assessment
description: Dependency Assessment enables you to view, analyze, and edit your performance analytics components including widgets, indicators, and breakdowns, from a single view. By viewing the hierarchy of components and the relationships between them, you can see immediately who is impacted by a change and what the effects of your changes are.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Dependency Assessment

Dependency Assessment enables you to view, analyze, and edit your performance analytics components including widgets, indicators, and breakdowns, from a single view. By viewing the hierarchy of components and the relationships between them, you can see immediately who is impacted by a change and what the effects of your changes are.

**Important:** Dependency Assessment does not support Platform Analytics artifacts. It analyzes information only for Core UI Performance Analytics widgets but not Platform Analytics data visualizations. Also, you can launch Dependency Assessment from a Core UI responsive dashboard but not from a Platform Analytics dashboard.

Dependency Assessment consists of several components:

-   **Top-down tree view**

    The top-down tree view shows the components of a performance analytics entity in a hierarchical view. If you launch dependency assessment on a dashboard, for example, the top-down tree view shows nodes for each of the dashboard tabs. When you select a dashboard tab, the tree view expands to show nodes that represent each of the widgets on the dashboard.

-   **Bottom-up tree view**

    The bottom-up tree view shows where a performance analytics entity is used in your instance. If you select **Show Used By** from the context menu of a tree view component, the tree view shows all the places where that entity is used. Click the reset icon \(![](../image/tree-view-reset-icon.png)\) to return to the top-down tree view.

-   **Component summaries**

    Click the info icon \(![Admin console tree view info button](../image/admin-console-treeview-info.png)\) to see a summary of the component.

-   **Other actions**

    Click the context menu icon \(![Admin console tree view context menu button](../image/admin-console-treeview-menu.png)\) in any component to view the actions available for that component. These include editing the component, viewing the schema map of the component, and previewing a widget.


**Note:** The tree view is persistent. When you return to Dependency Assessment, the tree view shows the same configuration as on the last visit.

-   **[Launch Dependency Assessment](../../dashboards/task/launch-dependency-assessment.md)**  
Use the Dependency Assessment tree view to view and edit Performance Analytics components including widgets, indicators, and breakdowns, from a single view. You can see the effects of your changes immediately.
-   **[Dependency Assessment tree view](dependency-assessment-treeview.md)**  
The tree view enables admin users to see the relationships between PA entities and to know the impact of changes made to any node in the tree view hierarchy.
-   **[Bottom-up tree view](../task/dependency-assessment-show-used-by.md)**  
You can see where any element in the tree view is used. This is useful when you want to change an element such as an indicator or breakdown and see the effect of your change on other PA elements.
-   **[Tree view navigation](../reference/admin-console-tree-view-nav.md)**  
To navigate the admin console tree view effectively, it's good to know what the various icons and other visual data in the tree view indicate.

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

