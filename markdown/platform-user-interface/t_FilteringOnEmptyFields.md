---
title: Filtering on empty fields
description: Most filter operations do not return empty fields in their result set. You can create a filter that displays records with an empty field value in addition to records that match the initial filter conditions.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Condition builder, Create a condition statement using the condition builder, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Filtering on empty fields

Most filter operations do not return empty fields in their result set. You can create a filter that displays records with an empty field value in addition to records that match the initial filter conditions.

## About this task

For example, when viewing all records that are assigned to the Hardware group, to include records with an empty **Assignment group** field, complete the following steps.

## Procedure

1.  Create the filter condition **\[Assignment group\] \[is\] \[Hardware\]**.

    **Note:** This condition does not return those records where the **Assignment group** field is empty.

2.  Click **OR** next to the original filter condition.

3.  Create another filter condition of **\[Assignment group\] \[is empty\]**.

4.  Run the filter.


**Parent Topic:**[Condition builder](../concept/c_ConditionBuilder.md)

**Related topics**  


[Values for date/time fields](../concept/c_ValuesForDateTimeFields.md#)

[Comparing field values](../../../administer/navigation-and-ui/reference/r_ComparingFieldValues.md)

