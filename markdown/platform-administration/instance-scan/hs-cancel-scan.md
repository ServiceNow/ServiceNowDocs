---
title: Cancel a scan
description: Cancel or abort an ongoing scan by either selecting Cancel Scan in the scan execution modal or the Cancel Scan related link in the results record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/instance-scan/hs-cancel-scan.html
release: australia
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Cancel a scan

Cancel or abort an ongoing scan by either selecting Cancel Scan in the scan execution modal or the Cancel Scan related link in the results record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Checks**.

    The list of checks shows up.

2.  Select a scan to run it on the selected check.

    \[Omitted image "hs-cancel-scan-module.png"\] Alt text: Screenshot showing the execution modal.

    The scan execution modal shows up.

3.  Select **Cancel Scan** to cancel the ongoing scan.

    The Cancel Scan modal shows up with the status of the cancelled transaction. You can also select **Go to Results** to see the results record of the selected scan.

    \[Omitted image "hs-cancel-scan.png"\] Alt text: Screenshot showing cancelled scan

    **Note:** The **Cancel Scan** button won’t show up if the scan is complete \(successful or failed\).

4.  Select **Cancel Scan** related link to cancel the scan, if you have selected **Go to Results** in the previous step.

    \[Omitted image "hs-cancel-scan-related-link.png"\] Alt text: Screenshot showing the status and cancel scan related link

    **Note:** The **Cancel Scan** related link is visible only if the scan is still running. The **Status** field in the Scan Results form say In Progress if the scan is still ongoing.

5.  Close the Cancel Scan modal or select **Go to Results** in the Cancel Scan modal.

    \[Omitted image "hs-status-cancel.png"\] Alt text: Screenshot showing cancelled status

    The Scan Result record is updated. The **Status** field now says Cancelled.

6.  Scroll down to the **Scan Findings** related list.

    It generates the findings of the scan till the point it was cancelled.

    **Note:** Since the scan is already cancelled, the Cancel Scan related link doesn’t show up.


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

[Using the Instance Scan dashboard]()

