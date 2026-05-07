---
title: View data asset details
description: View comprehensive information about data assets on the asset detail page.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Finding and accessing data assets, Data Catalog, Workflow Data Fabric]
---

# View data asset details

View comprehensive information about data assets on the asset detail page.

## Before you begin

Role required: WDF Consumer \(wdf\_consumer\)

## About this task

Asset detail pages organize information into tabs for easy navigation. The Overview tab provides summary information, while additional tabs offer detailed views of specific aspects like columns, relationships, and lineage. ![View details of a data asset](../image/dc-data-asset-details.png)

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Data catalog icon in the left sidebar.

3.  Select the data asset you want to view.

4.  On the Overview tab view the general details about the asset, such as, the name, source, columns included \(if it is a table\), the preview of the graph explorer.

5.  On the Columns tab, view column information for tabular assets, such as tables.

    Click a column name to browse to the details page of the column.

6.  On the Related assets tab, view the list of connected catalog assets.

7.  On the Graph Explorer tab, interact with the visual representation of relationships.

    Graph Explorer is an interactive, visual tool that helps you understand how data assets and business concepts are connected in your catalog. This tool supports semantic, conceptual, and governance connections across tables, dashboards, business terms, policies, and more — enabling faster discovery, better understanding, and more confident decision-making.

    -   The central node in the graph represents the data asset from which you are viewing the Graph Explorer. All connected nodes represent different types of related data assets, with arrows indicating the type of relationship. This is the same information shown in the Related assets tab of the data asset, but presented visually—making it easier to understand and explore the relationships at a glance.
    -   Select a node and use the **Hide relationships** and **Show relationships** options to expand or hide the related assets.
    -   For grouped nodes, like columns, use the **Unpack** and **Repack** options to show and hide the grouped assets.
    -   Use the **Show assets details** option to view the details of a related asset.
    -   Move nodes freely across the canvas to customize your layout.

**Parent Topic:**[Finding and accessing data assets](../concept/find-access-data-assets-dc.md)

