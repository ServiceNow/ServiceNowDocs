---
title: Resolving data replication errors in Instance Data Replication
description: Resolve errors and monitor the status of Instance Data Replication \(IDR\) replication sets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/instance-data-replication-idr/common-issues-idr.html
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Resolving data replication errors in Instance Data Replication

Resolve errors and monitor the status of Instance Data Replication \(IDR\) replication sets.

## Monitoring and diagnostic checklist

When you notice that the system is not replicating data, you can use the diagnostics checks to investigate the problem. To monitor the overall health of all replication sets, see [IDR Monitoring dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/instance-data-replication-dashboard.md).

<table id="table_dsk_121_mkb"><thead><tr><th>

Check

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Monitor

</td></tr><tr><td>

[Check connectivity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/test-IDR-connectivity.md)

</td><td>

Test your IDR instance connectivity to determine the connectivity of your instance to the message queue.

</td></tr><tr><td>

[Check IDR monitoring dashboard to see if replication jobs are active](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/instance-data-replication-dashboard.md)

</td><td>

For the dashboard to properly display replication set information, these IDR scheduled jobs must be available and running on your instance:-   Hermes Metrics Collection
-   Hermes Periodic Purge
-   Hermes Topics Util
-   IDRConsumerJob
-   IDRDeltaConsumerJob-&lt;instanceid&gt;
-   IDRHeartbeatJob
-   IDRMetadataConsumerJob
-   IDRProducerJob
-   IDRSeedingProducerJob

 If any of these jobs are missing or not running, contact Customer Service and Support.

 **Note:** The system only creates the IDRDeltaConsumerJob-&lt;instanceid&gt; when a consumer instance subscribes to a producer instance that is outside the local datacenter.

</td></tr><tr><td colspan="2">

Producer replication set

</td></tr><tr><td>

Check activation of the producer replication set

</td><td>

If the status of your producer replication set is In Draft, click **Activate**.

</td></tr><tr><td>

Check consumer subscription approval

</td><td>

Review the consumer access requests for your producer replication sets. A consumer replication set must request access before it can receive replication data.

</td></tr><tr><td>

[Check producer replication log errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/debug-instance-data-replication.md)

</td><td>

Identify IDR errors by viewing the metadata for messages between producer and consumer instances, payload error logs, and message logs.

</td></tr><tr><td colspan="2">

Consumer replication set

</td></tr><tr><td>

Check activation status of the consumer replication set

</td><td>

If the status of your consumer replication set is In Draft, click **Activate**.

</td></tr><tr><td>

[Check if you need to synchronize replication sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/synchronization-errors.md)

</td><td>

A synchronization issue occurs when a producer instance doesn't send data or a consumer instance doesn't receive data. Synchronization errors appear in the **Status** field on the consumer instance as **Replication Error**.

</td></tr><tr><td>

[Check your consumer replication set status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/instance-data-replication-error.md)

</td><td>

Review the status of your consumer replication set and what that means for your replication.

</td></tr><tr><td colspan="2">

Error and status messages

</td></tr><tr><td>

[Check replication or replication metadata log errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/debug-instance-data-replication.md)

</td><td>

Identify IDR errors by viewing the metadata for messages between producer and consumer instances, payload error logs, and message logs.

</td></tr><tr><td>

[Check status messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/instance-data-replication-error.md)

</td><td>

Review these status messages with recovery information.

</td></tr></tbody>
</table>-   **[Run Instance Data Replication diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/test-IDR-connectivity.md)**  
Verify the status of services and the connection between your instance and the Instance Data Replication \(IDR\) message queue.
-   **[Review synchronization errors in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/synchronization-errors.md)**  
Review the status field to check if synchronization is working correctly on the Instance Data Replication \(IDR\) consumer instance.
-   **[Discover replication delays in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/diagnose-delayed-replication.md)**  
Monitor possible data replication issues by using the Instance Data Replication \(IDR\) Monitoring Dashboard.
-   **[Fix seeding errors in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/fix-seeding-errors.md)**  
Retry Instance Data Replication \(IDR\) seeding on tables with seeding errors, which occur from network problems and failed inserts, so that you don't have to do a full seeding.
-   **[Identify Instance Data Replication errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/debug-instance-data-replication.md)**  
Identify Instance Data Replication \(IDR\) errors by viewing the metadata for messages between producer and consumer instances, payload error logs, and message logs.
-   **[Configure error notifications in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/configure-notification-idr.md)**  
Notify one or more users when errors occur in Instance Data Replication \(IDR\).
-   **[Consumer replication set status in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/instance-data-replication-error.md)**  
Review the status of your consumer replication set and research error messages to identify or fix Instance Data Replication \(IDR\) replication issues.
-   **[Instance Data Replication XML stats](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/IDR-XML-stats.md)**  
Extract Instance Data Replication \(IDR\)-related data from your instance to monitor replication status.

**Parent Topic:**[Administering Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/administering-instance-data-replication.md)

**Related topics**  


[Manage consumer access to replication data in Instance Data Replication]()

[Comparing replicated data between instances in Instance Data Replication]()

[Deploying a replication configuration from one instance to another in Instance Data Replication]()

[Cloning options with Instance Data Replication]()

[Monitoring replication status in Instance Data Replication]()

[Monitoring queues in Instance Data Replication]()

[Avoiding insert and update errors in Instance Data Replication]()

