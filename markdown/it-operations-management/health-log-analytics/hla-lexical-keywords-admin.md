---
title: Add, edit, or delete Health Log Analytics lexical keywords
description: Manage the keywords that Health Log Analytics looks for in your log data.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Influencing anomaly detection with lexical keywords, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Add, edit, or delete Health Log Analytics lexical keywords

Manage the keywords that Health Log Analytics looks for in your log data.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## About this task

In log data, terms like "crash" or "failed" are called lexical keywords because they indicate issues that can merit attention. When text in log data for a source matches a lexical keyword that exceeds a specified count threshold, the system identifies an anomaly and generates an alert.

**Important:** A lexical keyword differs from a key in a `key:value` pair in a log line. For example, Hostname is a key that takes on a value: the name or IP address of the host. In contrast, a keyword like Failed is important by itself and does not take on a value.

The application comes with many default global keywords. You can add, edit, and delete global keywords or phrases. These keywords apply to all source types.

**Note:** To add a specified keyword that is associated with a specific source type, see [Configure source type capabilities](hla-source-types.md).

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Log Anomaly Detection** &gt; **Lexical Keywords**.

    By default, the Lexical Keywords table lists only global keywords.

2.  Add a global keyword.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_z5c_ycf_r4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name for the keyword.

</td></tr><tr><td>

Regular expression

</td><td>

Regular expression \(regex\) that defines matches.

</td></tr><tr><td>

Exact match

</td><td>

Option to make Health Log Analytics match the exact regex. For example, 'NullPointerException' in a message would not match the regex 'exception'.This field is automatically set to **True**.

</td></tr><tr><td>

Case-sensitive

</td><td>

Option to make Health Log Analytics look for a case-sensitive match of the regex. This field is automatically set to **False**.

</td></tr><tr><td>

Range of analysis

</td><td>

Range of sources types where Health Log Analytics looks for the keyword in the log data. Choices are as follows:-   **All source types**
-   **Specified source type**


</td></tr><tr><td>

Excluded source types

</td><td>

Source types that are not associated with the keyword. Health Log Analytics does not look for the keyword in the log data of these source types.

</td></tr></tbody>
</table>    3.  Select **Submit**.

3.  Edit a global keyword.

    1.  Click the keyword that you want to edit in the list.

    2.  On the form, edit the relevant fields.

    3.  Select **Update**.

4.  Delete one or more global keywords.

    1.  Select the rows of the keywords that you want to delete.

    2.  From the Actions on selected rows list at the bottom of the page, select **Delete**.

    3.  Select **OK**.


**Parent Topic:**[Influencing anomaly detection with lexical keywords](../concept/hla-log-anomaly-detection.md)

**Related topics**  


[View the lexical keywords that generate alerts](../../health-log-analytics-operator/task/hla-op-lexical-keywords-manage.md)

