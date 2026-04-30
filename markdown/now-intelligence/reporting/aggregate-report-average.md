---
title: Aggregate a report on averages
description: When you create a report, you can aggregate the data on several calculations including the number of records, averages, and standard deviation. The sum aggregation shows the sum of the field you aggregate on.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Aggregation in reporting, Reporting reference, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Aggregate a report on averages

When you create a report, you can aggregate the data on several calculations including the number of records, averages, and standard deviation. The sum aggregation shows the sum of the field you aggregate on.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

**Average** aggregation shows the arithmetic mean of the field you aggregate on. For example, select a duration field. The aggregated data is expressed in terms of days, hours, minutes, and seconds. \(You can configure durations to show the level of detail you want.\) If you select an integer field, such as **Priority**, the data is expressed as a decimal value number.

When you choose the average aggregation, you can also specify the **Percentage calculation** The percentage calculation is displayed when you select **Show data table**.

-   **Use Aggregation**

    Shows the percentage as a part of the total amount of averages in a column called **Percentage of Average**. In this data table, for example, the average duration of the Inquiry, Network, and Software incidents was approximately one day and 16 hours or 30% \(or so\) of the total average business duration. Average hardware incidents took 12 hours, approximately 9% of the total average business duration for incidents.

    ![Data table showing four categories of incidents, their average business duration, and the percentage of the average time to solve](../image/aggregation-avg.png)

-   **Use Record Count**

    Shows the number of records in each category as a percentage of the total number of records in the visualization in a column called **Percentage of Incidents**. In this data table, we see the same Average Business Duration for each category, but the percentage is of the number of incidents in that category. For example Inquiry incidents are approximately 17% of all incidents, and software incidents are approximately 77% of all incidents, though the average time to solve these incidents is still 30% \(or so\). On the other hand, Hardware incidents are less than 1% of all incidents, but the average duration is 9% of the total average time to solve.

    ![Data table showing four categories of incidents, the average business duration of the incidents in the category, and the percentage of total incidents represented by each category.](../image/rec-count-avg.png)


|Average duration|Average priority|
|----------------|----------------|
|![Bar chart aggregated by Average duration with five bars representing incident categories, one showing the average duration for network incidents of approximately 12 days, 19 hours.](../image/aggregation-avg-dur.png)|![Bar chart aggregated by Average priority with five bars representing incident categories, one showing the average priority for network incidents of 2.98.](../image/aggregation-avg-prio.png)|

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Select the report that you want to aggregate.

3.  On the Configure tab, choose Average from the **Aggregation** list.

4.  Choose the field to aggregate.

5.  Select **Run**.


## Result

The sections of the visualization are grouped by the average of the selected records.

