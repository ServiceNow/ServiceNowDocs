---
title: Aggregate a report on sum
description: When you create a report, you can aggregate the data on several calculations including the number of records, averages, and standard deviation. The sum aggregation shows the sum of the field you aggregate on.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-05-09"
reading_time_minutes: 1
breadcrumb: [Aggregation in reporting, Reporting reference, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Aggregate a report on sum

When you create a report, you can aggregate the data on several calculations including the number of records, averages, and standard deviation. The sum aggregation shows the sum of the field you aggregate on.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## Sum

Select **Sum** to show the sum of the field you aggregate on. For example, select a duration field. The aggregated data is expressed in terms of days, hours, minutes, and seconds. \(You can configure durations to show the level of detail you want.\) Select an integer field, such as **Priority**, and the data is expressed as a whole number.

![Bar chart aggregated by Sum duration with five bars representing incident categories, one showing the sum duration for software incidents of approximately 100 days, 17 hours.](../image/aggregation-sum-dur.png)

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Select the report that you want to aggregate.

3.  On the Configure tab, choose Sum from the **Aggregation** list.

4.  Choose the field to aggregate.

5.  Select **Run**.


## Result

The sections of the visualization are grouped by the sum of the selected records. Select a duration field and the aggregated data is expressed in terms of days, hours, minutes, and seconds. Select an integer field, such as **Priority**, and the data is expressed as whole numbers.

