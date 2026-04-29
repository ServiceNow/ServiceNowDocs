---
title: Content pack for Telecommunications orders
description: Using the Process Mining content pack for Order Management for Telecommunications and Media enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with Telecommunications orders.Analyze a process for telecommunications orders and identify the bottlenecks to minimize delays in the case flow for a better customer experience.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Content pack for Telecommunications orders

Using the Process Mining content pack for Order Management for Telecommunications and Media enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with Telecommunications orders.

For information about enabling the Process Mining for Telecommunications, see [Activate content packs](../task/activate-po-content-pack.md).

## End user and roles

If you have the required roles, you can use Analyst workbench to access the visualized process workflow data, and tools for analyzing the data related to telecommunications orders. For more information, see [Process Mining workspace](analyst-workbench-overview.md).

Based on the Telecommunications application that you're using the Process Mining application for, you need the following roles:

-   For Telecommunications Product Orders: sn\_process\_mining\_admin, sn\_process\_mining\_analyst, and sn\_process\_mining\_power\_user
-   For Telecommunications Service Orders: sn\_process\_mining\_admin, sn\_process\_mining\_analyst, and sn\_process\_mining\_power\_user
-   For Telecommunications Resource Orders: sn\_process\_mining\_admin, sn\_process\_mining\_analyst, and sn\_process\_mining\_power\_user
-   For Telecommunications Order Tasks: sn\_process\_mining\_admin, sn\_process\_mining\_analyst, and sn\_process\_mining\_power\_user

## Optimization projects for Telecommunications application

The content pack adds prebuilt process optimization project definitions for these Order Management for Telecommunications and Media application entities:

-   Product Orders
-   Service Orders
-   Resource Orders
-   Order Tasks

You can also configure a new process project that is based on a prebuilt project. For more information, see [Create a project or template using Project Builder](../task/define-workflow-model.md).

**Parent Topic:**[Activate content packs](../task/activate-po-content-pack.md)

**Related topics**  


[Example of Process Mining for Telecommunications](integration-with-telecommunications-orders.md#)

## Example of Process Mining for Telecommunications

Analyze a process for telecommunications orders and identify the bottlenecks to minimize delays in the case flow for a better customer experience.

For example, if you’re a process analyst in your telecommunications service provider where you must submit an analysis on current processes that are associated with telecommunications orders, you can use Analyst workbench to access the mined processes for the project definition for telecommunications product orders, service orders, resource orders, and order tasks.

You can analyze the case process flow and suggest ways to improve the processes by using the following workflow for the product orders in telecommunications project definition:

1.  Select **View in Workspace** from the selected project. Analyst workbench opens in a new tab.

    You can observe the average duration that a telecommunications customer order takes to be fulfilled.

2.  View the metrics of the process map by setting the Primary Metric and Secondary Metric lists to **Unique Occurrences** and **Average Duration**, respectively.
3.  Refine the process map by selecting **Refine** and selecting a connection width to see the full list of metrics.

    You can observe the state transitions and their duration.

4.  In the **Filters** tab, set up the Breakdown filters list for categories, and use the process step filters to filter out the records.
5.  In the **Variation Analysis** tab, you can view the routes that are taken by the records, the number of cases in a route, the average duration, and the number of steps that are involved in the route. Selecting a route highlights the route in the map.
6.  Add notes to the project by selecting the notes icon \(![Notes icon](../image/notes-icon.png)\) and submit an analysis.

![Example: Process Mining Analyst workbench for Telecommunications Orders.](../image/example-po-omt.png "Process Mining for product orders in telecommunications")

**Related topics**  


[Process Mining workspace](analyst-workbench-overview.md)

[Analyzing and getting process insights](analyze-get-process-insights.md)

[Content pack for Telecommunications orders](integration-with-telecommunications-orders.md#)

