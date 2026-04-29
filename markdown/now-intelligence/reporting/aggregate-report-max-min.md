---
title: Aggregate a report on minimum or maximum
description: When you create a report, you can aggregate the data on several calculations including the number of records, averages, and standard deviation. The maximum and minimum aggregations show the maximum or minimum value for each segment of the visualization.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Aggregation in reporting, Reporting reference, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Aggregate a report on minimum or maximum

When you create a report, you can aggregate the data on several calculations including the number of records, averages, and standard deviation. The maximum and minimum aggregations show the maximum or minimum value for each segment of the visualization.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## Minimum and Maximum

Select **Minimum** or **Maximum** to show the maximum or minimum value for each segment of the report. For example, apply the Maximum aggregation to incidents grouped by priority. The report shows a bar for the incident in each priority with the highest business duration.

These images illustrate maximum and minimum duration using grouped bars to show the different priorities of each category of incident side by side. Stacked bars give the illusion that the element on top of the stack has a greater value. In fact, the bar is only showing the relative value of the two elements.

|Maximum duration|Minimum duration|
|----------------|----------------|
|![Bar chart aggregated by Maximum duration with bars representing incident categories and priorities, one showing the maximum duration for critical software incidents of approximately 23 days, 21 hours.](../image/aggregation-max-dur-gr.png)|![Bar chart aggregated by Minimum duration with bars representing incident categories and priorities, one showing the minimum duration for critical software incidents of approximately 5 days.](../image/aggregation-min-dur-gr.png)|

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Select the report that you want to aggregate.

3.  On the Configure tab, choose **Maximum** or **Minimum** from the **Aggregation** list.

4.  Select **Run**.


## Result

The sections of the visualization are grouped by the highest or lowest value for the selected records.

