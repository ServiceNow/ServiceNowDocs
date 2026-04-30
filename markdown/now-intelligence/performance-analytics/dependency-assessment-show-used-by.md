---
title: Bottom-up tree view
description: You can see where any element in the tree view is used. This is useful when you want to change an element such as an indicator or breakdown and see the effect of your change on other PA elements.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-11-25"
reading_time_minutes: 1
breadcrumb: [Dependency Assessment, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Bottom-up tree view

You can see where any element in the tree view is used. This is useful when you want to change an element such as an indicator or breakdown and see the effect of your change on other PA elements.

## Before you begin

Role required: admin

**Important:** Dependency Assessment does not support Platform Analytics artifacts. It analyzes information only for Core UI Performance Analytics widgets but not Platform Analytics data visualizations. Also, you can launch Dependency Assessment from a Core UI responsive dashboard but not from a Platform Analytics dashboard.

## Procedure

1.  [Launch Dependency Assessment](../../dashboards/task/launch-dependency-assessment.md) on the Performance Analytics entity you want to investigate.

    1.  Navigate to **Performance Analytics** &gt; **Dashboards**.

    2.  Select the dashboard you want to investigate or the dashboard that uses the entity you want to investigate.

        In this example, we start with the Usage by Requestor dashboard.

    3.  From the context menu \(![](../image/ContextMenu.png)\), select **Launch Dependency Assessment**.

2.  Expand the tree view to locate the entity you want to investigate.

3.  Click the context menu \(![](../image/ContextMenu.png)\) of the entity and select **Show Used By**.![context menu option Show Used By to launch bottom-up tree view](../image/launch-bottom-up.png)

4.  The top-down tree view is replaced with a view which shows all of the entities which use the selected entity.

    In this case, the API Transactions Requestor Stats table is used by one breakdown source, three reports, and two interactive filters: ![bottom-up tree-view example](../image/bottom-up-tree-view-example.png)

5.  Click the reset button \(![](../image/tree-view-reset-icon.png)\) to return the tree view to the base selection as shown in the header.![Dependency assessment on the dashboard Usage by Requestor, with the reset button highlighted.](../image/dependency-assessment-reset.png)


**Parent Topic:**[Dependency Assessment](../concept/impact-analysis.md)

