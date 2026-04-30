---
title: Remote Process Sync system properties
description: Refer to the list of system properties for Remote Process Sync to learn how to manage your process-oriented, multi-instance integration.
locale: en-US
release: xanadu
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integration Hub Remote Process Sync, Creating integrations with applications]
---

# Remote Process Sync system properties

Refer to the list of system properties for Remote Process Sync to learn how to manage your process-oriented, multi-instance integration.

To set Remote Process Sync system properties, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Properties** or set them on the System Properties \[sys\_properties\] table.

<table id="table_gqg_hxk_qnb"><thead><tr><th>

System Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.hub.process.sync.jobs.outbound.context\_reporting

</td><td>

If set to `true`, outbound scheduled jobs:

-   Use the standard **FlowAPI** instead of the quick API \(default\)
-   Write flow contexts to the outbound queue
-   Write outbound records to the Outbound Queue States \[ih\_sync\_outbound\_record\] table

 -   Default value: `false`
-   Minimum value: Not applicable
-   Maximum value: Not applicable

</td></tr><tr><td>

glide.hub.process.sync.jobs.inbound.context\_reporting

</td><td>

If set to `true`, inbound scheduled jobs:

-   Use the standard **FlowAPI** instead of the quick API \(default\)
-   Write flow contexts to the inbound queue
-   Write inbound records to the Inbound Records \[ih\_sync\_inbound\_record\] table

 -   Default value: `false`
-   Minimum value: Not applicable
-   Maximum value: Not applicable

</td></tr><tr><td>

glide.hub.process.sync.jobs.outbound.process\_maxtime

</td><td>

Maximum time, in seconds, that an outbound scheduled job runs before timing out.-   Default value: `300`
-   Minimum value: `60`
-   Maximum value: `1800`

</td></tr><tr><td>

glide.hub.process.sync.jobs.inbound.process\_maxtime

</td><td>

Maximum time, in seconds, that an inbound scheduled job runs before timing out.-   Default value: `300`
-   Minimum value: `60`
-   Maximum value: `1800`

</td></tr><tr><td>

glide.hub.process.sync.jobs.outbound.subflow.execution\_timeout

</td><td>

Time, in milliseconds, that an outbound subflow runs before timing out.-   Default value: `30000`
-   Minimum value: None
-   Maximum value: None

</td></tr><tr><td>

glide.hub.process.sync.jobs.inbound.subflow.execution\_timeout

</td><td>

Time, in milliseconds, that an inbound subflow runs before timing out.-   Default value: `30000`
-   Minimum value: None
-   Maximum value: None

</td></tr><tr><td>

glide.hub.process.sync.retry.times

</td><td>

Number of times to retry processing of an outbound queue before setting the queue's state to Error.-   Default value: `3`
-   Minimum value: `0`
-   Maximum value: `10`

</td></tr><tr><td>

glide.hub.process.sync.retry.interval.seconds

</td><td>

Time interval, in seconds, between each retry attempt to process an outbound or inbound queue.-   Default value: `60`
-   Minimum value: `0`
-   Maximum value: `300`

</td></tr><tr><td>

glide.hub.process.sync.debug

</td><td>

If set to `true`, log entries will be created in **System Logs** &gt; **System Log** &gt; **All** for Remote Process Sync tables.-   Default value: `false`
-   Minimum value: Not applicable
-   Maximum value: Not applicable

</td></tr><tr><td>

glide.hub.process.sync.record.successful.status

</td><td>

If set to `true`, the Status field for outbound queues will be updated to Success when there are no errors processing the record in the queue.-   Default value: `false`
-   Minimum value: Not applicable
-   Maximum value: Not applicable

</td></tr><tr><td>

glide.hub.process\_sync.inbound\_queue.error.ttl.seconds

</td><td>

Number of seconds that records in the error state can exist in the inbound queue before they expire. The system purges expired records from the queue once a day.**Important:** Records in the error state have not been processed. Review and fix the process definition and its related records. To reprocess records in the inbound queue, set the state to Ready. To ignore these records, set the state to skipped.

 -   Default value: `2592000` \(30 days\)
