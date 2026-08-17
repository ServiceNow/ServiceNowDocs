---
title: View scan results for Scan Engine
description: You can view scans in real-time as they run or after they're completed. 
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/viewing-scan-results-scan-engine.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Understand scan results and findings, Prevent and resolve technical debt with AI, Platform Health, Using Impact, Impact]
---

# View scan results for Scan Engine

You can view scans in real-time as they run or after they're completed. 

## Before you begin

-   Fully configure the general and additional Scan Engine properties.

    See [Configure Scan Engine parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-scan-engine-properties.md) and [Manage definition properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/additional-scan-engine-properties.md).

-   Role required: sn\_se.scan\_engine\_user or sn\_se.scan\_engine\_admin

## Procedure

1.  To view a completed scan, navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Summary Scans** \(`sn_se_summary_scan` table\), and then select the scan number to view.

2.  To view a scan that is currently running, navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Scan Status**\(`sn_se_scan_status` table\).

    The following information about the scan displays.

    |Field|Description|
    |-----|-----------|
    |Scan number|ID number assigned to the scan|
    |Type of scan |Type of scan being run|
    |Status|Status of the scan \(In progress,Error, Canceled, Completed\) |
    |Scan duration|How long the scan has been running|
    |Estimated time remaining|How much time is left until the scan is completed|
    |Percent complete|Percentage of how close the scan is to completing|

    The current step that the scan is on displays. The steps of a scan are:

    1.  Getting ready
    2.  Scanning
    3.  Reconcile findings
    4.  Complete
3.  On the **Actions** menu, select any of the following as needed.

    |Option|Description|
    |------|-----------|
    |View Summary Scan Record |Open the summary results for the scan.|
    |Cancel this scan|Cancel the scan before it completes.|
    |Reload page|Refresh the page.|

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

From the summary scan record, use the **Findings** related list to view all findings discovered during this scan. See [Understand scan results and findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/understand-scan-engine-results-findings.md) for more information.

