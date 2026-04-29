---
title: Explore and manage dashboards
description: Quickly identify the relationships between Performance Analytics elements, such as dashboards, reports, and indicators. Each dashboard tab has customized interactive filters that enable you to refine the information that the dashboard shows.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Explore and manage dashboards

Quickly identify the relationships between Performance Analytics elements, such as dashboards, reports, and indicators. Each dashboard tab has customized interactive filters that enable you to refine the information that the dashboard shows.

## Explore dashboards example

To see all the [automated indicators](../../performance-analytics/concept/performance-analytics-glossary.md#) related to the Incident dashboard group based on the Incident table:

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Admin Console**
2.  Select **Dashboards** in the Explore and Manage tile.
3.  Select Dashboard Groups and Incident from the first two lists.
4.  Select the **Indicators** tab.
5.  From the **Indicator — Table** list, select **Incident** to see only the indicators on the Incident table.
6.  From the **Type** list, select **Automated** to see only the automated indicators on the Incident table.

![Explore dashboards example](../image/expl-db-ex.png)

## Dashboard and Dashboard Groups

Click **Dashboard** or **Dashboard Groups** to view a dashboard that provides information about all the in your instance:

-   **Dashboard groups**

    A list of all the dashboard groups in your instance. This tab has focus if you select **Dashboard Groups** on the Admin Console. Dashboards that do not have a group specified fall under the group **Other**.

    Use the **Visibility** filter to show all dashboard groups, dashboard groups that are visible to everyone, or dashboard groups limited to specified groups and users.

-   **Dashboards**

    A list of all the dashboards in your instance sorted by group. Expand the group to view the individual dashboards. Click the dashboard name to view and edit its details. This tab has focus if you select **Dashboards** on the Admin Console.

    Filters:

    -   Active — Choose **All**, Active=**True**, or Active=**False**.
    -   Dashboard owner — Choose **All** or select one or more owners from a list.
-   **Widgets**

    A list of all widgets used in your instance's dashboards.

    Filters:

    -   Type — Choose **All** or filter on one or more widget types. See [Performance Analytics widgets](../../performance-analytics/concept/c_Widgets.md).
    -   Visualization — Choose **All** or filter on one or more report visualization types from a list.
-   **Indicators**

    A list of all indicators used in your instance's dashboards. Filters: You can filter the list on **Indicator Table**, **Type**, **Frequency**, **Indicator Source**, **Units**, **Direction**, **Scripted**, and **Aggregation Type**. Click the name of the **Indicator** or **Indicator Source** to view and edit its details. For more information, see [Performance Analytics indicators](../../performance-analytics/concept/c_Indicators.md).

-   **Indicator Sources**

    A list of all indicator sources in your instance. You can filter the list on **Indicator Table** and **Frequency**. Click the name of the **Indicator Source** to view and edit its details. For more information, see [Indicator sources](../../performance-analytics/concept/c_IndicatorSources.md#).

-   **Breakdowns**

    A list of all breakdowns in your instance. You can filter the list on one or more **Breakdown Tables**. Click the names of the breakdown and the breakdown source to view and edit their details. For more information, see [Performance Analytics breakdowns](../../performance-analytics/concept/c_CreatingBreakdowns.md).

-   **Breakdown Sources**

    A list of all breakdown sources in your instance. You can filter the list on one or more **Breakdown Tables**. Click the name of the breakdown source to view and edit its details. For more information, see [Define a breakdown source](../../performance-analytics/task/t_DefiningABreakdownSource.md).

-   **Jobs**

    A list of all jobs created in your instance. The **Run** column shows how often the job runs. The **Time** column shows how long the job took the last time it ran. The list also shows whether the job is **Active**. Click the name of the job to view its details. For more information, see [Configure a job indicator](../../performance-analytics/task/configure-job-indicator.md).

-   **Reports**

    A list of all reports created on your instance. You can filter the list on one or more Report Tables and one or more Report Types. Click the title of a report to view its details. For more information, see [Create a report visualization](../../reporting/task/t_CreateYourOwnReport.md#).

-   **Interactive Filters**

    A list of all interactive filters configured on your instance. You can filter on what tables and fields the interactive filter is based on and one or more UI control types. Click the **Look up name** to view and edit the details of the interactive filter. For more information, see [Interactive Filters](../concept/c_HomepagePublishers.md).


**Related topics**  


[Tree view navigation](../../performance-analytics/reference/admin-console-tree-view-nav.md)

[Performance Analytics terms](../../performance-analytics/concept/performance-analytics-glossary.md#)

