---
title: Add related list conditions
description: Related list conditions allow you to include a relationship with another table in the filter. Related list conditions are supported in both List v3 and the Report interface.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Filters, Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Add related list conditions

Related list conditions allow you to include a relationship with another table in the filter. Related list conditions are supported in both List v3 and the Report interface.

## Before you begin

Role required: none

## About this task

You can optionally include conditions on the related table. For example, you can filter active problems with one or more related incidents that are in the **Canceled** state. Another example is to filter incidents with a breached service level agreement \(SLA\).

The List v3 filter contains two sections, one for the current table conditions and one for related lists conditions. You can include only one related table in the query, however, you can add multiple conditions for that table.

![Problem filter for open problems](../image/related-list-conditions-problem.png "Problem filter for open problems")

The easiest way to understand the parts of a related list condition is to use an example. The steps below use the example of open problems with some number of related incidents. You can perform these steps for any list view that supports List v3.

## Procedure

1.  For this example, navigate to **Problems** &gt; **Open**.

2.  Open the list filter and select the conditions for the current \(Problem\) table.

    The **\[State\] \[is\] \[Open\]** condition is already added.

3.  Select **RELATED LISTS CONDITIONS** to expand the section.

4.  From the choice list, select the table relationship to include in the query.

    For this example, select **Incident&gt;Problem**. You can select any table that you have access to view.

5.  To select a quantifier, select **Greater Than Or Equal To 1**.

    The Quantity popover opens.

    ![Related list conditions quantity](../image/problems-with-related-incidents.png)

6.  Select a quantity, enter number of records in the related table that must match, and then select**X** to close the popover.

    The default number is **1**. Following are descriptions and examples of each quantifier for this example.

    -   **Greater Than Or Equal To**: Returns problem records where the number of related incidents is greater than or equal to the number you enter. A value of **5** includes problems with five or more related incidents. Problem records with 4 or fewer incidents are not returned.
    -   **Greater Than**: Returns problem records that have more than this number of related incidents.
    -   **Less Than Or Equal To**: Returns problem records that have the number or fewer than the specified number of related incidents. A value of **1** includes problem records with one or no related incidents.
    -   **Less Than**: Returns problem records with fewer than the number of related incidents. A value of **1** returns problems with no related incidents.
    -   **Equal To**: Returns problems with this number of related incidents. A value of **5** includes problem records with exactly five related incidents.
    -   **None**: Returns problems that do not match the specified table relationship. A selection of **None** returns problems with no related incidents.
    -   **Between**: Returns problems with any number of related incidents that is between the two numbers you enter. **Between** values of **5** and **10** include problem records with 5, 6, 7, 8, 9, or 10 related incidents.
7.  Enter one or more conditions for the related table.

    Select **New Criteria** to add another condition.

    The following image shows the example of filtering for problem records with more than two related incidents that are critical priority.

    ![Filter for problems with more than two related critical incidents](../image/related-list-conditions-incident-filter.png)

    **Note:** You cannot perform a keyword search in a related table condition.

8.  Select **Run** to execute the filter query.


## Result

The breadcrumb displays **Related List condition...**. Open the filter to view the related list query statement.

![List breadcrumb and the related list condition query statement](../image/related-list-breadcrumb.png "List breadcrumb and the related list condition query statement")

**Note:** If List v3 is disabled for a list with a related list condition query in the default filter, the filter edit function is disabled. Remove the related list condition to enable list filter editing.

![Remove a related list condition in List v2 filter](../image/related-list-condition-v2-remove.png)

**Parent Topic:**[Filters](../../using-lists/concept/c_Filters.md)

**Related topics**  


[Create a filter in List](../../using-lists/task/t_CreatingFilters.md)

[OR conditions](../../using-lists/concept/c_UsingORConditions.md)

[Filter on multiple string values](../../using-lists/task/t_FilteringOnMultipleStringValues.md)

[Dynamic operators](../../using-lists/reference/r_UsingTheDynamicOperator.md)

