---
title: Configure advanced conditions
description: Configure custom start and end conditions for your table configuration to define which part of the process should be included in the Process Mining project and made available for analysis.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up a table configuration, Create a project using Classic view, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure advanced conditions

Configure custom start and end conditions for your table configuration to define which part of the process should be included in the Process Mining project and made available for analysis.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

## Procedure

1.  From the **Advanced Condition** tab of your table configuration record, select the plus symbol next to the **Process start condition** field.

    Advanced conditions allow you to configure a specific start and end condition from your process map, such as, specifying resolved as your process end state instead of closed. Another example is only discovering process from the first occurrence of the New state until the last occurrence of Resolved, thus leaving the Closed state out of the analysis.

    If you’ve already configured a start condition, you can use the reference icon to add the existing condition to the **Process start condition** field.

2.  In the **Create new process start condition** form, fill in the fields.

    For a description of the field values, see [Create new process start condition](../reference/process-start-condition.md).

3.  Select **Submit** to save the condition.

4.  To create an end condition, select the plus symbol next to the **Process end condition** field.

5.  In the **Create new process end condition** form, fill in the fields.

    **Note:** The fields and descriptions are identical to those for the **Create a new process start condition** form.

6.  Select **Submit** to save the condition.


## A configured process condition

In this example, a process end condition is configured when an incident record enters the `Work in progress` state. Because the **Occurrence\(s\) to match** field is set to `First only`, the condition only triggers the first time a record's state changes to `Work in progress`.

![Configured process start condition](../image/start-condition-example.png)

**Parent Topic:**[Set up a table configuration](po-table-configuration.md)

