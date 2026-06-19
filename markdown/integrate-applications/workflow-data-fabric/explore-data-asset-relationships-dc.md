---
title: Explore data asset relationships
description: See the data assets, business terms, and governance objects connected to a data asset. Open the relationships view in Graph Explorer to expand, hide, and rearrange the graph.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/explore-data-asset-relationships-dc.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 2
breadcrumb: [View data asset details, Finding and accessing data assets, Data Catalog, Workflow Data Fabric]
---

# Explore data asset relationships

See the data assets, business terms, and governance objects connected to a data asset. Open the relationships view in Graph Explorer to expand, hide, and rearrange the graph.

Explore data asset relationships  

## Before you begin

Role required: WDF Consumer \(wdf\_consumer\)

## About this task

Graph Explorer is a visual tool in the Data Catalog for exploring how data assets and business concepts are connected. Graph Explorer has two views: **Relationships** shows direct semantic, conceptual, and governance connections among assets; **Lineage** shows the directed upstream and downstream flow of data.

The relationships view in Graph Explorer shows how a data asset connects to other assets, business concepts, and governance objects in the Data Catalog. The view covers semantic, conceptual, and governance connections across tables, columns, dashboards, business terms, policies, and other catalog objects. It presents the same content as the Related Assets tab of the asset page, in a graph for visual exploration.

\[Omitted image "dc-data-asset-relationship-view.png"\] Alt text: View relationships for a data asset

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Data catalog icon in the left sidebar.

3.  In Data Catalog, open the asset whose relationships you want to explore.

4.  On the **Overview** tab, locate the **Graph Explorer** section.

    The section contains side-by-side previews for **Relationships** and **Lineage**.

5.  Open the full relationships view.

    -   Select **View** on the **Relationships** preview.
    -   Select **Open Graph Explorer** at the top of the asset page.
    The full visualization opens in a new tab. The Relationships view opens by default.

6.  Interact with the visual representation of relationships.

    The central node represents the data asset from which you opened Graph Explorer . All connected nodes represent different types of related data assets, with arrows indicating the type of relationship. This is the same information shown in the Related assets tab of the data asset, but presented visually.

7.  To expand or hide the connections of a related asset, select the node, then select **Show relationships** or **Hide relationships**.

8.  To inspect a grouped node, select the node, then select **Unpack**.

    The group expands to show the individual assets it contains. To collapse the group again, select **Repack**.

9.  To view the details of a related asset, select the node, then select **Show asset details**.

    The asset preview panel opens with the asset name, hierarchy, type, original name, and recent activity. To navigate to the asset's full page, select the link next to the asset name.

10. To customize the layout, drag nodes to new positions on the canvas.

11. Use the controls in the diagram toolbar to zoom in, zoom out, or recenter the visualization.


**Parent Topic:**[View data asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/view-data-asset-details.md)

