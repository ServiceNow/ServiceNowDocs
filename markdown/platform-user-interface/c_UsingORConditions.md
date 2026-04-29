---
title: OR conditions
description: The condition builder uses two different types of OR conditions: top-level and dependent.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Filters, Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# OR conditions

The condition builder uses two different types of OR conditions: top-level and dependent.

Using a dependent OR condition, you can specify alternative criteria to a single operation. Dependent OR conditions work in the manner A and \(B or C\). When you have an OR condition in the query, the magnifying glass is no longer available. The conditions you put in the quick search headers are ANDed together. Having an OR makes it ambiguous as to where the new condition should go, for example before the OR, or after the OR.

For example, to return a list of all unassigned problem and incident records from the Task table, create a filter with a dependent OR on the **Number** field.

**\[Assigned to\] \[is\] \[empty\]** AND **\[Number\] \[begins with\] \[PRB\]** OR **\[Number\] \[begins with\] \[INC\]**.

![Dependent OR condition](../image/DependentOR.png "Dependent OR")

A top-level OR condition allows you to display the results of multiple filter criteria in a single list. Top level OR conditions work in the manner \(A and B\) or \(C and D\).

For example, to return a single list of all active incidents with a category of hardware, and all inactive incidents with a category of software, create two condition sets separated by a top-level OR condition.

-   **\[Active\] \[is\] \[true\]** AND **\[Category\] \[is\] \[Hardware\]**
-   Top level OR condition
-   **\[Active\] \[is\] \[false\]** AND **\[Category\] \[is\] \[Software\]**

![Top level OR condition](../image/TopLevelOR.png "Top level OR")

Top-level and dependent OR conditions can be used together. Filters using both types of OR conditions work in the manner \(A or B\) or \(C or D\). By mixing AND conditions with top-level and dependent OR conditions, you can create very specific filters.

**Parent Topic:**[Filters](c_Filters.md)

**Related topics**  


[Create a filter in List](../task/t_CreatingFilters.md)

[Add related list conditions](../../using-lists-v3/task/create-related-list-query.md)

[Filter on multiple string values](../task/t_FilteringOnMultipleStringValues.md)

[Dynamic operators](../reference/r_UsingTheDynamicOperator.md)

