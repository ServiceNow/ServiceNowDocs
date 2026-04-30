---
title: Configure advanced conditions: crop process
description: Configure custom start and end conditions for your table configuration to define which part of the process should be included in the Process Mining project and made available for analysis.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up a table configuration, Create a project using Classic view, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure advanced conditions: crop process

Configure custom start and end conditions for your table configuration to define which part of the process should be included in the Process Mining project and made available for analysis.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

## Procedure

1.  Go to the **Advanced Condition** tab of your table configuration record.

    ![Crop process in table configuration](../image/table-config-classic.png)

2.  Select **Crop** from the **Condition type** list.

    Crop conditions allow you to configure a specific start and end condition from your process map, such as, specifying resolved as your process end state instead of closed. Another example is only discovering process from the first occurrence of the New state until the last occurrence of Resolved, thus leaving the Closed state out of the analysis.

3.  Select the plus symbol next to the **Start condition** field.

4.  In the **Create new process start condition** form, fill in the fields.

    For a description of the field values, see [Create new process start/end condition](../reference/process-start-condition.md).

5.  Select **Submit** to save the condition.

6.  To create an end condition, select the plus symbol next to the **End condition** field.

7.  In the **Create new process end condition** form, fill in the fields.

    **Note:** The fields and descriptions are identical to those for the **Create a new process start condition** form.

8.  Select **Submit** to save the condition.


## A configured process condition

In this example, a process end condition is configured when an incident record enters the `Work in progress` state. Because the **Occurrence\(s\) to match** field is set to `First only`, the condition only triggers the first time a record's state changes to `Work in progress`.

![Configured process start condition](../image/start-condition-example.png)

**Parent Topic:**[Set up a table configuration](po-table-configuration.md)

