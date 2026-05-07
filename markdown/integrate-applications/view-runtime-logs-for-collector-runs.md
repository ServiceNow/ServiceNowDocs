---
title: View runtime logs for collector runs
description: Access execution logs and download detailed log files for metadata collector runs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Running metadata collectors, Data Catalog, Workflow Data Fabric]
---

# View runtime logs for collector runs

Access execution logs and download detailed log files for metadata collector runs.

## Before you begin

Role required: connection\_admin

## About this task

Runtime logs provide visibility into collector execution progress, discovered metadata, and any errors or warnings that occurred during the collection process. Use these logs to monitor collection health, troubleshoot failed runs, verify that expected data assets were discovered, and diagnose connectivity or permission issues.

The execution run page displays real-time status information and a searchable table of log entries organized by severity level \(Info, Warning, Error\). For advanced troubleshooting or detailed analysis, you can download complete log files containing granular execution details and the raw collected metadata in RDF format.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub icon in the left sidebar.

3.  Select **Connectors**.

4.  Select **Metadata collector**.

5.  Select a metadata collector for which you want to review the logs.

6.  Access the runtime logs.

    -   To view the most recent run logs, select **Runtime logs** from the form context menu.

    -   To view logs from previous runs, select **Previous runs** and then select a specific execution run from the list.

7.  Review the execution details.

    The execution run page displays:

    -   Current Phase: Status of the collector run \(COMPLETED, FAILED, IN PROGRESS\)
    -   Start time and End time: Timestamp information
    -   Percent Complete: Progress percentage
    -   State: Overall execution state
    -   Configuration: Associated collector configuration name
8.  Review the execution logs table.

    Scroll to the **Execution logs** section to view log entries. The table displays:

    |Column|Description|
    |------|-----------|
    |Level|Log severity \(Info, Warning, Error\)|
    |Logged At|Timestamp when the log entry was created|
    |Message|Log message describing the event or issue|
    |Exception Class Name|Type of exception if an error occurred|
    |Exception Message|Detailed error message|
    |Recommended Action|Suggested steps to resolve the issue|

9.  Download detailed log files for advanced troubleshooting.

    In the **Manage Attachments** section, select the download link next to the log file name. Two types of log files are available:

<table id="table_log_files"><thead><tr><th>

File Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

execution\_projection\_\*.log

</td><td>

Detailed execution logs containing timestamped entries about: -   Log projection start and completion status
-   Discovered data asset types and counts \(for example, tables, columns, views\)
-   Attribute projection processing for each data asset type
-   Mapping information between source metadata and catalog tables
-   SPARQL queries used for data extraction
-   Processing statistics including error counts
 Use this file to understand what the collector discovered, how data assets were mapped, and identify processing issues

</td></tr><tr><td>

catalog-\*-results.nt

</td><td>

Raw collected metadata in N-Triples RDF format containing: -   Collector execution metadata \(start time, end time, execution properties\)
-   System environment information \(OS, architecture, version\)
-   Complete data asset definitions using Open KOS schema URIs
-   Relationships between discovered data assets
-   Technical metadata for all collected assets
 This machine-readable format is primarily for advanced troubleshooting and integration scenarios. Use RDF tools to parse and analyze this data

</td></tr></tbody>
</table>
## Result

Use the logs to identify collection issues, verify data asset discovery, and troubleshoot failed runs. Focus on Warning and Error level messages for troubleshooting. Download detailed log files when you need to share diagnostic information with support or perform deep analysis of collection behavior.

**Parent Topic:**[Running metadata collectors](../concept/run-metadata-collectors-dc.md)

