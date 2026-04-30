---
title: Producer Event Notification Framework developer guide
description: The Producer Event Notification Framework for Telecommunications, Media, and Technology enables the external distribution of events, such as trouble tickets, using a message-bus implemented in your network.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Developer guides, API implementation and reference]
---

# Producer Event Notification Framework developer guide

The Producer Event Notification Framework for Telecommunications, Media, and Technology enables the external distribution of events, such as trouble tickets, using a message-bus implemented in your network.

The Producer Event Notification Framework supports two different message-bus use cases:

1.  Publishing events through the Hermes Messaging Service: If you plan to publish events using Hermes Kafka, you must configure the Producer Event Notification Framework for the Kafka message-bus. You can only use this message-bus for cloud-based instances. For details, see [Configure the Producer Event Notification Framework to use the Hermes Messaging Service](../task/prod_evt_not-dev_gd-cfg_herm_bus.md).

    For additional information on how to publish trouble ticket notifications using Hermes, see [Producing outbound API notifications using Hermes](https://www.servicenow.com/docs/access?context=hermes-stream-connect-kafka-workflow&version=yokohama&pubname=yokohama-proactive-service-exp-workflows&ft:locale=en-US).

    **Note:** Before you are able to implement this use case, you must already have the Hermes Messaging Service installed and configured on your instance. For details, see [Hermes Messaging Service](https://www.servicenow.com/docs/access?context=hermes-messaging-service&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

2.  Publishing events through the open message bus: If your instance uses a custom message-bus, you must configure the Producer Event Notification Framework to use the open message bus to send events from your ServiceNow instance to consumers on your network. Both cloud-based and on-premise ServiceNow instances can publish events through the open message bus. For details, see [Configure the Producer Event Notification Framework to use the Open Message Bus](../task/prod_evt_not-dev_gd-cfg_open_bus.md).

    For additional information on how to publish trouble ticket notifications using the open message bus, see [Producing outbound API notifications using the open message bus](https://www.servicenow.com/docs/access?context=trouble-ticket-workflow-using-pub-sub-model&version=yokohama&pubname=yokohama-proactive-service-exp-workflows&ft:locale=en-US).


This document describes the system configuration that must be performed, including the script includes that must be overridden to deploy these message-bus implementations in your ServiceNow ecosystem.

## Producer system properties

The following table lists the properties within your ServiceNow instance that control the functionality of the Producer Event Notification Framework. Review the default values of these properties and if necessary, modify them for your specific implementation. To modify these properties, in the ServiceNow UI go to **All** &gt; **System Properties** &gt; **All Properties**.

<table id="table_v4w_33k_yzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_api\_notif\_mgmt.event.log

</td><td>

Level of logging to written to the debug logs.Valid values:

-   alert
-   crit
-   debug
-   emerg
-   err
-   info
-   notice
-   warning

Default: err

</td></tr><tr><td>

sn\_api\_notif\_mgmt.glide.​mutex.​script.​maxspins

</td><td>

Maximum number of attempts to acquire a mutex lock on the records in the inbound queue.Default: 100

</td></tr><tr><td>

sn\_api\_notif\_mgmt.​glide.​mutex.​script.​spinwait

</td><td>

Time to wait between attempts to acquire a lock on the records in the inbound queue.Unit: Milliseconds

Default: 100

</td></tr><tr><td>

sn\_api\_notif\_mgmt.​inboundqueue.​batch.​limit

</td><td>

Number of records that the scheduler will pull and process from the inbound queue at one time \(one batch\).Default: 200

</td></tr><tr><td>

sn\_api\_notif\_mgmt.​inboundqueue.maxrecords

</td><td>

Maximum number of records that the scheduler will pull from the inbound queue for one scheduler run. This value is used in conjunction with the **sn\_api\_notif\_mgmt.inboundqueue.batch.limit** parameter.For example, if the batch limit is set to 50 and the maxrecords is set to 200, and the number of records that are in the inbound queue is 130, the scheduler would pull three different batches of records in a single run; two with 50 records and one with 30 records. If the number of records in the inbound queue is 220, the scheduler would pull four batches of 50 records and the remaining 20 records would not be processed until the next time the scheduler runs.

When setting this value, you must also consider the time that it will take for the scheduler to process multiple batches and set the **sn\_api\_notif\_mgmt.schedule.max.runtime** value accordingly.

Default: 200

</td></tr><tr><td>

sn\_api\_notif\_mgmt.​publisher\_message\_bus\_configuration

</td><td>

Defines whether messages are published using the Hermes Messaging Service, the open message bus, or both message buses.Valid values:

-   hermes = Hermes Messaging Service
-   openMessageBus = open message bus
-   both = Event/message is sent out on both message buses.

Default: openMessageBus

</td></tr><tr><td>

sn\_api\_notif\_mgmt.​schedule.​max.​runtime

</td><td>

Max time that a schedule job can run before it fails and reports an error.Unit: Milliseconds

Default: 90,000

</td></tr></tbody>
</table>