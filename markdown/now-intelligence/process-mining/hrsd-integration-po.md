---
title: Content pack for HR Service Delivery
description: Using the Process Mining content pack for HR Service Delivery enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.Analyze a process for your HR service or, if installed, Lifecycle Events cases and identify bottlenecks to minimize delays in the case flow for a better user experience.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Content pack for HR Service Delivery

Using the Process Mining content pack for HR Service Delivery enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

For more information about enabling the HRSD Process Mining Content Pack, see [Activate content packs](../task/activate-po-content-pack.md).

## End user and roles

If you have the required roles, you can use Analyst workbench to access the visualized process workflow data, and tools for analyzing the data related to customer service cases. For more information, see [Analyst workbench page](analyst-workbench-dashboard.md).

The following combinations of roles are required for using the Process Mining application with HR Service Delivery.

|Process Mining role|HR Service Delivery role|
|-------------------|------------------------|
|sn\_process\_mining\_admin|sn\_hr\_core.admin|
|sn\_process\_mining\_power\_user|sn\_hr\_core.case\_writer|
|sn\_process\_mining\_analyst|sn\_hr\_core.basic|

## Optimization project for HR cases

The HRSD Process Mining Content Pack \(com.sn\_hr\_process\_optimization\) adds a prebuilt project that includes predefined HR service cases and, if installed, Lifecycle Events cases project definitions. By default, the project filters cases for the last two quarters. You can also configure a new process project based on the prebuilt project. For more information, see [Create a project or template using Project Builder](../task/define-workflow-model.md).

The project definition includes default activity definitions and breakdown definitions for cases that you can use as they’re or modify for a custom configuration.

-   Use activity definitions to understand state transitions such as cases transitioning from the work in progress state to the solution proposed state and analyze the linked processes such as Problem \(PRB\) records.
-   Use breakdown definitions to filter records and analyze a process map by categories. For example, you can filter the case data by different channels, products, assignment groups, and locations.

## Continual Improvement Management initiative for HR cases

If the Continual Improvement Management \(CIM\) application is enabled, you can also use the CIM project from Analyst workbench to track the progress of improvement initiatives for HR cases. The improvement initiative and Process Mining project are automatically linked. For more information, see [Integration with Continual Improvement Management](integrate-with-continuous-i.md#).

## Performance Analytics for HR cases

If the Performance Analytics \(PA\) application is enabled, you can also use the available template configurations to open the Process Mining application from a Performance Analytics [indicator](../../../use/performance-analytics/concept/performance-analytics-glossary.md#) based on the customer service case data. For more information, see [Integration with Performance Analytics](integrate-pa.md#).

**Parent Topic:**[Activate content packs](../task/activate-po-content-pack.md)

## Example of Process Mining for HR Service Delivery

Analyze a process for your HR service or, if installed, Lifecycle Events cases and identify bottlenecks to minimize delays in the case flow for a better user experience.

Say that you’re an HR onboarding process analyst who wants to improve the speed or quality of your service delivery and you must submit analysis on your current case processes. You can use Analyst workbench to access the mined processes for the HR service and, if installed, Lifecycle Events cases project definitions.

You can analyze the case process flow and suggest ways to improve the processes by using the following workflow. For example, for a standard HR Service case model definition, you can:

1.  Select **View in Workspace** from the selected project. Analyst workbench opens in a new tab.

    On the **All by HR Service** tab, you can observe how long it takes for an HR service case record to be closed.

2.  View metrics of the process map by setting the Primary Metric and Secondary Metric lists to **Total Occurrences** and **Avg Duration**, respectively.
3.  Refine the process map by selecting **Refine** and selecting a connection width to see the full list of metrics.

    You can observe the state transitions and their duration.

4.  In the **Breakdown** tab, set up the Breakdown filters list for categories and use the activity transitions filters to filter out the records.
5.  In the Variation Analysis tab, you can view the routes taken by the records, the number of cases in a route, the average duration, and the number of steps involved in the route. Selecting a route highlights the route in the map.

    **Note:** After applying one of more routes, the breakdowns listed in the **Breakdown Filters** tab display only those breakdowns applicable to those routes.

6.  Add notes to the project by selecting the notes icon \(![notes icon](../image/notes-icon.png)\) and submit an analysis.

![Process Mining for a standard HR Service case](../image/example-po-hrsd2.png "Process Mining for a standard HR Service case")

