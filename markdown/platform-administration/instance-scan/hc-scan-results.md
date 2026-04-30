---
title: Scan results
description: Scan Results dashboard helps you with an overview of all details of an executed scan.
locale: en-US
release: yokohama
product: Instance Scan
classification: instance-scan
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Results, Reviewing of scans, Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Scan results

Scan Results dashboard helps you with an overview of all details of an executed scan.

Navigate to **All** &gt; **Instance Scan** &gt; **Results**. Select a scan result from the Scan Results list. Click Results Dashboard link on the Scan Result form.

![Image showing scan results dashboard](../image/hc-scan-results-dashboard.png)

Select **Rescan** to execute the same scan again. If you want to see all the findings grouped by checks, select **Findings** at the top right corner.

<table id="table_ph5_fns_xjb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Previous Scan

</td><td>

Details about the previous scan.-   Result number: Link to the previous scan result record
-   Outstanding Findings: Total findings whose status has not been marked as Resolved.
-   Resolved Findings: Total findings whose status has been marked as Resolved.

**Note:** Not all findings that have been marked Resolved are fixed. If a finding has not been fixed and has been marked Resolved, it still adds to the count of total findings.

-   Date: Date and time on which the previous scan started
-   Duration: Total time needed to complete the previous scan

</td></tr><tr><td>

Latest Scan

</td><td>

Details about the recent completed scan.-   Result number: Link to the latest scan result record
-   Findings: Total number of findings found in the latest scan
-   Target: Target against which the scan is executed
    -   Full Instance: Scans all the available records in the instance
    -   Scoped App: Scans selected scoped apps. You can select multiple scoped apps.
    -   Update Set: Scans multiple update sets.
-   Date: Date and time on which the scan started
-   Duration: Total time needed to complete the scan

</td></tr><tr><td>

Scan Tasks By Priority

</td><td>

Scan tasks sorted by priority. The priority comes from the checks to which these tasks belong.**Note:** The states come from the states of the tasks associated with the findings.

</td></tr><tr><td>

Average Findings Over Time

</td><td>

Reporting of the average number of findings in a day.

</td></tr><tr><td>

Category Breakdown

</td><td>

Category breakdown of the checks that have run as part of the scan

</td></tr><tr><td>

Product Breakdown

</td><td>

Product family of each of the scan findings records.**Note:** Incident records don't have product family.

</td></tr><tr><td>

Findings By Developer

</td><td>

Name of the user whose changes generated the findings.**Note:** Only the top 5 user names appear on the list. Click **View All** to view all the findings grouped by users.

</td></tr></tbody>
</table>If a scan is in progress and at least one of the checks fails, the following warning message shows up.![Image showing warning message for scan results](../image/hc-scan-results-warning.png)

**Parent Topic:**[Results](hs-results.md)

