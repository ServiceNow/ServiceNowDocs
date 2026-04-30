---
title: Queue your scan
description: Leverage the scan queue feature to line up your scans for automatic execution following the current scan.
locale: en-US
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Instance Scan, Maintain and monitor, Administer]
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

    ![Screenshot showing the queue message](../image/hs-queue-msg.png)

    If you select the View All link, the list of all queued scans shows up. If you select View Request, it only shows the status of the selected scan.

    ![Screenshot showing the queued status](../image/hs-queue-status.png)

    **Note:** If a scan is already in progress and you select another scan, it gets queued to be executed. If you select the same scan again, it doesn't create duplicate records in the queue. Once the ongoing scan completes \(successful or failed\), the next scan in the queue starts executing automatically.

    If there is no ongoing scan, the selected scan starts the execution process. You will see the execution modal with **Cancel Scan** and **Go to Results** options.

3.  Implement the following steps to view the status of the ongoing scan or any other scans.

    1.  Go to **All** &gt; **Instance Scan** &gt; **Scan Results**. The list of all scan results and their status shows up.
    2.  Select a scan record to see more details. The Scan Results form for the selected scan record shows up.

        **Note:** If the scan is ongoing, the status is In progress. If the scan is queued, the status is Pending.

    3.  Select Show Progress related link.

        ![Screenshot showing Show Progress related link when the status is In Progress](../image/hs-show-progress-link.png)

        **Note:** This related link is visible only if the selected scan is currently executing.

    4.  Select either the Cancel Scan related link or the **Cancel Scan** button on the scan execution modal if you want to cancel the ongoing scan.

        **Note:** These options are visible only if the scan is currently executing and is not yet completed \(successful or failed\).


**Parent Topic:**[Using Instance Scan](../concept/hs-using-scans.md)

**Related topics**  


[Create a check](hs-create-health-check.md)

[Create a check suite](hc-create-check-suite.md)

[Executing a scan](../reference/hs-execute-scans.md)

[Schedule a full scan](hs-schedule-full-scan.md)

[Schedule a suite scan](hc-schedule-suite-scan.md)

[Monitoring a scan](hs-progress-status-full-scan.md)

[Reviewing of scans](../reference/hs-review-scans.md)

[Cancel a scan](hs-cancel-scan.md)

[Using the Instance Scan dashboard](hs-implement-dashboard.md)

