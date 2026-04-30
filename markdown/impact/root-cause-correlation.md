---
title: Root Cause Correlation
description: Root Cause Correlation \(RCC\) streamlines performing a root cause analysis by automatically correlating metrics, logs, and event information for supported symptoms on production instances for the last 24 hours.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Alerts in Instance Observer, Impact Instance Observer, Platform Health, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Root Cause Correlation

Root Cause Correlation \(RCC\) streamlines performing a root cause analysis by automatically correlating metrics, logs, and event information for supported symptoms on production instances for the last 24 hours.

## RCC symptom categories

The RCC feature is available for self-service alerts and supports the following symptom categories:

-   Memory
-   Longest running sessions
-   Slow transactions
-   Cache flush
-   Database locks
-   Database impacts

The table describes the symptom categories and the corresponding alerts that the RCC engine detects.

<table id="table_jpp_xtf_d2c"><thead><tr><th>

Symptoms​ categories

</th><th>

Description

</th><th>

Corresponding alert

</th></tr></thead><tbody><tr><td>

DB Impact​

</td><td>

Helps the user to identify and address extended SQL queries impacting database performance, tied to high execution time, or increased volumes. The query patterns give snapshots of 30 minute and 60 minute durations from the time the impact is observed on query execution times.​

</td><td>

Database response time

</td></tr><tr><td>

Cache Flush​

</td><td>

Cache flushes and node restarts are detected, as well as high service saturation levels that may have occurred around the time a performance alert was triggered.​

</td><td>

Default semaphore mean

</td></tr><tr><td>

Longest Running Session​

</td><td>

Searches for the top long-running sessions in mean time to recover \(MTTR\) logs and identifies the top transaction pattern hash with the highest processing times and then the transaction IDs.​

</td><td>

Default semaphore mean

</td></tr><tr><td>

Slow Transactions ​

</td><td>

-   Identifies the top long-running transactions using the total duration, including ACL time, SQL time, CPU time, processing time, BR time, and script time.
-   Returns the transaction IDs, the pattern hash, and these metrics to help users identify the specific causes of long-running transactions.

​

</td><td>

Default semaphore mean​

</td></tr><tr><td>

Memory​

</td><td>

-   Pinpoints the three nodes most impacted by garbage collection pauses, determined by the aggregate duration of the pauses.
-   Identifies any transactions or worker threads on these nodes that exceed 200 seconds.

**Note:** Users are advised to review these long-running or frequently recurring threads.​


</td><td>

Node Garbage Collection Time

</td></tr><tr><td>

DB locks​

</td><td>

The RCC engine monitors innodb\_row\_lock\_waits and threads\_running to detect anomalous database lock events that occur when a database operation requires exclusive access.​

</td><td>

Threads running​

</td></tr></tbody>
</table>## RCC report statuses

When an RCC report is generated several statuses are available:

-   RCC In progress: The RCC report generation is being generated.
-   RCC generated: The report has been successfully generated.
-   No RCC found: When there is not enough information to generate the report.
-   RCC failed: Returned when there is a technical issue, generally remedied to regenerate the report.

