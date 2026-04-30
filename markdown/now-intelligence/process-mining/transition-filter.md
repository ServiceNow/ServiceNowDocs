---
title: Configure advanced conditions: transition filter
description: Activity transitions filtering enables you to get closer views of the different routes that records go through.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-03-06"
reading_time_minutes: 1
breadcrumb: [Set up a table configuration, Create a project using Classic view, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure advanced conditions: transition filter

Activity transitions filtering enables you to get closer views of the different routes that records go through.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

Use transition filters to filter records for executed workflows that transition through specified activities. This helps you investigate corresponding values more closely.

## About this task

You can apply a transition filter in two ways:

-   By creating a specific condition manually
-   By applying transition filter on a pre-defined filter

## Procedure

1.  Go to the **Advanced Condition** tab of your table configuration record.

    ![Crop process in table configuration](../image/table-config-classic.png)

2.  Select **Transition** from the **Condition type** list.

3.  Select the plus symbol next to the **Start condition** field.

4.  In the **Create new process start condition** form, fill in the fields.

    For a description of the field values, see [Create new process start/end condition](../reference/process-start-condition.md).

5.  Select **Submit** to save the condition.

6.  Select a value in the **Relation** field.

7.  To create an end condition, select the plus symbol next to the **End condition** field.

8.  In the **Create new process end condition** form, fill in the fields.

    **Note:** The fields and descriptions are identical to those for the **Create a new process start condition** form.

9.  Select **Submit** to save the condition.


**Parent Topic:**[Set up a table configuration](po-table-configuration.md)

