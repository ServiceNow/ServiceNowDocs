---
title: DCE Insights tables
description: DCE Insights is a feature of the Data Context Engine that enhances how users view and interact with data directly on record pages and includes the following tables
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure DCE Visualizations, Set up the Data Context Engine, Customer success, Customer Success Management, Customer Success Management]
---

# DCE Insights tables

DCE Insights is a feature of the Data Context Engine that enhances how users view and interact with data directly on record pages and includes the following tables

## DCE Visualization

DCE Visualization enables users to configure data sources, define baselines and targets, and apply aggregation rules. It also supports the setup of conditional logic, allowing visualizations to be tailored to specific scenarios, for example, displaying customer-specific data based on defined conditions. See [Configure DCE Visualizations](../task/account-lifecycle-configure-dce-visual.md) for detailed descriptions of all the fields in this table.

## DCE Insights

The DCE Insights table is a central repository for all configured data visualizations. It contains the following fields.

-   Name: Name of the entity.
-   Entity: Table where the visualization items are to be displayed.

## DCE Insights Item

Each DCE Item maps a specific visualization to a designated location on a layout, ensuring that insights are displayed in the right context within the user interface. It contains the following fields.

-   Name: Name of the insight item.
-   DCE Insight: References the DCE Insights entity.
-   Visualization mode:
    -   Single: If it is mapped to a single metric.
    -   Multiple: If it is mapped to a group of metrics.

## DCE Visualization M2Ms

This table maintains the relationship between DCE Visualization and DCE Insights Item. It contains the following fields.

-   DCE insight item: References the DCE Insights item.
-   Visualization: References the DCE Visualization item.
-   Rank: The rank for the visualization.

