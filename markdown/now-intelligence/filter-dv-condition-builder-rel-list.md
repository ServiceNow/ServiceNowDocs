---
title: Related list conditions example
description: Related list conditions enable you to include a relationship with another table in the filter.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Filter data visualizations with the condition builder, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Related list conditions example

Related list conditions enable you to include a relationship with another table in the filter.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

You can optionally include conditions on the related table. For example, you can filter active problems with one or more related incidents that are in the **Canceled** state. Another example is to filter incidents with a breached service level agreement \(SLA\).

The condition builder contains two sections, one for the current table conditions and one for related lists conditions. You can include only one related table in the query, however, you can add multiple conditions for that table.

The easiest way to understand the parts of a related list condition is to use an example. The following steps use the example of open problems with some number of related incidents.

## Procedure

1.  For this example, create a visualization on the Problem \[problem\] table.

2.  Open the filter and select **Add custom conditions**.

    Configure the condition **\[State\] \[is not one of\] \[Resolved, Closed\]**.

3.  Select the **Related list conditions** tab.

4.  Select the operator **Greater than or equal to** and the Value `1`.

    The default number is **1**. Following are descriptions and examples of each operator for this example.

    -   **Greater Than Or Equal To**: Returns problem records where the number of related incidents is greater than or equal to the number you enter. A value of **5** includes problems with five or more related incidents. Problem records with 4 or fewer incidents are not returned.
    -   **Greater Than**: Returns problem records that have more than this number of related incidents.
    -   **Less Than Or Equal To**: Returns problem records that have the number or fewer than the specified number of related incidents. A value of **1** includes problem records with one or no related incidents.
    -   **Less Than**: Returns problem records with fewer than the number of related incidents. A value of **1** returns problems with no related incidents.
    -   **Equal To**: Returns problems with this number of related incidents. A value of **5** includes problem records with exactly five related incidents.
    -   **None**: Returns problems that do not match the specified table relationship. A selection of **None** returns problems with no related incidents.
    -   **Between**: Returns problems with any number of related incidents that is between the two numbers you enter. **Between** values of **5** and **10** include problem records with 5, 6, 7, 8, 9, or 10 related incidents.
5.  From the **Related list**, select the table relationship to include in the query.

    For this example, select **Incident&gt;Problem**. You can select any table that you have access to view.

6.  Enter one or more conditions for the related table.

    Select a field, an operator, and \(if required\) a value, to add another condition.

    The following image shows the example of filtering for problem records with more than two related incidents that are critical priority.

    ![Condition builder's related list conditions tab with the operator, related list, and additional conditions filled in.](../../par-for-workspace/image/related-list-conditions-incident-filter-2.png)

    **Note:** You cannot perform a keyword search in a related table condition.

7.  Select **Run** to execute the filter query.

8.  Select Save as predefined condition to make this filter available to others reporting on this table.


## Result

The Preview record list shows the records that match the conditions you've defined. Select **Add this source** to use the data source with the applied conditions in your visualization.

**Parent Topic:**[Filter data visualizations with the condition builder](filter-dv-condition-builder.md)

