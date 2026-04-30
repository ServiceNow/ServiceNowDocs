---
title: Evaluate equality between date values
description: Date comparison evaluates a match for one of several date increments.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Comparing field values, Condition builder, Create a condition statement using the condition builder, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Evaluate equality between date values

Date comparison evaluates a match for one of several date increments.

## Before you begin

Role required: none

## About this task

You can specify granularity to the hour, day, week, month, quarter, or year. For example, the filter **\[Created on\] \[is same\] \[Week\] as \[Closed\]** returns records that were closed in the same week that they were opened. When you run this type of filter, be sure to specify the year in an additional filter condition of **\[Created\] \[is same\] \[Year\] as \[Closed\]** to eliminate records that were created a year before they were closed.

![](../image/DatesFieldComparison.png "Date field comparison")

## Procedure

1.  In the condition builder, create a new condition.

2.  Select a date field from the left operand choice list.

3.  Select **\[is same\]** or **\[is different\]** from the operator choice list.

    An additional choice list appears.

4.  Select the granularity from the date range choice list.

    |Date Range|Description|
    |----------|-----------|
    |Hour|Filters on the hour of the day.|
    |Day|Filters on the day of the month, not the date. For example, a Day value of the 1 of August matches with a Day value of the 1 of September.|
    |Week|Filters on the week of the year. ServiceNow defines a week as Sunday through Saturday for the purposes of Field Comparison.|
    |Month|Filters on the month of the year. For example, any date within December returns the 12 month of the year.|
    |Quarter|Filters on the quarter of the year.|
    |Year|Filters on the year.|

5.  Select a different date field from the right operand choice list.

6.  Click **Run**.


**Parent Topic:**[Comparing field values](../reference/r_ComparingFieldValues.md)

