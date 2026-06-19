---
title: Bottom-up tree view
description: You can see where any element in the tree view is used. This is useful when you want to change an element such as an indicator or breakdown and see the effect of your change on other PA elements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/dependency-assessment-show-used-by.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [\(Legacy\) Dependency Assessment, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Bottom-up tree view

You can see where any element in the tree view is used. This is useful when you want to change an element such as an indicator or breakdown and see the effect of your change on other PA elements.

## Before you begin

Role required: admin

**Important:** Dependency Assessment does not support Platform Analytics artifacts. It analyzes information only for Core UI Performance Analytics widgets but not Platform Analytics data visualizations. Also, you can launch Dependency Assessment from a Core UI responsive dashboard but not from a Platform Analytics dashboard.

## Procedure

1.  [Launch Dependency Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/launch-dependency-assessment.md) on the Performance Analytics entity you want to investigate.

    1.  Navigate to **Performance Analytics** &gt; **Dashboards**.

    2.  Select the dashboard you want to investigate or the dashboard that uses the entity you want to investigate.

        In this example, we start with the Usage by Requestor dashboard.

    3.  From the context menu \(\[Omitted image "ContextMenu.png"\] Alt text:\), select **Launch Dependency Assessment**.

2.  Expand the tree view to locate the entity you want to investigate.

3.  Select the context menu \(\[Omitted image "ContextMenu.png"\] Alt text:\) of the entity and select **Show Used By**.\[Omitted image "launch-bottom-up.png"\] Alt text: context menu option Show Used By to launch bottom-up tree view

4.  The top-down tree view is replaced with a view which shows all of the entities which use the selected entity.

    In this case, the API Transactions Requestor Stats table is used by one breakdown source, three reports, and two interactive filters: \[Omitted image "bottom-up-tree-view-example.png"\] Alt text: bottom-up tree-view example

5.  Click the reset button \(\[Omitted image "tree-view-reset-icon.png"\] Alt text:\) to return the tree view to the base selection as shown in the header.\[Omitted image "dependency-assessment-reset.png"\] Alt text: Dependency assessment on the dashboard Usage by Requestor, with the reset button highlighted.


**Parent Topic:**[\(Legacy\) Dependency Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/impact-analysis.md)

