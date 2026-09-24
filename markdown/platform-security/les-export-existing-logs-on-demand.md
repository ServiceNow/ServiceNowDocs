---
title: Export existing logs on demand
description: Replay historical log data from a supported table to a Hermes topic by creating and starting a Backfill Run. Use this process to export logs from a specific time range for analysis or archival.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/les-export-existing-logs-on-demand.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 3
breadcrumb: [Administer, Log Export Service \(LES\), Platform Security]
---

# Export existing logs on demand

Replay historical log data from a supported table to a Hermes topic by creating and starting a Backfill Run. Use this process to export logs from a specific time range for analysis or archival.

## Before you begin

Role required: admin or sn\_logstoanalytics.admin

Before you begin:

-   Verify that the source table is present in the LES Sources allow-list.
-   Verify that the target topic belongs to the LES application scope.

## About this task

By default, Log Export Service forwards a copy of log events to Hermes Messaging Service as those events are generated. Use a backfill run to replay historical rows from a supported log table for a bounded time range.

Each Backfill Run replays rows from one source table into one Hermes Messaging Service topic, in ordered batches. Only one active run per table is allowed at a time. After you start a run, its configuration is locked to prevent accidental edits.

## Procedure

1.  Navigate to **All** &gt; **Log Export Service \(LES\)** &gt; **Export Historical Data**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table><tbody><tr><td>

**Field**

</td><td>

**Description**

</td></tr><tr><td>

Name

</td><td>

Name of the Backfill Run.

</td></tr><tr><td>

Table

</td><td>

Log source table whose historical rows you want to replay.

 For more information on supported tables, see [Log Sources.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-log-sources-export.md)

</td></tr><tr><td>

Log level

</td><td>

A set of standard logging levels that can be used to control logging output. Each level forwards logs of equal or greater severity.

 Log level options:

 -   INFO - Forwards all logs
-   WARN - Forwards warnings and errors
-   ERROR - Forwards errors only
 **Note:** This field appears only when you select Table as the Source Type and the table is syslog.

</td></tr><tr><td>

Topic

</td><td>

Reference to the Hermes Messaging Service topic that the run publishes to. Select an existing topic, or create a topic through the lookup icon. For more information on creating a topic, see [Create source type and multi topics in the LES source table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-multi-topics-v2.md).

</td></tr><tr><td>

Range Start

</td><td>

Earliest timestamp of the historical window to replay. Rows with a timestamp on or after Range Start are included.

</td></tr><tr><td>

Range End

</td><td>

Latest timestamp of the historical window to replay. Range End can be any time up to now and must be equal to or later than Range Start.

</td></tr><tr><td>

Max Rows

</td><td>

Optional cap on the total number of rows the run publishes. Leave blank to publish all rows in the range.

</td></tr><tr><td>

Batch Size

</td><td>

Number of rows the worker publishes per batch. The default is 1000.

</td></tr><tr><td>

Throttle Ms

</td><td>

Optional wait time, in milliseconds, between batches. The default is 0. Increase this value only when the source instance is under heavy load. Typical non-zero values range from 10 to 100 milliseconds.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the Backfill Run is active.

</td></tr><tr><td>

Status

</td><td>

Current state of the run: **New**, **Queued**, **Running**, **Completed**, **Error**, or **Cancelled**. A background scheduler picks up queued runs approximately once every minute.

</td></tr><tr><td>

Status Detail

</td><td>

Plain-language summary of the current state.

</td></tr><tr><td>

Rows Published

</td><td>

Number of rows successfully published to the topic since the run started.

</td></tr><tr><td>

Rows Failed

</td><td>

Number of rows that failed to publish.

</td></tr><tr><td>

First Timestamp Sent

</td><td>

Timestamp of the first row published in this run. Set once when the run starts and does not change.

</td></tr><tr><td>

Last Timestamp Sent

</td><td>

Timestamp of the most recent row published. Updates as the run progresses.

</td></tr><tr><td>

First Sys Id Sent

</td><td>

Sys ID of the first row published in this run.

</td></tr><tr><td>

Last Sys Id Sent

</td><td>

Sys ID of the most recent row published.

</td></tr><tr><td>

Resolved Topic

</td><td>

Reference to the topic record that the **Topic** field resolved to.

</td></tr></tbody>
</table>4.  Select **Submit**.

    The **Status** field is set to **New**.

5.  Open the record and select **Start**.

    The **Status** field changes to **Queued** and then to **Running** when the scheduled worker picks it up. All input fields become read-only.

6.  To stop a run that has not finished, select **Cancel** while the **Status** is **Queued** or **Running**.


## Result

When the run finishes, the **Status** field is set to **Completed** and the **Status Detail** field displays a summary such as "Backfill completed: forwarded 12,345 rows from syslog." If the run stops because of an error, the **Status** field is set to **Error** and the **Status Detail** field describes the cause.

You can also verify that logs are published to the topic using the Hermes topic inspector. For more information, see [View a message in a Hermes topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/view-messages-hermes-topic.md).

**Parent Topic:**[Administering Log Export Service \(LES\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-administer.md)

