---
title: Monitoring replication status in Instance Data Replication
description: Monitor the status of active producer and consumer replication sets, scheduled jobs, seeding requests, license usage, or scheduled replication through the Instance Data Replication \(IDR\) Monitoring Dashboard.
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Monitoring replication status in Instance Data Replication

Monitor the status of active producer and consumer replication sets, scheduled jobs, seeding requests, license usage, or scheduled replication through the Instance Data Replication \(IDR\) Monitoring Dashboard.

## Accessing the IDR Monitoring dashboard

Users with the admin or idr\_admin role can access the dashboard.

Access the IDR Monitoring dashboard in the following way:

-   Navigate to **Instance Data Replication** &gt; **Monitoring Dashboard**.
-   Choose one of the following: **IDR Overall Monitoring**, **IDR License and Usage SMv2**, or **Scheduled Replication** dashboard.

## IDR Overall Monitoring dashboard

The IDR Overall Monitoring dashboard monitors the following:

-   Active Producer Replication Sets
-   Active Consumer Replications Sets
-   Suite of IDR Scheduled Jobs
-   Producer Seeding Requests Within Last 7 Days
-   Consumer Seeding Requests Within Last 7 Days

![IDR Monitoring dashboard.](../image/IDR-monitoring-dashboard.png "IDR overall monitoring dashboard")

-   **Active Producer Replication Sets**

    The Active Producer Replication Sets monitors your producer replication set status and reports the data lag time between your instance and the replication queue.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the producer replication set|
    |Replication Queue Reading Lag|Time between a record change on the producer instance and the moment that it’s sent over the outbound replication queue|
    |Status|Status of a replication set, either active or in error|
    |Status Message|Message that describes the error status|
    |Message Queue Version|Version of the Message Queue. Default is V2 \(Hermes\).|

-   **Active Consumer Replication Sets**

    Active Consumer Replication Sets monitors your consumer replication set status, reports the network lag time, and reports the data lag time between the producer instance and consumer instance.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the consumer replication set.|
    |Data Lag|Time between a record change on the producer instance and the moment that it’s recorded in the consumer instance.|
    |Network Lag|Time between a record change log in the outbound replication queue and the moment that it’s recorded in the consumer instance.|
    |Status|Status of a replication set, either active or in error.|
    |Status Message|Message that describes the error status.|
    |Message Queue Version|Version of the Message Queue. Default is V2 \(Hermes\).|

-   **Suite of IDR Scheduled Jobs**

    The suite of IDR scheduled jobs poll for data changes, requests, and check the health of your producer and consumer instances. You can monitor the following jobs:

    |Jobs|Description|
    |----|-----------|
    |Hermes Metrics Collection|Collects metrics related to the Hermes Messaging Service.|
    |Hermes Periodic Purge|Cleans obsolete cached data in the Hermes API.|
    |Hermes Topics Util|Synchronizes topics across Hermes clusters. Initially, topics are created in a single Hermes cluster. This job detects new topics and creates the same topics in the remaining Hermes clusters.|
    |IDRConsumerJob|Polls for record changes and seeding requests on the consumer instance in 15-second intervals.|
    |IDRDeltaConsumerJob|Beginning in the San Diego release, when a consumer instance subscribes to a producer instance that is outside the local datacenter, the IDRDeltaConsumerJob job is created on the producer instance. The function is the same as the IDRConsumerJob. The three-letter code denotes the datacenter location.|
    |IDRHermesDeltaConsumer|Polls for consumer record changes from the Hermes delta topic in 15-second intervals.|
    |IDRHeartBeatJob|Updates information about the health of every active producer or consumer set.|
    |IDRMetadataConsumerJob|Polls for metadata record changes on the consumer instance in 15-second intervals.|
    |IDRProducerJob|Polls for new, updated, or deleted records in the data replication queue for a producer instance in 15-second intervals.|
    |IDRSeedingProducerJob|Checks for new seeding requests coming from consumer instances.|

    **Note:** You can set when your IDR scheduled jobs run and configure a periodic trigger that specifies how often the job runs.

    |Field|Description|
    |-----|-----------|
    |Name|Scheduled job name.|
    |Next Action|Date and time when the job next runs.|
    |Trigger type|Job that you can configure to run daily, weekly, monthly, periodically, once, on-demand, or business calendar start or end date. The trigger can repeat daily, hourly, by minute, or by second.|
    |Job ID|ID of the scheduled job.|
    |State|State of the job, for example, ready.|

-   **Producer Seeding Request Within Last 7 Days**

    You can monitor the status of a producer seeding request within the last seven days.

    |Field|Description|
    |-----|-----------|
    |Replication Set|Producer set and the consumer set.|
    |Status|Status of the seeding request. The status can be completed, in progress, or failed.|
    |Start Time|Time that the seeding begins.|
    |End Time|Time that the seeding ends.|
    |Percent Complete|Percentage of the seeding request job that is complete.|

