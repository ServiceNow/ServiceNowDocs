---
title: View scan results for Scan Engine
description: You can view scans in real-time as they run, or after they're completed. 
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# View scan results for Scan Engine

You can view scans in real-time as they run, or after they're completed. 

## Before you begin

-   Fully configure the general and additional Scan Engine properties.

    See [Configure Scan Engine properties](configure-scan-engine-properties.md) and [Configure definition properties](../reference/additional-scan-engine-properties.md).

-   Role required: Scan Engine User \(`sn_se.scan_engine_user`\), Scan Engine Admin \(`(sn_se.scan_engine_admin`\) or Impact specific roles \(Impact App Admin, Impact Platform Owner, Impact Development Team Lead, Impact Executive, Impact Developer\).

## Procedure

1.  To view a completed scan, navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Summary Scans** \(`sn_se_summary_scan` table\), and then select the scan number to view.

2.  To view a scan that is currently running, navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Scan Status**\(`sn_se_scan_status` table\).

    The following information about the scan displays.

<table id="choicetable_ojz_rmk_hhc"><tbody><tr><td id="d93147e132">

**Scan number**

</td><td>

ID number assigned to the scan

</td></tr><tr><td id="d93147e141">

**Type of scan **

</td><td>

Type of scan being run

</td></tr><tr><td id="d93147e150">

**Status**

</td><td>

Status of the scan \(In progress,Error, Canceled, Completed\) 

</td></tr><tr><td id="d93147e159">

**Scan duration**

</td><td>

How long the scan has been running

</td></tr><tr><td id="d93147e168">

**Estimated time remaining**

</td><td>

How much time is left until the scan is completed

</td></tr><tr><td id="d93147e178">

**Percent complete**

</td><td>

Percentage of how close the scan is to completing

</td></tr></tbody>
</table>    The current step that the scan is on displays. The steps of a scan are:

    1.  Getting ready
    2.  Scanning
    3.  Reconcile findings
    4.  Complete
3.  On the **Actions** menu, select any of the following as needed.

<table id="choicetable_e3k_nnk_hhc"><tbody><tr><td id="d93147e216">

**View Summary Scan Record **

</td><td>

Open the summary results for the scan.

</td></tr><tr><td id="d93147e225">

**Cancel this scan**

</td><td>

Cancel the scan before it completes.

</td></tr><tr><td id="d93147e234">

**Reload page**

</td><td>

Refresh the page.

</td></tr></tbody>
</table>    The following tabs display scan information.

<table id="choicetable_g11_5nk_hhc"><tbody><tr><td id="d93147e249">

**Batch**

</td><td>

-   The batches currently being scanned.
-   Each batch shows its own progress bar.  
-   To skip a batch, select the option next to the batch to skip.


</td></tr><tr><td id="d93147e270">

**Status history**

</td><td>

Status messages that displayed during the scan. 

</td></tr><tr><td id="d93147e279">

**Message**

</td><td>

System messages and progress updates from the scan.

**Note:** To view the actual findings, navigate to **ALL &gt; Impact &gt; Platform Health &gt; Open Findings**.

</td></tr></tbody>
</table>
## What to do next

From the summary scan record, use the **Findings** related list to view all findings discovered during this scan. See [Work with Scan Engine findings](work-with-scan-engine-findings.md) for more information.

