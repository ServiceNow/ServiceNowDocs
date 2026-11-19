---
title: Execute a full scan
description: Execute a scan for the entire instance by selecting Execute Full Scan. Implementing a full scan runs all the active checks present in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/instance-scan/hs-execute-full-scan.html
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Executing a scan, Use, Instance Scan, Maintain and monitor, Administer]
---

# Execute a full scan

Execute a scan for the entire instance by selecting **Execute Full Scan**. Implementing a full scan runs all the active checks present in your instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Checks**.

2.  To run all the active checks in your instance, select **Execute Full Scan**.

    The progress tracker shows the status of the scan.

    \[Omitted image "hs-progress-worker.png"\] Alt text: Image showing full scan progress tracker

    **Note:** Running of multiple full scans simultaneously is not allowed. If two or more checks overlap during full scan execution, only the first check succeeds. The first check keeps running while the other overlapping checks fail immediately.

3.  To find the **Result Number** and the number of checks that ran as part of the full scan, select **Go to Result**.

4.  From the related list, select **Checks** to view the list of all the checks that ran as a part of the full scan.

5.  From the related list, select **Errors** to review the errors encountered during the full scan.


## Result

A scan of the whole instance is executed.

**Parent Topic:**[Executing a scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/instance-scan/hs-execute-scans.md)

**Related topics**  


[Execute a point scan]()

[Execute a test scan]()

[Execute a suite scan]()

[Execute a reactive scan]()

