---
title: Explore data assets lineage
description: Trace the upstream sources and downstream consumers of a data asset. Open the lineage view in Graph Explorer to examine specific relationships, focus on a path, and review related asset details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/explore-data-assets-lineage-dc.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 3
breadcrumb: [View data asset details, Finding and accessing data assets, Data Catalog, Workflow Data Fabric]
---

# Explore data assets lineage

Trace the upstream sources and downstream consumers of a data asset. Open the lineage view in Graph Explorer to examine specific relationships, focus on a path, and review related asset details.

Explore data assets lineage  

## Before you begin

Role required: WDF Consumer \(wdf\_consumer\)

## About this task

Graph Explorer is a visual tool in the Data Catalog for exploring how data assets and business concepts are connected. Graph Explorer has two views: **Relationships** shows direct semantic, conceptual, and governance connections among assets; **Lineage** shows the directed upstream and downstream flow of data.

The lineage view displays upstream sources, downstream consumers, and the relationships that connect them, at both the table level and the column level. It supports four primary use cases:

-   Impact analysis and change management. Identify the downstream reports, dashboards, models, and datasets that depend on a data asset before you modify or deprecate it.
-   Root cause analysis. Trace upstream from a problematic asset to find where a data quality issue originated, whether in a source system, a transformation, or a join.
-   Data discovery and understanding. Assess an asset's context and reliability by examining its sources and consumers.

Each asset's **Overview** tab includes a **Graph Explorer** section with side-by-side previews for **Relationships** and **Lineage**. The full visualization opens in a new tab and contains both views.

The lineage diagram has a sidebar that lists every asset, grouped by direction \(**Upstream**, **Lineage Target**, **Downstream**, **Ignored**\) and by degree of separation. The graph shows each asset as a node, with edges representing lineage relationships. An axis indicates the degree of separation for each column, from upstream to downstream. When multiple relationships connect the same two assets, the edge shows a numbered badge with the count of bundled relationships.

\[Omitted image "dc-data-asset-lineage-view.png"\] Alt text: View lineage for a data asset

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Data Catalog icon in the sidebar.

3.  In Data Catalog, open the asset whose lineage you want to explore.

4.  On the **Overview** tab, locate the **Graph Explorer** section.

    The section contains side-by-side previews for **Relationships** and **Lineage**.

5.  Open the full lineage view.

    -   Select **View** on the **Lineage** preview.
    -   Select **Open Graph Explorer** at the top of the asset page, then select the **Lineage** tab.
    The full visualization opens in a new tab.

6.  Interact with the visual representation of lineage.

    The focused asset appears in the diagram with upstream sources and downstream consumers, organized by degree of separation. The sidebar lists every asset in the lineage. This is the same data flow that the asset participates in, presented visually so that you can trace dependencies in either direction.

7.  Review the lineage tree in the sidebar.

    The sidebar groups assets by direction — **Upstream**, **Lineage Target**, **Downstream**, and **Ignored** — and by degree of separation within each direction. To narrow the list, enter text in the **Filter assets** field.

8.  Select an edge in the diagram to inspect its lineage relationships.

    A numbered badge on the edge shows the count of bundled relationships. Selecting the edge reveals the table-level and column-level dependencies it represents.

9.  Expand a container node to reveal the assets inside.

    Containers — such as databases that contain schemas, tables, and columns — appear as single nodes by default. Expanding a container reveals its nested assets so that you can examine the lineage in more detail.

10. Select a node to open the asset preview panel and view its details.

    The preview panel shows the asset name, hierarchy, type, original name, and recent activity. To navigate to the asset's full page, select the link next to the asset name.

11. Focus on a node to narrow the view to a specific path.

    Other assets are hidden and move to the **Ignored** group in the sidebar. To restore the hidden assets, select **Unignore**.

12. Use the controls in the diagram toolbar to zoom in, zoom out, or recenter the visualization.


**Parent Topic:**[View data asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/view-data-asset-details.md)

