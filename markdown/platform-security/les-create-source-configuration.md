---
title: Create a log source configuration
description: Regulate and set filters on the logs to be forwarded by creating a log source configuration.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Log Export Service \(LES\), Platform Security]
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
</table>4.  Select **Submit** to create a new source configuration.


-   **[Create multi topics in the LES source table](les-multi-topics.md)**  
Consume messages for each source type independently by creating a unique topic per source type.

**Parent Topic:**[Log Export Service \(LES\)](../concept/les-landing-page.md)

