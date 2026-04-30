---
title: Create a log source configuration
description: Regulate and set filters on the logs to be forwarded by creating a log source configuration.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Administering Log Export Service \(LES\), Log Export Service \(LES\), Platform Security]
---

# Create a log source configuration

Regulate and set filters on the logs to be forwarded by creating a log source configuration.

## Before you begin

Role required: admin or sn\_logstoanalytics.admin

## Procedure

1.  Navigate to **All** &gt; **Log Export Service \(LES\)** &gt; **Sources**.

    A list of log sources shows up.

2.  Select **New** if you want to create a new log source.

    You can also select an existing log source if you want to modify it.

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

Table

</td><td>

Selection of table for table type logs.**Note:** This field is visible only when you select Table as the Source Type.

</td></tr><tr><td>

Log Level

</td><td>

A set of standard logging levels that can be used to control logging output.You have the following log level to select from:

-   INFO
-   WARN
-   ERROR
**Note:** Following convention, each level will forward logs of equal or greater severity. For example, if you select WARN as the log level, it forwards both WARN and ERROR logs but not INFO logs.

**Note:** This field is visible only when one of the following conditions is met.

-   When you select Node Log as the Source Type
-   When you select Table as the Source Type and the table is syslog


</td></tr><tr><td>

Accepts

</td><td>

Specifies the format in which the logs are forwarded to Hermes. They can either be sent as JSON or as plain text.

</td></tr><tr><td>

Topic

</td><td>

Select or create a topic for the source type and table type.

**Note:** This field is visible only when one of the following conditions is met.

-   When you select Node Log as the Source Type
-   When you choose Table as the Source Type and then select any table other than syslog

**Note:** If you choose sys\_audit as the Table and Log Table as Filter Type, the Topic field doesn't show up.

If you are creating a new topic, fill up the following fields.

-   Name: Name of the topic you are creating
-   Application ID: Enter sn\_logstoanalytics
-   Namespace: Enter Default Namespace
-   Partition: The partition field of a topic in Hermes refers to the partitions into which the topic's data is divided. It plays a key role in scalability and parallelism
See [Create source type and multi topics in the LES source table](les-multi-topics-v2.md) for more information.

</td></tr><tr><td>

Filter Type

</td><td>

Conditions to forward logs selectively.**Note:** This field is visible only if you select sys\_audit as the table.

</td></tr><tr><td>

Active

</td><td>

Option to activate the new source type.

</td></tr></tbody>
</table>4.  Select **Submit** to save the new log source.

    The list of log sources shows up.

5.  Select the log source you just created.

6.  Review the information in the Source Topics related list for the log sources and add filters accordingly.

    You can also create a new filter type and assign it to an existing or a new topic by selecting **New**. Proceed with the next step to create a filter type.

    **Note:** The Source Topics related list shows up only if one of the following conditions are fulfilled:

    -   If you choose syslog as the table and submit the source configurations.
    -   If you select sys\_audit as the table and select Log Table in the Filter Type field.
    If you have selected sys\_audit as the Table, information regarding only Log Table and Topic is displayed in the Source Topics related list. You can view filter information only when you select syslog as Table.

    **Note:** By default, you can create only upto ten filter types. If you need to change the number of filter types, you can add the glide.log.forwarding.syslog.topics.limit property and modify the default value associated with it.

7.  Create a filter type and assign it to a topic.

    1.  Select **New** to create a new filter type. The Source Topics form shows up.
    2.  Select one of the following Filter Type options.

        -   All
        -   Application Family
        -   Package
        -   Scope
        **Note:** This field is visible only when you select syslog as the table.

    3.  Select the required table in the Log Table field.

        **Note:** This field is visible only when you select sys\_audit as the table.

    4.  Select the lookup icon in the Topic field.

        **Note:** You can select an existing Kafka topic from the list. You can also create a new Kafka topic by selecting **New** in the Kafka Topics list. See [Create source type and multi topics in the LES source table](les-multi-topics-v2.md) to create a new Kafka topic.

    5.  Select **Submit** on the Source Topics form.
8.  View the recently created log table and its corresponding topic in the Source Topics related list.


-   **[Create source type and multi topics in the LES source table](les-multi-topics-v2.md)**  
Consume logs for each source type by assigning either the same topic or different topics for different source types. You can now leverage the option of customized selection of specific topics for different log sources during the debugging process, without impacting the other log tables.

**Parent Topic:**[Administering Log Export Service \(LES\)](../concept/les-administer.md)

