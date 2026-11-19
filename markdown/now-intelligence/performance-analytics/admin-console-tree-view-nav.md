---
title: Tree view navigation
description: To navigate the admin console tree view effectively, it's good to know what the various icons and other visual data in the tree view indicate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/performance-analytics/admin-console-tree-view-nav.html
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [\(Legacy\) Dependency Assessment, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Tree view navigation

To navigate the admin console tree view effectively, it's good to know what the various icons and other visual data in the tree view indicate.

**Important:** Dependency Assessment does not support Platform Analytics artifacts. It analyzes information only for Core UI Performance Analytics widgets but not Platform Analytics data visualizations. Also, you can launch Dependency Assessment from a Core UI responsive dashboard but not from a Platform Analytics dashboard.

## Moving through the tree view

You can click and drag the tree view to show nodes that are outside of the screen. You can also use Ctrl+A and then use the arrow keys to move the tree view around. Use Tab to return to the first node in the tree.

## Node types

The node types reflect the different features of Performance Analytics. When you click a node, it expands into its child features on the next level of the tree view.

-   **Dashboard-related nodes**

    Dashboards group nodes expand into dashboards. Dashboards expand into dashboard tabs even if the dashboard has only one tab. Dashboard tabs expand into the contents of the tab.

-   **Widgets**

    Widgets open nodes that show their component parts.

-   **Indicators**

    All indicator nodes open into nodes for their component sources, breakdowns, jobs, and scripts. Indicator nodes include automated, formula, widget, manual, external and supporting indicators.

-   **Reports**

    Reports open nodes that show their component tables.

-   **Breakdowns**

    Breakdowns open nodes that show their sources.

-   **Sources**

    All source nodes \(breakdown, indicator, and report sources\) open nodes that show their source tables.


When you click a text widget, the underlying file appears as a pop-up over the tree view. Choices from a context menu appear in a pop-up as well.

## Icons

<table id="table_vkf_3gx_1cb"><thead><tr><th>

Icon

</th><th>

Function

</th><th>

Context menu actions

</th></tr></thead><tbody><tr><td>

\[Omitted image "admin-console-treeview-dashboard-group.png"\] Alt text: tree view dashboard group

</td><td>

Dashboard group

</td><td>

Edit

</td></tr><tr><td>

\[Omitted image "admin-console-treeview-dashboard.png"\] Alt text: tree view dashboard

</td><td>

Dashboard

</td><td>

-   Edit
-   View Dashboard

When you select View Dashboard, the dashboard is shown in a pop-up over the tree view. All the dashboard's features are available including sharing, layout configuration, and adding widgets. When you close the pop-up, the tree view is visible again.

-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-tab.png"\] Alt text: tree view tab

</td><td>

Dashboard tab

</td><td>

-   Edit
-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-report.png"\] Alt text: tree view report

</td><td>

Report

</td><td>

-   Edit

Opens the report in the Report Designer in a pop-up window. When you close the pop-up, the tree view is visible again.

-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-report-source.png"\] Alt text: tree view report source

</td><td>

Report source

</td><td>

-   Edit
-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-filter.png"\] Alt text:

</td><td>

Interactive Filter

</td><td>

-   Edit
-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-indicator-widget.png"\] Alt text:

</td><td>

Performance Analytics Widget

</td><td>

-   Edit
-   Preview Widget

Select **Preview Widget** to show the widget in a pop-up window.

-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-widget.png"\] Alt text: tree view other widget icon

</td><td>

Other Widget

</td><td>

No context menu.

</td></tr><tr><td>

\[Omitted image "admin-console-treeview-formula-indicator.png"\] Alt text:

</td><td>

Formula Indicator

</td><td>

-   Edit
-   Show Analytics Hub
-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-automatic-indicator.png"\] Alt text:

</td><td>

Automated Indicator

</td><td>

-   Edit
-   Show Analytics Hub
-   Show Scores
-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-indicator-widget.png"\] Alt text:

</td><td>

Widget Indicator

</td><td>

-   Edit
-   Preview Widget

Select **Preview Widget** to show the widget in a pop-up window.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-indicator-widget.png"\] Alt text:

</td><td>

Supporting Indicators

</td><td>

Edit

</td></tr><tr><td>

\[Omitted image "admin-console-treeview-manual-indicator.png"\] Alt text:

</td><td>

Manual indicator

</td><td>

Edit

</td></tr><tr><td>

\[Omitted image "admin-console-treeview-manual-indicator.png"\] Alt text:

</td><td>

External indicator

</td><td>

Edit

</td></tr><tr><td>

\[Omitted image "admin-console-treeview-indicator-source.png"\] Alt text:

</td><td>

Indicator source

</td><td>

-   Edit
-   Show Schema Map
-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-breakdown-widget.png"\] Alt text:

</td><td>

Linked Breakdown

</td><td>

No context menu. Click the tile to reveal the associated breakdowns.

</td></tr><tr><td>

\[Omitted image "admin-console-treeview-breakdown.png"\] Alt text:

</td><td>

Breakdown

</td><td>

-   Edit
-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-breakdown-source.png"\] Alt text:

</td><td>

Breakdown Source

</td><td>

-   Edit
-   Show Schema Map
-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-dc-job.png"\] Alt text:

</td><td>

Job

</td><td>

-   Edit
-   Execute Now
-   View All Logs
-   View Last executed Log
-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-script.png"\] Alt text:

</td><td>

Script

</td><td>

Edit

</td></tr><tr><td>

\[Omitted image "admin-console-treeview-fact-table.png"\] Alt text:

</td><td>

Table

</td><td>

-   Edit
-   Show Schema Map
-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr><tr><td>

\[Omitted image "admin-console-treeview-if.png"\] Alt text:

</td><td>

Filter widget

</td><td>

-   Edit
-   Preview Widget

Select **Preview Widget** to show the widget in a pop-up window.

-   Show Used By

Launches the [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) which shows all entities that use this entity.


</td></tr></tbody>
</table>## Other visual data

Each node has one or more of these icons. Point to the upper right corner of the node to show them.

-   **Info button \[\[Omitted image "admin-console-treeview-info.png"\] Alt text: Admin console tree view info button\]**

    Click the info button to reveal further details about the node. A node's information panel shows different information depending on the type of node, but all information panels have an **Open Record** button. Click **Open Record** to open the record for editing.

-   **Context menu \[\[Omitted image "admin-console-treeview-menu.png"\] Alt text: Admin console tree view context menu button\]**

    Click the context menu icon to perform further actions on the node's source.

-   **Error indicators \[\[Omitted image "admin-console-treeview-error.png"\] Alt text: Admin console tree view error indicator\]**

    Open the element the node refers to so that you can correct any issues.


**Parent Topic:**[\(Legacy\) Dependency Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/impact-analysis.md)

