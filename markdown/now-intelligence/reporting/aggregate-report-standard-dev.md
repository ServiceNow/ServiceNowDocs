---
title: Aggregate a report on standard deviation
description: When you create a report, you can aggregate the data on several calculations including the number of records, averages, and standard deviation. The standard deviation aggregation shows variation from average values for a duration or numeric field in a visualization.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-05-09"
reading_time_minutes: 1
breadcrumb: [Aggregation in reporting, Reporting reference, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Aggregate a report on standard deviation

When you create a report, you can aggregate the data on several calculations including the number of records, averages, and standard deviation. The standard deviation aggregation shows variation from average values for a duration or numeric field in a visualization.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## Standard deviation

Select **Standard deviation** \(SD\) to see variation from average values for a duration or numeric field. For example, apply the Standard deviation aggregation to business duration of incidents. The report shows deviation from the average business duration of incidents in each priority.

Standard deviation is always expressed in the same unit as the data. In the following example, the data is in time units and so is the aggregation.

![Bar chart aggregated by Standard deviation with bars representing incident categories and priorities, one showing the standard deviation for critical software incidents of approximately 10 days, 9 hours.](../image/aggregation-standard-deviation.png)

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Select the report that you want to aggregate.

3.  On the Configure tab, choose **Standard Deviation** from the **Aggregation** list.

4.  Select **Run**.


## Result

The sections of the visualization are grouped by the highest or lowest value for the selected records.

