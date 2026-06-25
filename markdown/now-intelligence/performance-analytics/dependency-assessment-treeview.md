---
title: Dependency Assessment tree view
description: The tree view enables admin users to see the relationships between PA entities and to know the impact of changes made to any node in the tree view hierarchy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/dependency-assessment-treeview.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [\(Legacy\) Dependency Assessment, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Dependency Assessment tree view

The tree view enables admin users to see the relationships between PA entities and to know the impact of changes made to any node in the tree view hierarchy.

**Important:** Dependency Assessment does not support Platform Analytics artifacts. It analyzes information only for Core UI Performance Analytics widgets but not Platform Analytics data visualizations. Also, you can launch Dependency Assessment from a Core UI responsive dashboard but not from a Platform Analytics dashboard.

The Dependency Assessment tree view consists of a variety of possible nodes and a legend. The nodes represent Performance Analytics entities. Point to a node and the node's type is highlighted in the legend. When you click on a node in the tree view, the child nodes open. If there are more than eight nodes in a level of the tree view, then six are shown and a seventh node indicates how many nodes are not shown. Click this node to view a list of the other nodes.

The tree view header contains choice lists for changing the PA entity type and a value. The tree view updates according to your choices. Click the reset button \(\[Omitted image "tree-view-reset-icon.png"\] Alt text:\) to return the tree view to the starting point with just the first level parent and its immediate child nodes.

Each node has a context menu \(\[Omitted image "admin-console-treeview-menu.png"\] Alt text: Admin console tree view context menu button\) where you can choose from a number of actions. Choose **Show Used By** to change the tree view to show where a node is used in your instance. See [Bottom-up tree view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/dependency-assessment-show-used-by.md) for more information.

\[Omitted image "impact-analysis-remaining-nodes2.png"\] Alt text: Top-down dependency assessment with list of remaining nodes

The figure below gives an example of the top-down tree view, starting from a dashboard at the top level, its tabs on the second level, the widgets of one of the dashboard tabs on the third level, and so on. The tree view in the example shows all breakdowns and supporting indicators as they are defined in the Breakdown form.

\[Omitted image "impact-analysis-example.png"\] Alt text: Top-down dependency assessment with legend

**Parent Topic:**[\(Legacy\) Dependency Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/impact-analysis.md)

**Related topics**  


[Performance Analytics breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_CreatingBreakdowns.md)

