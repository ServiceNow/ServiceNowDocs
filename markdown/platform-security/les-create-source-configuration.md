---
title: Create a log source configuration
description: Regulate and set filters on the logs to be forwarded by creating a log source configuration.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Log Export Service \(LES\), Platform Security]
---

# Create a log source configuration

Regulate and set filters on the logs to be forwarded by creating a log source configuration.

## Before you begin

Role required: admin or sn\_logstoanalytics.admin

## Procedure

1.  Navigate to **All** &gt; **Log Export Service**.

    A list of source configurations shows up.

2.  Select **New** if you want to create a new source configuration.

    You can also select an existing source configuration if you want to modify it.

    The Source form shows up.

3.  On the form, fill up the fields.

<table id="table_ph5_fns_xjb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Type

</td><td>

Types of log sources-   Node Log
-   Table
See [Log sources](../concept/les-log-sources-export.md) for more information.

</td></tr><tr><td>

Log Level

</td><td>

A set of standard logging levels that can be used to control logging output. Following convention, each level will forward logs of equal or greater severity.**Note:** This field is visible only when one of the following conditions is met.

-   When you select Node Log as the Source Type
-   When you select Table as the Source Type and the table is syslog


</td></tr><tr><td>

Accepts

</td><td>

Specifies the format in which the logs are forwarded to Hermes. They can either be sent as JSON or as plain text.

</td></tr><tr><td>

Table

</td><td>

Selection of table for table type logs.**Note:** This field is visible only when you select Table as the Source Type.

</td></tr><tr><td>

Filter Type

</td><td>

Conditions to forward logs selectively.**Note:** This field is visible only if you select either syslog or sys\_audit as the table.

</td></tr></tbody>
</table>4.  Review the Source Topics related list details.

    You can review each of the log tables and can create its own topics.

    **Note:** The related list is visible only if you select Log Table in the Filter Type field.

    The topic name is not auto-populated, and you can either select or create its own topics.

5.  Select a topic for the log table.

    You can either select an existing topic or can create a new topic for a log table.

    1.  Select **New** to create a new source topic for a log table. The Source Topics form shows up.
    2.  Select the required table in the Log Table field.
    3.  Select the lookup icon in the Topic field.

        **Note:** You can select an existing topic from the list. You can also create a new topic by selecting **New** in the Kafka Topics list. See [Create source type and multi topics in the LES source table](les-multi-topics-v2.md) to create a new Kafka topic.

    4.  Select **Submit** on the Source Topics form.
6.  View the recently created log table and its corresponding topic in the Source Topics related list.

7.  Select **Submit** to create a new source configuration.


-   **[Create source type and multi topics in the LES source table](les-multi-topics-v2.md)**  
Consume logs for each source type by creating multiple topics per source type. You can now leverage the option of customized selection of specific topics for different log sources during the debugging process, without impacting the other log tables.

**Parent Topic:**[Administering Log Export Service \(LES\)](../concept/les-administer.md)