-   **Consumer Seeding Request Within Last 7 Days**

    You can monitor the status of a consumer seeding request within the last seven days.

    |Field|Description|
    |-----|-----------|
    |Replication Set|Corresponding consumer set.|
    |Status|Status of the seeding request. The status can be completed, in progress, or failed.|
    |Start Time|Time that the seeding begins.|
    |End Time|Time that the seeding ends.|
    |Percent Complete|Percentage of the seeding request job that is complete.|

-   **IDR dashboard properties**

    You can access the IDR dashboard properties by navigating to **Instance Data Replication** &gt; **Properties**.

    You can change the following properties on your dashboard:

    |Property field|Description|
    |--------------|-----------|
    |Minutes of lag before the Data Lag field are highlighted in red on the IDR Monitoring Dashboard|**Data Lag** field that is part of the Active Consumer Replication set. If the actual lag time is greater than the time threshold that you set, the system highlights the field. The default is 15 minutes.|
    |Minutes of lag before the Network Lag field is highlighted in red on the IDR Monitoring Dashboard|**Network Lag** field that is part of the Active Consumer Replication set. If the actual lag time is greater than the time threshold that you set, the system highlights the field. The default is 15 minutes.|
    |Minutes of lag before the system highlights the Replication Queue Reading Lag field in red on the IDR Monitoring Dashboard|**Replication Queue Reading Lag** field that is part of the Active Consumer Replication set. If the actual lag time is greater than the time threshold that you set, the system highlights the field. The default is 15 minutes.|

    **Note:** You can set the colors on the fields through the personalize list columns \(v\_idr\_dashboard\_list.do\).


## IDR License and Usage SMv2 dashboard

The IDR License and Usage SMv2 dashboard monitors the following:

-   Subscriber Sent Messages
-   Subscriber Received Messages
-   IDR License Details
-   IDR Messages Sent
-   IDR Messages Received

-   **Subscriber Sent Messages**

    The number of messages each subscriber instance sent, by month.

    ![Subscriber sent messages.](../image/messages-sent.png "Subscriber messages sent")

-   **Subscriber Received Messages**

    The number of messages each subscriber instance received, by month.

    ![Subscriber received messages.](../image/subscriber-received-messages.png "Subscriber messages received")

-   **IDR License Details**

    You can monitor the status of a consumer seeding request within the last seven days.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the IDR license.|
    |Type|Type of subscription: **Per-User** for user subscriptions, **Capacity** for data driven subscriptions, or **Unrestricted User** for subscriptions capped by the maximum user count.|
    |Category|License category: ServiceNow license or Store App license.|
    |Start date|Start of the licensing period.|
    |End date|End of the licensing period.|
    |Display only|Does not support resource allocation or monitoring.|
    |Purchased|Number of purchased licenses.|
    |Allocated|Number of allocated licenses.|

-   **IDR Messages Sent**

    The number of messages sent, per license, monthly.

    ![IDR messages sent.](../image/messages-sent.png "IDR messages sent")

-   **IDR Messages Received**

    The number of messages received, per license, monthly.

    ![IDR messages received.](../image/message-received.png "IDR messages received")


## Scheduled Replication dashboard

Monitor the status of scheduled replication requests within a specific time period. For example, you might track the count of failures for a specific scheduled replication set, or compare the number of scheduled requests to the number of completed requests. You can view the following scheduled replication details:

-   Scheduled Sets
-   Scheduled Requests
-   Completed
-   Failed
-   Overall Request Status
-   Replication Set Status Overview

-   **Scheduled Sets**

    The total count of scheduled replication sets created in the selected date range.

-   **Scheduled Requests**

    The total count of scheduled request runs queued in the selected date range.

-   **Completed**

    The total count of scheduled request runs that completed in the selected date range.

-   **Failed**

    The total count of scheduled request runs that failed to complete or encountered an error in the selected date range.

-   **Overall Request Status**

    A donut chart showing status distribution for scheduled requests in the selected date range.

-   **Replication Set Status Overview**

    A table showing the count for each status in the selected date range.


**Parent Topic:**[Administering Instance Data Replication](administering-instance-data-replication.md)

**Related topics**  


[Manage consumer access to replication data in Instance Data Replication](../task/approve-consumer.md)

[Comparing replicated data between instances in Instance Data Replication](comparing-replicated-data.md)

[Deploying a replication configuration from one instance to another in Instance Data Replication](copying-replication-configuration.md)

[Cloning options with Instance Data Replication](cloning-with-instance-data-replicaton.md)

[Monitoring queues in Instance Data Replication](idr-queue-dashboard.md)

[Avoiding insert and update errors in Instance Data Replication](preventing-insert-update-errors.md)

[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

