---
title: Schedule a CMDB query
description: Schedule a saved CMDB query to run once at a scheduled time or on a recurring schedule, and to email the query results to specified users.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Schedule a CMDB query

Schedule a saved CMDB query to run once at a scheduled time or on a recurring schedule, and to email the query results to specified users.

## Before you begin

A saved CMDB query that was built in the CMDB Query Builder must exist.

Role required: cmdb\_query\_builder

## About this task

The query results are attached to the email as a file in the specified format. The maximum number of result rows that can be attached is determined by the **glide.cmdb.query.max\_results\_limit** system property \(10,000 by default\).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Query Builder** and then select a saved query.

2.  Select **Create Schedule** and then fill in the form.

<table id="table_vbw_g3y_rw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Query

</td><td>

The query to run.

</td></tr><tr><td>

Users

</td><td>

Users who should receive query results email.

 To receive emails, users must have an Email address defined and have Notifications set to Enable in their user records.

</td></tr><tr><td>

Groups

</td><td>

Groups to email the query results to.

</td></tr><tr><td>

Zip output

</td><td>

Indicates whether the report should be sent as a zip file.

</td></tr><tr><td>

Active

</td><td>

Indicates whether to run the query according to the specified schedule.

</td></tr><tr><td>

Run

</td><td>

Frequency for running the query.

</td></tr><tr><td>

Time

</td><td>

Time of day to run the query.

</td></tr><tr><td>

Conditional

</td><td>

Indicates whether to display the **Condition** field, which allows you to specify conditions under which the query runs.

</td></tr><tr><td>

Omit if not records

</td><td>

Indicate whether to distribute email if the query returns zero results.

</td></tr><tr><td>

Email addresses

</td><td>

Email addresses of users who should receive the email but who are not in the system.

</td></tr><tr><td>

Subject

</td><td>

Text that appears in the subject line of the distribution email.

</td></tr><tr><td>

Introductory message

</td><td>

Additional message that is delivered with the query results.

</td></tr><tr><td>

Condition

</td><td>

User-created script that checks for certain conditions to be true before running the query.

 This field is visible only when **Conditional** is checked.

</td></tr><tr><td>

Type

</td><td>

File format to use for the query results.**Note:** [Configure the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md) to add this field to the form.

</td></tr></tbody>
</table>
