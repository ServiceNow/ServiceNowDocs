---
title: Schedule a full scan
description: Create a schedule to regularly trigger a full scan even when you don’t have an active session. A schedule creates an established baseline for the health of the instance and provides a comparison to configuration and instance health over time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/instance-scan/hs-schedule-full-scan.html
release: australia
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Schedule a full scan

Create a schedule to regularly trigger a full scan even when you don’t have an active session. A schedule creates an established baseline for the health of the instance and provides a comparison to configuration and instance health over time.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Checks**.

2.  Select **Schedule Full Scan**.

3.  On the Trigger full scan form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the check record.|
    |Active|Option to execute the scan at a scheduled time.|
    |Application|Application where the job belongs.|
    |Conditional|Option to select conditions under which the scan runs.|
    |Run|List used to select the scheduling of full scan.|
    |Run this script|Selection to run the default script.|
    |Update|The script that is updated for full scan.|
    |Execute Now|The default script that is executed for full scan.|
    |Delete|The script is deleted for full scan.|

4.  To run the full scan, select **Execute Now**.

    A list of findings is displayed.

5.  From the application navigator, select **Results**.

    The status of the execution is displayed along with the **Result Number**.

6.  To display the list of findings, select the **Result Number**.

7.  From the application navigator, select **Dashboard** to display data about the findings.


## Result

A schedule to trigger a full scan regularly even without an active session is created.

**Parent Topic:**[Using Instance Scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-using-scans.md)

**Related topics**  


[Create a check]()

[Create a check suite]()

[Executing a scan]()

[Schedule a suite scan]()

[Monitoring a scan]()

[Parallel scans]()

[Reviewing of scans]()

[Queue your scan]()

[Cancel a scan]()

[Using the Instance Scan dashboard]()

