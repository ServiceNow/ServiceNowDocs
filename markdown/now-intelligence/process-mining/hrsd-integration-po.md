---
title: Content pack for HR Service Delivery
description: Using the Process Mining content pack for HR Service Delivery enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.Analyze a process for your HR service or, if installed, Lifecycle Events cases and identify bottlenecks to minimize delays in the case flow for a better user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/hrsd-integration-po.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Automatic content pack delivery, Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Content pack for HR Service Delivery

Using the Process Mining content pack for HR Service Delivery enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.

This content pack loads automatically when HR Service Delivery is installed on your instance and the relevant tables are present. For more information, see [Automatic delivery of content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/process-mining-content-pack-delivery.md).

## Templates shipped with content pack

|Content pack|Template name|Table|
|------------|-------------|-----|
|HR Service Delivery|Standard template for HR Cases|sn\_hr\_core\_case|
|Custom template for HR LE Onboarding Cases|sn\_hr\_le\_case|
|Standard template for HR Lifecycle Events Cases|sn\_hr\_le\_case|

## What you get with this content pack

This content pack analyzes your HR case processes, including onboarding and lifecycle events cases if Lifecycle Events is installed. It gives you visibility into common process issues, such as:

-   Cases that take longer than expected to resolve
-   Rework, such as cases that get reopened or bounced back between teams
-   Deviations from the expected process flow
-   Work that stalls with a particular team or agent longer than expected

For onboarding cases specifically, the content pack also analyzes related onboarding tasks \(such as Day 1, Day 30, pre-boarding, and pre-hire tasks\) as part of the same analysis. Viewing this deeper onboarding analysis requires the `sn_hr_core.admin` or `sn_hr_core.manager` role.

## End user and roles

If you have the required roles, you can use Analyst workbench to access the visualized process workflow data, and tools for analyzing the data related to customer service cases. For more information, see [Analyst workbench page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/analyst-workbench-dashboard.md).

The following combinations of roles are required for using the Process Mining application with HR Service Delivery.

|Process Mining role|HR Service Delivery role|
|-------------------|------------------------|
|sn\_process\_mining\_admin|sn\_hr\_core.admin|
|sn\_process\_mining\_power\_user|sn\_hr\_core.case\_writer|
|sn\_process\_mining\_analyst|sn\_hr\_core.basic|

**Parent Topic:**[Automatic delivery of content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/process-mining-content-pack-delivery.md)

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

6.  Add notes to the project by selecting the notes icon \(\[Omitted image "notes-icon.png"\] Alt text: notes icon\) and submit an analysis.

\[Omitted image "example-po-hrsd2.png"\] Alt text: Process Mining for a standard HR Service case

