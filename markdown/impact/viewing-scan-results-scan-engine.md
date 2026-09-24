---
title: View scan results for Scan Engine
description: You can view scans in real-time as they run or after they're completed. 
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/viewing-scan-results-scan-engine.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Understand scan results and findings, Prevent and resolve technical debt with AI, Platform Health, Using Impact, Impact]
---

# View scan results for Scan Engine

You can view scans in real-time as they run or after they're completed. 

## Before you begin

Role required: sn\_se.scan\_engine\_user or sn\_se.scan\_engine\_admin

## Procedure

1.  To view a completed scan, navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Summary Scans** \(`sn_se_summary_scan` table\), and then select the scan number to view.

2.  To view a scan that is currently running, navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Scan Status**\(`sn_se_scan_status` table\).

<table id="table_nqn_vdt_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scan number

</td><td>

Unique scan record identifier \(PSR\#\)

</td></tr><tr><td>

Start time

</td><td>

Time that the scan executed

</td></tr><tr><td>

Type of scan

</td><td>

-   Full Instance Scan
-   Delta Instance Scan
-   On Demand Instance Scan


</td></tr><tr><td>

Status

</td><td>

-   **Getting ready**: New scan initial status in initialization phase
-   **Scanning**: Indicates that the scan is in progress
-   **Reconciling findings**: Organizing the findings to post on scan results and the findings dashboards
-   **Complete**: Displays a green status indicator when the scan has successfully completed
-   **Canceled**: Displays a yellow status indicator if the scan was canceled.

**Note:** In the **Actions** menu, you can select to **Cancel this scan** before scan completion.

</td></tr><tr><td>

Scan duration

</td><td>

The amount of time the scan has been running.

</td></tr><tr><td>

Estimated time remaining

</td><td>

An approximate remaining time required to complete the scan.

</td></tr><tr><td>

Percent complete

</td><td>

The percentage of the instance definitions that have been scanned.

</td></tr></tbody>
</table>3.  On the **Actions** menu, select any of the following as needed.

    |Option|Description|
    |------|-----------|
    |View Summary Scan Record |Open the summary results for the scan.|
    |Cancel this scan|Cancel the scan before it completes.|
    |Reload page|Refresh the page to see updated scan progress.|

    The following tabs display scan information.

<table id="table_g11_5nk_hhc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Batch

</td><td>

-   The batches currently being scanned.
-   Each batch shows its own progress bar.  
-   To skip a batch, select the option next to the batch to skip.


</td></tr><tr><td>

Status history

</td><td>

Status messages that displayed during the scan. 

</td></tr><tr><td>

Message

</td><td>

System messages and progress updates from the scan.

**Note:** To view the actual findings, navigate to **ALL &gt; Impact &gt; Platform Health &gt; Open Findings**.

</td></tr></tbody>
</table>
## What to do next

From the summary scan record, use the **Findings** related list to view all findings discovered during this scan. See [Understand scan results and findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/understand-scan-engine-results-findings.md) for more information.

