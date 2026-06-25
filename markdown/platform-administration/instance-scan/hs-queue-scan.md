---
title: Queue your scan
description: Leverage the scan queue feature to line up your scans for automatic execution following the current scan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/instance-scan/hs-queue-scan.html
release: australia
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Queue your scan

Leverage the scan queue feature to line up your scans for automatic execution following the current scan.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Checks**.

    The list of checks shows up.

2.  Select a scan to run it on the selected check.

    The scan execution modal shows up.

    **Note:** If another scan is ongoing, the modal gives a message that the current scan is in the queue. You will also see View Request and View All links in the scan modal.

    \[Omitted image "hs-queue-msg.png"\] Alt text: Screenshot showing the queue message

    If you select the View All link, the list of all queued scans shows up. If you select View Request, it only shows the status of the selected scan.

    \[Omitted image "hs-queue-status.png"\] Alt text: Screenshot showing the queued status

    **Note:** If a scan is already in progress and you select another scan, it gets queued to be executed. If you select the same scan again, it doesn't create duplicate records in the queue. Once the ongoing scan completes \(successful or failed\), the next scan in the queue starts executing automatically.

    If there is no ongoing scan, the selected scan starts the execution process. You will see the execution modal with **Cancel Scan** and **Go to Results** options.

3.  Implement the following steps to view the status of the ongoing scan or any other scans.

    1.  Go to **All** &gt; **Instance Scan** &gt; **Scan Results**. The list of all scan results and their status shows up.
    2.  Select a scan record to see more details. The Scan Results form for the selected scan record shows up.

        **Note:** If the scan is ongoing, the status is In progress. If the scan is queued, the status is Pending.

    3.  Select Show Progress related link.

        \[Omitted image "hs-show-progress-link.png"\] Alt text: Screenshot showing Show Progress related link when the status is In Progress

        **Note:** This related link is visible only if the selected scan is currently executing.

    4.  Select either the Cancel Scan related link or the **Cancel Scan** button on the scan execution modal if you want to cancel the ongoing scan.

        **Note:** These options are visible only if the scan is currently executing and is not yet completed \(successful or failed\).


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

[Cancel a scan]()

[Using the Instance Scan dashboard]()

