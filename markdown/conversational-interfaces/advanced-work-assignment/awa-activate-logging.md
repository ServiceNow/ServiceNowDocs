---
title: Enable logging for Advanced Work Assignment
description: Enable logging to monitor AWA routing and assignment.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Enable logging for Advanced Work Assignment

Enable logging to monitor AWA routing and assignment.

## Before you begin

Role required: maint

## Procedure

1.  In the navigation filter, enter `sys_logger_configuration.list`.

2.  On the Logger Configurations screen, select **New**.

3.  On the New record screen, fill out the fields:

<table id="table_xyj_bnv_vrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Logger Name

</td><td>

Name of logger that this configuration applies to. This should be set to `com.snc.awa`.

</td></tr><tr><td>

Application

</td><td>

This field defaults to `Global` and cannot be changed.

</td></tr><tr><td>

Active

</td><td>

Option to activate logging.

</td></tr><tr><td>

Additive

</td><td>

Option to use the new logging in addition to any existing logging. This should be set to `false`.

</td></tr><tr><td>

Level

</td><td>

Type of errors that should be logged: -   FATAL - errors that cause the service to shut down \(status 0\).
-   ERROR - non-fatal service error messages.
-   WARN - warning messages indicating potential issues.
-   INFO - informational messages representing service actions.
-   DEBUG - detailed service operation messages which help troubleshoot issues.
-   TRACE - very detailed service operation messages which help troubleshoot issues.
-   ALL - all errors should be logged.
This should be set to `INFO`.

</td></tr><tr><td>

Filters

</td><td>

Enter any filters and their values that you want applied to the results.

</td></tr><tr><td>

Destination

</td><td>

Where the format log is sent. This should be set to `Database`.

</td></tr><tr><td>

Layout

</td><td>

Layout format that should be applied to the logs.

</td></tr></tbody>
</table>4.  Select `Submit`.

    Logging for the AWA assignment engine is enabled in the syslog table.

5.  To view the system log, navigate to **System Logs** &gt; **System Log** &gt; **All**.


