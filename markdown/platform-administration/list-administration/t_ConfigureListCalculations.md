---
title: Configure list calculations
description: You can configure list calculations for columns, which calculate column totals, minimums, maximums, and averages.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [List configuration, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure list calculations

You can configure list calculations for columns, which calculate column totals, minimums, maximums, and averages.

## Before you begin

Role required: personalize\_list.

## About this task

You can configure list calculations for multiple columns in the same list. List calculations apply only to the view of the list in which they are configured. All users can see configured list calculations.

**Note:**

-   List calculations are also available in list reports.
-   List calculations for a calculated field can only operate on the \*current values stored in the database for each record and not the values as calculated fresh when the list is rendered.

## Procedure

1.  In a list of records, right-click the header of a numeric column you want to evaluate with list calculations.

2.  Select **Configure** &gt; **List Calculations**.

3.  Select one or more of the following list calculation options:

    -   Total value \(not available for string, date, or date/time fields\)
    -   Minimum value
    -   Maximum value
    -   Average value \(not available for string, date, or date/time fields\)
4.  Select **OK**.

    The calculations appear below the last record in the column. If the list is grouped, in addition to the overall calculations at the bottom of the list, group calculations appear below the last record in each group.


**Parent Topic:**[List configuration](../concept/c_ListConfiguration.md)

