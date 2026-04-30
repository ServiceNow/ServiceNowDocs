---
title: Using the Instance Scan dashboard
description: Compare and analyze the results of the scans in your instance by representing it on the premium Performance Analytics \(PA\) dashboard.
locale: en-US
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Instance Scan, Maintain and monitor, Administer]
---

# Using the Instance Scan dashboard

Compare and analyze the results of the scans in your instance by representing it on the premium Performance Analytics \(PA\) dashboard.

## Before you begin

You've created some checks to execute the full scan. See [Create a check](hs-create-health-check.md) and [Execute a full scan](hs-execute-full-scan.md) for more information.

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Dashboard**.

2.  Select an option from the **Instance Scan Category** or **Instance Scan Priority** list.

    **Note:** The dashboard is applicable only for full scans. The **Instance Scan Category** appears only if you have data or a finding in the result set that are applicable to the categories.

3.  Select the scan result from the Scan Results list that generates an unexpected number of check findings.

    A related list of findings related to only that scan is expanded.

    ![Image showing the scan that generated unexpected results and its related list of findings](../image/hs-implement-dashboard.png)

4.  Select the scan column directly from the dashboard to display the related list of checks.

    ![Image showing how to select a particular scan result column](../image/hs-click.png)

    The related list of checks appears. The list also indicates the source that the finding has been retrieved from. ![Image showing checks for the selected health scan and the source of the problem](../image/hs-dashboard-related-list.png)


## Result

A dashboard showing the results of scans is created.

**Parent Topic:**[Using Instance Scan](../concept/hs-using-scans.md)

**Related topics**  


[Create a check](hs-create-health-check.md)

[Create a check suite](hc-create-check-suite.md)

[Executing a scan](../reference/hs-execute-scans.md)

[Schedule a full scan](hs-schedule-full-scan.md)

[Schedule a suite scan](hc-schedule-suite-scan.md)

[Monitoring a scan](hs-progress-status-full-scan.md)

[Reviewing of scans](../reference/hs-review-scans.md)

[Queue your scan](hs-queue-scan.md)

[Cancel a scan](hs-cancel-scan.md)

