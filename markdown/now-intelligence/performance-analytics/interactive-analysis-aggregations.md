---
title: Interactive Analysis aggregations
description: When you work with Interactive Analysis, you can view data from the perspectives of record counts, sums, averages, and distinct counts.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Interactive Analysis, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Interactive Analysis aggregations

When you work with Interactive Analysis, you can view data from the perspectives of record counts, sums, averages, and distinct counts.

## Aggregation types

-   **Count**

    Count is the default aggregation and shows when you launch Interactive Analysis. The Count aggregation shows the number of records selected. For example, an analysis of incidents grouped by state, stacked by priority, and aggregated by count shows the number of incidents in each category in hints and in the cells of multidimensional reports.

    ![Interactive analysis with count aggregation and hints.](../image/ia-aggregation-count.png)

-   **Average, Sum, Count Distinct**

    Select **Average**, **Sum**, or **Count Distinct**, to show a list of fields from the selected **Table**. You may further be able to aggregate on fields from extended tables. See [How to report on extended tables.](t_AccessFieldExtendedTable.md#) Select a field to **Aggregate by** from this list. For example, if you select an integer field, such as **Reassignment count**, the data is expressed as a decimal value number. For more information, see [Column reports](../concept/c_CreateColumnCharts.md#).

    **Note:** For duration values, the unit of measurement displayed in the aggregation axis cannot be customized.

    If you select **Count Distinct**, only unique records are counted. For example, you want to generate a report with a distinct number of users who have one or more of the roles in a given list of roles. Users with more than one role would be counted twice unless you use **Count Distinct**.


![Interactive analysis with Sum aggregation and Priority field](../image/ia-aggregation-sum-rc.png)

**Parent Topic:**[Interactive Analysis](../../dashboards/concept/interactive-analysis.md)

