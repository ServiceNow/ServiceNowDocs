---
title: Add an additional group by or stack by
description: You can configure a report to let users adjust its grouping and stacking.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Add an additional group by or stack by

You can configure a report to let users adjust its grouping and stacking.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## About this task

Configure **Additional group by** and **Stack by** choices that users can select when viewing the chart. Additional group bys can be added to any report that supports group bys \(such as bar or pie\) and to list reports as columns. When you configure an additional group by to a bar or horizontal bar, it is also added as an additional stack by. You can add variables and variable groups as additional group bys.

**Note:**

-   Available **Stack by** fields are limited to catalog variables, reference fields, choice lists, and boolean values. Date/time, integer, long, string, list, and text fields cannot be used as stacked fields.
-   You can see choices in the **Additional group by** list that do not appear in the main **Group by** list. The report does not support grouping or stacking by the extra fields you see. Unlike the main **Group by** choices, the **Additional group by** fields are not filtered. If you select an unsupported field, it has no effect.
-   When you select an Additional Group by field on a report and then export that report, the export shows only the initial group by set on the report, not the additional group by that you have selected.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Select a report.

3.  On the Configure tab, select **Additional group by**.

    ![Additional group by example](../image/additional-group-by-stack-by.png)

4.  Move one or more fields to the **Selected** list.

5.  Select a **Stack by** field used to show the relationship of individual items from the selected field to the whole.

    For example, group a bar chart of incidents by **Category** and stack by **Priority**. The viewer can then determine at a glance the proportion of high, medium, and low priority issues for each category.

    Users viewing the report can select one of these fields to group or stack the report data. The report **Group by** and **Stack by** field values are the default choices.

    **Note:** Only bar and horizontal bar reports use stacked data. Other report types allow only grouping.

6.  Arrange the fields in the **Selected** column in the order you want them to appear to users.![Additional group by - ordering example](../image/additional-group-by-stack-by-order.png)

7.  Select **OK**.

8.  Select **Save**.


**Parent Topic:**[Advanced Core UI reporting topics](../concept/c_AdvancedReporting.md)

