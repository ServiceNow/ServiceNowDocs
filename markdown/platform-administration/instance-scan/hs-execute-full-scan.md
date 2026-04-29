---
title: Execute a full scan
description: Execute a scan for the entire instance by selecting Execute Full Scan. Implementing a full scan runs all the active checks present in your instance.
locale: en-US
release: australia
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Executing a scan, Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Execute a full scan

Execute a scan for the entire instance by selecting **Execute Full Scan**. Implementing a full scan runs all the active checks present in your instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Checks**.

    A list of all the checks on the instance shows up.

2.  Select **Execute Full Scan** to execute full scan on all the checks.

    The progress tracker shows the status of the scan.

    ![Image showing full scan progress tracker](../image/hs-progress-worker.png)

    **Note:** You can now execute multiple full scans simultaneously if you have enabled glide.scan.parallel\_scan\_enabled system property. You can also set the maximum number of scans that can run concurrently by setting the value for glide.scan.max\_parallel\_scans property. See [Instance Scan properties](../reference/hs-sys-properties.md) for more information.

    ![Image showing parallel scan in full scan](../image/hs-full-scan-queue-parallel.png)

    Select View queued requests link to see all the queued requests on the Scan Queue Operations page.

    **Note:** This modal shows up only when the number of parallel scans exceeds the set value for concurrent scans.

3.  Review the results and other information about the scan execution on the Scan Queue Operations page.

    **Note:** This step is applicable only when you are executing multiple full scans in parallel.

4.  To find the **Result Number** and the number of checks that ran as part of the full scan, select **Go to Result**.

5.  From the related list, select **Checks** to view the list of all the checks that ran as a part of the full scan.

6.  From the related list, select **Errors** to review the errors encountered during the full scan.


## Result

A scan of the whole instance is executed.

**Parent Topic:**[Executing a scan](../reference/hs-execute-scans.md)

**Related topics**  


[Execute a point scan](hs-execute-point-scan.md)

[Execute a test scan](hs-execute-test-scan.md)

[Execute a suite scan](hc-execute-suite-scan.md)

[Execute a reactive scan](hs-reactive-scan.md)