-   Minimum value: `0`
-   Maximum value: `5184000` \(60 days\)

</td></tr><tr><td>

glide.hub.process\_sync.inbound\_queue.processed.ttl.seconds

</td><td>

Number of seconds that records in the processed state can exist in the inbound queue before they expire. The system purges expired records from the queue once a day.-   Default value: `604800` \(7 days\)
-   Minimum value: `0`
-   Maximum value: `5184000` \(60 days\)

</td></tr><tr><td>

glide.hub.process\_sync.inbound\_queue.ready.ttl.seconds

</td><td>

Number of seconds that records in the ready state can exist in the inbound queue before they expire. The system purges expired records from the queue once a day.**Important:** Records in the ready state have not been processed. Review the system batch size settings to ensure that it can process all incoming records before they expire.

 -   Default value: `2592000` \(30 days\)
-   Minimum value: `0`
-   Maximum value: `5184000` \(60 days\)

</td></tr><tr><td>

glide.hub.process\_sync.inbound\_queue.skipped.ttl.seconds

</td><td>

Number of seconds that records in the skipped state can exist in the inbound queue before they expire. The system purges expired records from the queue once a day.**Important:** Records in the skipped state will not be processed. Review and fix the process definition and its related records. To reprocess records in the inbound queue, set the state to Ready. To ignore these records, leave the state as skipped.

 -   Default value: `604800` \(7 days\)
-   Minimum value: `0`
-   Maximum value: `5184000` \(60 days\)

</td></tr><tr><td>

glide.hub.process\_sync.inbound\_queue.table\_cleaner\_batch\_size

</td><td>

Number of inbound queue records to process per batch when purging expired records.-   Default value: `10000`
-   Minimum value: `1000`
-   Maximum value: `500000`

</td></tr><tr><td>

glide.hub.process\_sync.outbound\_queue.error.ttl.seconds

</td><td>

Number of seconds that records in the error state can exist in the outbound queue before they expire. The system purges expired records from the queue once a day.**Important:** Records in the error state have not been processed. Review and fix the process definition and its related records. To reprocess records in the outbound queue, set the state to Ready. To ignore these records, set the state to skipped.

 -   Default value: `2592000` \(30 days\)
-   Minimum value: `0`
-   Maximum value: `5184000` \(60 days\)

</td></tr><tr><td>

glide.hub.process\_sync.outbound\_queue.processed.ttl.seconds

</td><td>

Number of seconds that records in the processed state can exist in the outbound queue before they expire. The system purges expired records from the queue once a day.-   Default value: `604800` \(7 days\)
-   Minimum value: `0`
-   Maximum value: `5184000` \(60 days\)

</td></tr><tr><td>

glide.hub.process\_sync.outbound\_queue.ready.ttl.seconds

</td><td>

Number of seconds that records in the ready state can exist in the outbound queue before they expire. The system purges expired records from the queue once a day.**Important:** Records in the ready state have not been processed. Review the system batch size settings to ensure that it can process all outgoing records before they expire.

 -   Default value: `2592000` \(30 days\)
-   Minimum value: `0`
-   Maximum value: `5184000` \(60 days\)

</td></tr><tr><td>

glide.hub.process\_sync.outbound\_queue.skipped.ttl.seconds

</td><td>

Number of seconds that records in the skipped state can exist in the outbound queue before they expire. The system purges expired records from the queue once a day.**Important:** Records in the skipped state will not be processed. Review and fix the process definition and its related records. To reprocess records in the outbound queue, set the state to Ready. To ignore these records, leave the state as skipped.

 -   Default value: `604800` \(7 days\)
-   Minimum value: `0`
-   Maximum value: `5184000` \(60 days\)

</td></tr><tr><td>

glide.hub.process\_sync.outbound\_queue.table\_cleaner\_batch\_size

</td><td>

Number of outbound queue records to process per batch when purging expired records.-   Default value: `10000`
-   Minimum value: `1000`
-   Maximum value: `500000`

</td></tr></tbody>
</table>