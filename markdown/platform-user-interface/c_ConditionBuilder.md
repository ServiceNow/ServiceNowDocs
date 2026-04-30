---
title: Condition builder
description: A condition builder constructs a condition statement with a series of contextually generated fields. Condition builders are used in many operations, such as creating filters, administering surveys, and administering access control.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a condition statement using the condition builder, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Condition builder

A condition builder constructs a condition statement with a series of contextually generated fields. Condition builders are used in many operations, such as creating filters, administering surveys, and administering access control.

## Condition builder format

A condition consists of three parts:

-   Field: a choice list based on the table and user access rights. The choice list can include fields on related tables by dot-walking.
-   Operator: a choice list based on the field type. For example, in the Incident \[incident\] table, the greater than operator does not apply to the **Active** field but it does apply to the **Priority** field.
-   Value: a text entry field or a choice list, depending on field type. For example, in the Incident \[incident\] table, the **Active** field offers a choice list with the values **true**, **false**, and **empty**, while the **Short Description** field offers a text entry field.

The conditions display above lists in Core UI as a breadcrumb, summarizing what you have selected.

![An image of the condition builder breadcrumb above a list in Core UI.](../image/condition-builder-breadcrumb.png)

**Note:** The condition builder breadcrumb in Core UI list view can be truncated depending on the values of two system properties:

-   **glide.ui.breadcrumb\_max\_entries**: specifies the maximum number of items displayed in the breadcrumb, with a default of 10.
-   **glide.ui.export.choice\_list\_max\_characters**: specifies the maximum number of characters displayed for a choice list within the breadcrumb, with a default of 80.

For more information, see [KB1962280](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1962280).

## Condition builder actions

You can add a dependent condition by clicking **AND** or **OR** next to the condition. You can add a top-level condition by clicking **AND** or **OR** on the condition builder toolbar above the conditions. You can remove a condition by clicking the delete icon \(X\) next to the condition.

![Example AND condition.](../image/ExampleConditionActiveIsTrueAndCallerIsNotEmpty.png "Example AND condition in filter")

For an example of a scripted filter see the KB article [Creating dynamic JavaScript filters in reports](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0746219).

-   **[Filtering on empty fields](../task/t_FilteringOnEmptyFields.md)**  
Most filter operations do not return empty fields in their result set. You can create a filter that displays records with an empty field value in addition to records that match the initial filter conditions.
-   **[Values for date/time fields](c_ValuesForDateTimeFields.md#)**  
When you filter on fields of type date/time, such as the **Created** field on any task record, several time-related options are available, such as **Today**, **This week**, **Last 3 months**, and so on.
-   **[Comparing field values](../../../administer/navigation-and-ui/reference/r_ComparingFieldValues.md)**  
Field comparison allows users to evaluate equality between fields on the same table or on related tables by using operators in the condition builder.

**Parent Topic:**[Create a condition statement using the condition builder](../task/create-cond-state-using-cond-build.md)

**Related topics**  


[Operators available for filters and queries](../reference/r_OpAvailableFiltersQueries.md)

[OR conditions](../../using-lists/concept/c_UsingORConditions.md)

[Filters](../../using-lists/concept/c_Filters.md)

[Dot-walking to data in related tables](../../navigation/concept/c_DotWalking.md)

