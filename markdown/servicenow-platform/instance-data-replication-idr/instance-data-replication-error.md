---
title: Consumer replication set status in Instance Data Replication
description: Review the status of your consumer replication set and research error messages to identify or fix Instance Data Replication \(IDR\) replication issues.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Resolving errors, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Consumer replication set status in Instance Data Replication

Review the status of your consumer replication set and research error messages to identify or fix Instance Data Replication \(IDR\) replication issues.

## Consumer replication set status and status message

Navigate to **Instance Data Replication** &gt; **Consumer Replication Sets** to access a consumer replication set, and view the status and status messages.

![Consumer replication set status and messages.](../image/consumer-replication-status.png "Consumer Replication Set")

|Status|Description|
|------|-----------|
|In Draft|To use your consumer replication set, click **Activate**.|
|Activation Requested|After you initiate an activation, you must wait for the producer instance to respond to your request. If the wait time is excessive, then check the replication log for errors.|
|Seeding|The seeding job must complete before replication can resume.|
|Seeding Paused|The seeding job must resume before the seeding can continue.|
|Active|Normal status.|
|Replication Stopped|Check the Status Messages in the following table for a specific message and associated fix.|
|Replication Paused|The replication process must resume before the replication can continue.|
|Replication Error|Check the Status Messages in the following table for a specific message and associated fix.|
|Replication Deactivated|Activate the producer and consumer instances.|
|Subscription Requested|Approve the request for a consumer subscription on the producer instance.|

|Message|Action|
|-------|------|
|`All Producer Replication Sets have been deactivated due to fatal replication error`|All consumer replication sets are moved to the error state. Contact Customer Service and Support.|
|`Consumer replication set received out of order messages`|Contact Customer Service and Support.|
|`Error while seeding data. Please refer to the Replication Payload Error table for details`|On the consumer instance, more than one record failed to seed. To recover, go to the [Replication Payload Error](../task/debug-instance-data-replication.md) table to find and fix the error, and then activate the consumer replication set.|
|`Error while seeding data. Please retry seeding this table`|To recover, [reseed the table](../task/seed-consumer-instance.md).|
|`Producer has encountered an error while seeding`|To recover, contact the administrator of the producer instance to determine the cause of the problem.|
|`Producer Replication Set configuration has been modified`|On the consumer instance, click **Synchronize Replication Entries** and then click **Activate**.|
|`Producer Replication Set has been deactivated due to replication error`|Contact Customer Service and Support.|
|`Producer Replication Set has been deactivated`|To recover, activate the producer replication set, and then activate the consumer replication set.|
|`Producer Replication Set has been deleted`|To recover, delete the consumer replication set.|
|`Producer Replication Set is inactive`|To recover, activate the producer replication set, and then synchronize and activate the consumer replication set.|
|`Producer Replication Set not found`|To recover, delete the consumer replication set.|
|`Replication Set Paused`|To recover, click **Resume** or **Activate**.|
|`Replication set was in pause/error/seeding pause state for more than 7 days`|The consumer replication set has been in the pause state, error state, or seeding pause state for more than the timeout period. The replication set is put into the disabled state. To recover, [check for seeding errors](../task/fix-seeding-errors.md) and activate the consumer replication set with seeding.|
|`Seeding has been terminated due to timeout`|To recover, retry the seeding request or contact Customer Service and Support.|
|`Seeding request for a Producer Replication Set containing more than X number of records is not supported`|To recover, change the filter criteria to reduce the number of records to be seeded or use partial seeding. The default limit is 10 million records. Contact Customer Service and Support to change the default limit.|
|`Seeding was cancelled by a consumer admin`|To recover, activate the consumer replication set.|
|`Seeding was cancelled by a producer admin`|To recover, activate the consumer replication set. Only seeding requests in the queued, paused, or started states can be canceled. In this case, the consumer replication state is Replication Error.|
|`Shared key not matching`|The producer and consumer replication sets have different shared keys. To recover, copy the shared encryption key on the producer replication set, paste it into the consumer replication set, and activate the replication set.|

**Parent Topic:**[Resolving data replication errors in Instance Data Replication](common-issues-idr.md)

