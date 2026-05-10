---
title: Using the producer framework for outbound notifications
description: The producer framework picks the event from the ServiceNow instance and sends the outbound notification to the external system. You can consume the details of the notification from the messaging service that is installed in your external system.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Handling API notifications, Use, Product Support for Technology]
---

# Using the producer framework for outbound notifications

The producer framework picks the event from the ServiceNow instance and sends the outbound notification to the external system. You can consume the details of the notification from the messaging service that is installed in your external system.

## System properties

You must configure the system properties to use the producer framework for outbound notification. The following table explains the list of system properties that are set for the scheduled jobs.

<table id="table_y3w_k2j_b1c"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Type

</th></tr></thead><tbody><tr><td>

sn\_api\_notif\_mgmt.event.log

</td><td>

Level of logging to be written to the debug logs. You can select the following logging levels:

-   **emerg**: Total failure.
-   **alert**: System corruption of a database, for example.
-   **crit**: Typically used for hardware errors, for example.
-   **err**: Any errors.
-   **warning**: Any warnings
-   **notice**: Possible action required but not essential.
-   **Info**: No action required.
-   **debug**: Generally not used except for capturing everything for fault-finding.

 Default value: **err**

</td><td>

String

</td></tr><tr><td>

sn\_api\_notif\_mgmt.publisher\_message\_bus\_configuration

</td><td>

Defines whether messages are published using the Hermes Messaging Service, the Open Message Bus, or both message buses. You can use the following values:-   **openMessageBus**
-   **hermes**
-   **both**

Default value: **openMessageBus**

</td><td>

String

</td></tr><tr><td>

sn\_api\_notif\_mgmt.inboundqueue.maxrecords

</td><td>

Maximum number of records that the scheduler will pull from the inbound queue for one scheduler run. This value is used in conjunction with the **sn\_api\_notif\_mgmt.inboundqueue.batch.limit** parameter.-   Default value: **200**
-   Other possible values: As needed

For example, if the batch limit is set to 50 and the maxrecords is set to 200, and if the number of records that are in the inbound queue is 130, then the scheduler would pull three different batches of records in a single run; two with 50 records and one with 30 records. If the number of records in the inbound queue is 220, the scheduler would pull four batches of 50 records and the remaining 20 records would not be processed until the next time the scheduler runs.

When setting this value, you must also consider the time that it will take for the scheduler to process multiple batches and set the sn\_api\_notif\_mgmt.schedule.max.runtime value accordingly.

</td><td>

Integer

</td></tr><tr><td>

sn\_api\_notif\_mgmt.inboundqueue.batch.limit

</td><td>

Number of records that the scheduler pulls and processes from the inbound queue at one batch.-   Default value: **200**
-   Other possible values: As needed

</td><td>

Integer

</td></tr><tr><td>

sn\_api\_notif\_mgmt.glide.mutex.script.maxspins

</td><td>

Maximum number of attempts to acquire a mutex lock in the inbound queue records.-   Type: Integer
-   Default value: **100**
-   Other possible values: As needed

</td><td>

Integer

</td></tr><tr><td>

sn\_api\_notif\_mgmt.schedule.max.runtime

</td><td>

The maximum time, in milliseconds, that the scheduled job can run before it fails and reports an error.-   Type: Integer
-   Default value: **90000**
-   Other possible values: As needed

</td><td>

Integer

</td></tr><tr><td>

sn\_api\_notif\_mgmt.glide.mutex.script.spinwait

</td><td>

Maximum Time, in milliseconds, to wait between attempts to acquire a mutex lock on the records in the inbound queue.-   Type: Integer
-   Default value: **100**
-   Other possible values: As needed

</td><td>

Integer

</td></tr></tbody>
</table>## Producer framework workflow

When the system pushes an event to the staging table, the following steps take place as part of the producer framework mechanism:

1.  The scheduler picks a number of records at a preconfigured interval and then sends Glide snapshots to the event processor.
2.  The system converts the Glide snapshot to a TMF 688 complaint event payload based on the event type.

    To learn more about the methods used to define and generate the TMF-compliant payloads for trouble ticket events, see [TopicAPIUtilsOOB - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/TopicAPIUtilsOOBAPIScoped.md).

3.  The system checks whether the notification configuration is intended for Hermes Kafka or the open message bus.

    To learn more about configuring the producer event notification framework, see [Producer Event Notification Framework developer guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/prod_evt_not-dev_guide-overview.md).


**Related topics**  


[Producing outbound API notifications using Hermes](hermes-stream-connect-kafka-workflow.md)

[Producing outbound trouble ticket notifications using the open message bus](trouble-ticket-workflow-using-pub-sub-model.md)

