---
title: Initiate and manage scans
description: Use the Scan Results list view to initiate scans, monitor scan status, and manage scan execution using the Initiate Scan and Force Full Scan buttons.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/initiate-manage-scan-engine.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-03-05"
reading_time_minutes: 2
breadcrumb: [Run your first scan, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Initiate and manage scans

Use the Scan Results list view to initiate scans, monitor scan status, and manage scan execution using the Initiate Scan and Force Full Scan buttons.

## Before you begin

Your ServiceNow instance must be running a minimum of Zurich release with the Impact Platform Health product installed. See [Configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-impact-platform.md) for details.

Role required: impact\_admin, impact\_ai\_fix\_user, impact\_scan\_user, impact\_scan-read\_user

## About this task

The Scan Results list view provides two UI action buttons for scan initiation: **Initiate Scan** and **Force Full Scan**. The **Initiate Scan** button intelligently determines whether to run a full or delta scan based on instance history. **Force Full Scan** allows administrators to override in-progress scans and start a new full instance scan.

**Important:** The system prevents parallel scans from running simultaneously to protect resource allocation. You may need to wait for an in-progress scan to complete or use **Force Full Scan** to override.

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Scan Results**.

    This is the primary interface for initiating and monitoring scans. The Scan Results list view displays all previous scans with their status, type, and metadata.

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

4.  Refresh the **Scan Results** page to view the latest scan status in the Scan Results list view.

<table id="table_nqn_vdt_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Scan record identifier \(PSR\#\)

</td></tr><tr><td>

Start time

</td><td>

Time that the scan executed

</td></tr><tr><td>

Scan type

</td><td>

-   Full Instance Scan
-   Delta Instance Scan
-   On Demand Instance Scan


</td></tr><tr><td>

Status

</td><td>

-   **Getting ready**: New scans initial status in initialization phase
-   **In-progress**: Status after getting ready
-   **Complete**: Displays a green status indicator
-   **Canceled**: Displays a yellow status indicator


</td></tr><tr><td>

Scan Engine Score

</td><td>

Percentage score with visual bar

</td></tr></tbody>
</table>
## Example

## What to do next

After scan completion:

-   Review scan results in the Scan Results list view.
-   Address any identified issues or recommendations.
-   Review the Scan Engine Score to assess instance health.

**Parent Topic:**[Run your first scan with the Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/run-scan-engine.md)

