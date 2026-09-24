---
title: Manage and monitor scans
description: Initiate scans, monitor scan status, and manage scan execution using the Initiate Scan and Force Full Scan buttons.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/initiate-manage-scan-engine.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Run on-demand scans, Scan your instance, Impact Guided Setup, Configuring Impact, Impact]
---

# Manage and monitor scans

Initiate scans, monitor scan status, and manage scan execution using the Initiate Scan and Force Full Scan buttons.

## Before you begin

Your ServiceNow instance must be running a minimum of Zurich release with the Impact Platform Health product installed. See [Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-impact-platform.md) for details.

Role required: impact\_admin, impact\_ai\_fix\_user, impact\_scan\_user, impact\_scan-read\_user

## About this task

The Scan Results list view provides two UI action buttons for scan initiation: **Initiate Scan** and **Force Full Scan**. The **Initiate Scan** button intelligently determines whether to run a full or delta scan based on instance history. **Force Full Scan** allows administrators to override in-progress scans and start a new full instance scan.

**Important:** The system prevents parallel scans from running simultaneously to protect resource allocation. You may need to wait for an in-progress scan to complete or use **Force Full Scan** to override.

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Summary Scans**.

    The Scan Results list view displays all previous scans with their status, type, and metadata. This is the primary interface for initiating and monitoring scans.

2.  Select **Initiate Scan**.

    The **Initiate Scan** button intelligently determines the scan type:

    -   If the instance has no prior full scan, a Full Instance Scan is initiated.
    -   If a full scan exists, a Delta Instance Scan is initiated.
    One of the following messages appears:

    -   **Scan initiated**: "A new scan has been triggered and it will take a moment to reflect in the queue. Please refresh the page for the latest scan results."
    -   **Scan blocked**: If a scan is already in progress: "Cannot initiate a delta scan while another scan is in progress. Please wait for the current scan to complete or use Force Full Scan to override."
3.  Select **Force Full Scan** to override and run a complete full instance scan if a Delta Scan is already in progress \(available to Admin role only\).

    -   A confirmation modal appears with the title "Trigger Scan" and the message: "A Delta Scan is currently in progress. Do you want to cancel the ongoing Delta Scan and start a Full Scan instead?"
    -   Select **OK** to confirm the override. The current Delta Scan is canceled automatically, and a new Full Instance Scan is initiated immediately.

        Select **Cancel** to discontinue the override.

4.  View the scan information.

    |Field|Description|
    |-----|-----------|
    |Number|ID number assigned to the scan|
    |Start time|UTC time of when the scan executed.|
    |Scan type|Type of scan being run. See [Monitor and manage instance health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-parallel-processing.md) for details.|
    |Status|Status of the scan.|
    |Active custom definition limit|Indicates if the number of custom definitions is within your Impact package allocation. For details on the limits, see [Impact packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-packages1.md).|
    |Scan Engine score|A percentage of|
    |Local update set|Displays the update set being scanned|
    |State|Getting ready, Scanning, Reconcile findings, Complete.|
    |Scan duration|How long the scan has been running|
    |Application|Displays the Application being scanned.|
    |Source|Percentage of how close the scan is to completing|

5.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scan Status**to track the scan progress to view the latest scan status in list view.

    See [View scan results for Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/viewing-scan-results-scan-engine.md) for additional information.

6.  On the **Actions** menu, select any of the following as needed.

    |Option|Description|
    |------|-----------|
    |View Summary Scan Record |Open the summary results for the scan.|
    |Cancel this scan|Cancel the scan before it completes.|
    |Reload page|Refresh the page to see updated scan progress.|


## Example

## What to do next

After scan completion:

-   Review scan results in the Scan Results list view.
-   Address any identified issues or recommendations.
-   Review the Scan Engine Score to assess instance health.

**Parent Topic:**[Run on-demand scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/using-impact-scan-engine.md)

