---
title: Execute a full scan
description: Execute a scan for the entire instance by selecting Execute Full Scan. Implementing a full scan runs all the active checks present in your instance.
locale: en-US
release: xanadu
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Execute a full scan

Execute a scan for the entire instance by selecting **Execute Full Scan**. Implementing a full scan runs all the active checks present in your instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Checks**.

2.  To run all the active checks in your instance, select **Execute Full Scan**.

    The progress tracker shows the status of the scan.

    ![Image showing full scan progress tracker](../image/hs-progress-worker.png)

    **Note:** Running of multiple full scans simultaneously is not allowed. If two or more checks overlap during full scan execution, only the first check succeeds. The first check keeps running while the other overlapping checks fail immediately.

3.  To find the **Result Number** and the number of checks that ran as part of the full scan, select **Go to Result**.

4.  From the related list, select **Checks** to view the list of all the checks that ran as a part of the full scan.

5.  From the related list, select **Errors** to review the errors encountered during the full scan.


## Result

A scan of the whole instance is executed.

