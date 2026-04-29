---
title: Comparing field values
description: Field comparison allows users to evaluate equality between fields on the same table or on related tables by using operators in the condition builder.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Condition builder, Create a condition statement using the condition builder, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Comparing field values

Field comparison allows users to evaluate equality between fields on the same table or on related tables by using operators in the condition builder.

Also, you can compare date type fields to determine whether the values are within a certain range of each other. For example, you can compare the planned start date of a task to the actual start date. You can use field comparisons in a list view and to generate reports.

The primary function of field comparison is evaluating whether two fields on a record or related record have identical values. For example, you can create a filter to display all incidents whose **Caller** field references the same user record as the **Closed by** field.

## Available operators

Field comparison provides several filter operators for comparing field values.

-   **\[is same\]** if two field values are the same, evaluates to true.
-   **\[is different\]** if two field values are not the same, evaluates to true.
-   **\[is less than\]** if two date values are within a user-defined range of each other, evaluates to true.
-   **\[is more than\]** if two date values are not within a user-defined range of each other, evaluates to true.

## Comparing choice list values

Field comparison compares the dictionary **Value** field of a choice list, not the **Label** value. For example, a high priority incident has a priority value of **1**, not **1 - High**. To find the **Value** of a choice, right-click the field label and select **Configure Dictionary**. The **Choices** related list shows the **Value** for each choice.

## Comparing empty fields

By default, most filter operations do not return empty fields in their result set. To include records with empty fields in a result set, add a filter condition for the left operand with an operator of **\[is empty\]**. For more information, see [Filtering on empty fields](../../../use/common-ui-elements/task/t_FilteringOnEmptyFields.md).

## Using operators and operands

When comparing fields, the two fields being compared are called the left operand and right operand. The type of field selected in the left operand, and the operator selected, determine which right operands are available. When using the **\[is same\]** or **\[is different\]** operators, the right operand choices include only fields of the same field type, such as **String** or **Integer**, as the left operand.

For example, a filter on the Task \[task\] table with a left operand of **\[Opened by\]** and an operator of **\[is same\]**, only allows you to choose user reference fields, such as the **\[Closed by\]** field, in the right operand.

The **\[is more than\]** and **\[is less than\]** operators are only available with date type fields.

This example filter returns records where the user who opened the record also closed the record.

![Example filter.](../image/ExampleFilter.png "Example filter")

## Comparable fields

Field comparison supports the comparison of several fields. The fields that are comparable include the following types:

-   String, choice, integer, and boolean fields: Return true if both values match.
-   Reference fields: Return true if both reference fields refer to the same record.
-   Date and time fields: Can match date values based on hour, day, week, month, quarter, or year. Also, you can evaluate whether two dates fall within a certain range of each other.

**Note:** Field comparison does not support journal, keyword, script, duration, list, or HTML fields.

## Comparing dates

Date comparison allows you to evaluate equality between two components of the date, such as the hour of the day or the date within a month. Also, you can evaluate if two dates fall within a certain range of each other.

Date comparisons are based on the active user's time zone. For example, as a user in the PST time zone, a filter of **\[Created\] \[is same\] \[Day\] as \[Closed\]** evaluates true for an incident created at 6 AM PST and closed at 3:00 PM PST as both times are within the same day. However, a user in the GMT time zone would not see this same incident record in response to the example filter; in GMT those times do not fall on the same date.

You can [Evaluate equality between date values](../task/t_EvaluatingEqualityBetweenDates.md) and you can evaluate unequal dates within a range.

## Evaluate unequal dates within a range

You can compare unequal date field values by evaluating whether two dates fall within a certain range of each other. For example, you can create a filter of **\[Created on\] \[is more than\] \[3\] \[Months\] \[before\] Closed\]** to display all records that were created at least three months before they were closed. The numerical value specified, such as the value **3** in the example, must be an integer of no more than two digits. For evaluations of differences larger than 99 units, select a less granular unit of time, such as **Months** instead of **Days**.

![Unequal dates field comparison.](../image/UnequalDatesFieldComparison.png "Unequal dates field comparison")

|Choice field|Date Comparison Choices|
|------------|-----------------------|
|Operator|is more than, is less than|
|Unit of time|Hours, Days, Weeks, Months, Quarters, Years|
|Relative position of dates|before, after, before or after|

-   **[Evaluate equality between date values](../task/t_EvaluatingEqualityBetweenDates.md)**  
Date comparison evaluates a match for one of several date increments.

**Parent Topic:**[Condition builder](../../../use/common-ui-elements/concept/c_ConditionBuilder.md)

**Related topics**  


[Filtering on empty fields](../../../use/common-ui-elements/task/t_FilteringOnEmptyFields.md)

[Values for date/time fields](../../../use/common-ui-elements/concept/c_ValuesForDateTimeFields.md#)

