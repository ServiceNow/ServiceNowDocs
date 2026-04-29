---
title: Parallel scans
description: Parallel scan is a functionality in Instance Scan that allows multiple scans to run in parallel instead of sequential execution. This improves efficiency and reduces wait times when several scans are executed concurrently.
locale: en-US
release: australia
product: Instance Scan
classification: instance-scan
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Parallel scans

Parallel scan is a functionality in Instance Scan that allows multiple scans to run in parallel instead of sequential execution. This improves efficiency and reduces wait times when several scans are executed concurrently.

Use parallel scan to reduce wait times and improve throughput when multiple scans are triggered at the same time. Parallel execution is especially useful in environments with large development teams or frequent scans, where running scans sequentially can delay feedback and slow development and validation workflows. By enabling concurrent execution, parallel scan reduces delays caused by sequential processing and helps teams receive faster feedback when multiple scans are triggered across scripts, tables, update sets, or large code and configuration changes.

Parallel scan uses a queue-based execution model when `glide.scan.queue.enabled` property is enabled. If queuing is enabled, the request is placed in the queue and later picked up for execution. If queuing is not enabled, the scan starts immediately when selected.

**Note:** Scans can run in parallel only when both queuing and parallel scan properties are enabled.

## System properties for parallel scan

-   glide.scan.parallel\_scan\_enabled: This property enables or disables parallel scan execution for Instance Scan. The default value for this property is `true`, allowing multiple scan requests to execute concurrently, subject to the configured maximum parallel scan limit. If set to `false`, scans run sequentially, even if queuing is enabled.

    For example, if the maximum parallel scan value is configured as 5, the first five scans are executed simultaneously. Any subsequent scans are added to a queue and run after the initial scans complete.

-   glide.scan.queue.enabled: This property controls whether Instance Scan uses the queue-based execution model. The default value is `true` allowing scan requests to be sent to NowMQ and processed through the queue. This property must be enabled to allow scans to run in parallel, as queued execution is required for concurrent processing. When disabled, scan execution starts immediately when a scan is selected, bypassing the queue.
-   glide.scan.max\_parallel\_scans: This property defines the maximum number of instance scans that can run concurrently. The default value for parallel scan limit is 5, with a supported minimum value of 1 and a maximum value of 15.

**Note:** Parallel scan is applicable on full scan, test scan, suite scan, and reactive scan. It is not applicable with point scan.

See [Instance Scan properties](../reference/hs-sys-properties.md) for more information.

**Parent Topic:**[Using Instance Scan](hs-using-scans.md)

**Related topics**  


[Create a check](../task/hs-create-health-check.md)

[Create a check suite](../task/hc-create-check-suite.md)

[Executing a scan](../reference/hs-execute-scans.md)

[Schedule a full scan](../task/hs-schedule-full-scan.md)

[Schedule a suite scan](../task/hc-schedule-suite-scan.md)

[Monitoring a scan](../task/hs-progress-status-full-scan.md)

[Reviewing of scans](../reference/hs-review-scans.md)

[Queue your scan](../task/hs-queue-scan.md)

[Cancel a scan](../task/hs-cancel-scan.md)

[Using the Instance Scan dashboard](../task/hs-implement-dashboard.md)

