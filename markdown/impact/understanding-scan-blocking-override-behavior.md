---
title: Scan blocking and override behavior scenarios
description: The Scan Engine blocks concurrent scans to protect instance performance. Understanding these rules helps you plan scan execution efficiently and how the system handles concurrent scan requests and when Force Full Scan override is necessary.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Full and delta instance scan initiation, Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan blocking and override behavior scenarios

The Scan Engine blocks concurrent scans to protect instance performance. Understanding these rules helps you plan scan execution efficiently and how the system handles concurrent scan requests and when Force Full Scan override is necessary.

## Scenario 1: Attempting to initiate a scan while another scan is in progress

If you select **Initiate Scan** while any scan is already running, the system displays an alert: "Cannot initiate a delta scan while another scan is in progress. Please wait for the current scan to complete or use Force Full Scan to override."Options:

-   Wait for the current scan to complete, then select **Initiate Scan** again
-   Use **Force Full Scan** to cancel the current scan and start a new full scan immediately

## Scenario 2: Using Force Full Scan when a Delta Scan is running

When you need to run a full instance scan instead of waiting for a delta scan to complete:

1.  Select **Force Full Scan**.
2.  Review the Trigger Scan confirmation modal that displays: "A Delta Scan is currently in progress. Do you want to cancel the ongoing Delta Scan and start a Full Scan instead?"
3.  Select **OK** to cancel the delta scan and start the full scan, or **Cancel** to discontinue.

The in-progress delta scan is canceled automatically and the new full scan begins immediately.

## Scenario 3: Viewing canceled scans in the Scan Results list

Canceled scans remain visible in the Scan Results list with:

-   Yellow status indicator
-   Canceled status label
-   Original start time and scan type preserved

This provides an audit trail of all scan activity, including canceled operations.

Understanding scan blocking behavior helps you choose the appropriate action based on your immediate needs and scan priorities.

## Scenario 4: Refreshing the page to see latest scan status

The system requires a page refresh to display the most current scan information. After initiating or canceling a scan:

-   Select the browser refresh button or press `F5`.
-   The Scan Results list updates to show the latest scan status.
-   New scans appear with **Getting ready** status before transitioning to in-progress

