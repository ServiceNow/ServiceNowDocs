---
title: Using the Instance Scan dashboard
description: Compare and analyze the results of the scans in your instance by representing it on the premium Performance Analytics \(PA\) dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/instance-scan/hs-implement-dashboard.html
release: australia
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Using the Instance Scan dashboard

Compare and analyze the results of the scans in your instance by representing it on the premium Performance Analytics \(PA\) dashboard.

## Before you begin

You've created some checks to execute the full scan. See [Create a check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-create-health-check.md) and [Execute a full scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-execute-full-scan.md) for more information.

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Dashboard**.

2.  Select an option from the **Instance Scan Category** or **Instance Scan Priority** list.

    **Note:** The dashboard is applicable only for full scans. The **Instance Scan Category** appears only if you have data or a finding in the result set that are applicable to the categories.

3.  Select the scan result from the Scan Results list that generates an unexpected number of check findings.

    A related list of findings related to only that scan is expanded.

    \[Omitted image "hs-implement-dashboard.png"\] Alt text: Image showing the scan that generated unexpected results and its related list of findings

4.  Select the scan column directly from the dashboard to display the related list of checks.

    \[Omitted image "hs-click.png"\] Alt text: Image showing how to select a particular scan result column

    The related list of checks appears. The list also indicates the source that the finding has been retrieved from. \[Omitted image "hs-dashboard-related-list.png"\] Alt text: Image showing checks for the selected health scan and the source of the problem


## Result

A dashboard showing the results of scans is created.

**Parent Topic:**[Using Instance Scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-using-scans.md)

**Related topics**  


[Create a check]()

[Create a check suite]()

[Executing a scan]()

[Schedule a full scan]()

[Schedule a suite scan]()

[Monitoring a scan]()

[Parallel scans]()

[Reviewing of scans]()

[Queue your scan]()

[Cancel a scan]()

