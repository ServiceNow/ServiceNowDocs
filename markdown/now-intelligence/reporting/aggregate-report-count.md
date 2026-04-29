---
title: Aggregate a report on count
description: When you create a report, you can aggregate the data on several calculations including the number of records, averages, and standard deviation. The count aggregation gives the number of records in each element of a visualization.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Aggregation in reporting, Reporting reference, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Aggregate a report on count

When you create a report, you can aggregate the data on several calculations including the number of records, averages, and standard deviation. The count aggregation gives the number of records in each element of a visualization.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

The default aggregation is **Count**. The Count aggregation shows the number of records selected.

To show only unique records, select **Count Distinct**. For example, you want to show the value for the distinct number of task types being performed. Task types being performed for multiple customers are counted multiple times unless you use **Count Distinct**.

These images compare Count and Count Distinct. The first shows that the raw count of for one column is 632. The second shows that the distinct count for the same column is only 8.

|Count|Count Distinct|
|-----|--------------|
|![Bar chart aggregated by Count with four bars, one showing the count for 90 days equals 632.](../image/aggregation-count.png)|![Bar chart aggregated by Count Distinct with four bars, one showing the distinct count for 90 days equals 8.](../image/aggregation-count-distinct.png)|

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Select the report you want to aggregate.

3.  On the Configure tab, choose **Count** or **Count Distinct** from the **Aggregation** list.

4.  Select **Run**.


## Result

The sections of the visualization are grouped by the count of records.

