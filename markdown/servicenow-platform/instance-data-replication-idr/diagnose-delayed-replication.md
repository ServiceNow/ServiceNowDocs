---
title: Discover replication delays in Instance Data Replication
description: Monitor possible data replication issues by using the Instance Data Replication \(IDR\) Monitoring Dashboard.
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resolving errors, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Discover replication delays in Instance Data Replication

Monitor possible data replication issues by using the Instance Data Replication \(IDR\) Monitoring Dashboard.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  To view the time lag on a producer instance, navigate to **Instance Data Replication** &gt; **Monitoring Dashboard**, and check the Active Producer Replication Sets for the following details.

<table id="choicetable_mkm_wmd_skb"><tbody><tr><td id="d75370e70">

**Name**

</td><td>

Name of the producer replication set.

</td></tr><tr><td id="d75370e79">

**Replication Queue Reading Lag**

</td><td>

Time between a record change on the producer instance and the moment it is sent over the outbound replication queue.

</td></tr><tr><td id="d75370e88">

**Status**

</td><td>

Status of a replication set, either active or in error.

</td></tr><tr><td id="d75370e97">

**Status Message**

</td><td>

Message that describes the error status.

</td></tr><tr><td id="d75370e106">

**Message Queue Version**

</td><td>

Version of the Message Queue. Default is V2 \(Hermes\).

</td></tr></tbody>
</table>    To get additional information, view the producer instance xmlstats at `https://<producer-instance-name>/xmlstats.do?include=idr`.

    ![Producer instance xmlstats](../image/xmlstats-producer.png)

    The xmlstats shows:

    -   The *producer\_last\_run* indicates the last time that the replication job ran on the producer instance.
    -   The *last\_message\_sent\_on* indicates the last time that the producer sent updated data to consumers.

        **Note:** The timestamps are GMT.

2.  To view the time lag on a consumer instance, navigate to **Instance Data Replication** &gt; **Monitoring Dashboard** and check the Active Consumer Replication Sets for the following details.

<table id="choicetable_pgt_f12_skb"><tbody><tr><td id="d75370e165">

**Name**

</td><td>

Name of the consumer replication set.

</td></tr><tr><td id="d75370e174">

**Data Lag**

</td><td>

Time between a record change on the producer instance and the moment it is recorded in the consumer instance.

</td></tr><tr><td id="d75370e183">

**Network Lag**

</td><td>

Time between a record change logs in the outbound replication queue and the moment it is recorded in the consumer instance.

</td></tr><tr><td id="d75370e192">

**Status**

</td><td>

Status of a replication set, either active or in error.

</td></tr><tr><td id="d75370e201">

**Status Message**

</td><td>

Message that describes the error status.

</td></tr><tr><td id="d75370e211">

**Message Queue Version**

</td><td>

Version of the Message Queue. Default is V2 \(Hermes\)

</td></tr></tbody>
</table>    To get additional information, view the consumer instance xmlstats at `https://<consumer-instance-name>/xmlstats.do?include=idr`. ![Consumer xmlstats](../image/xmlstats-consumer.png) The xmlstats shows:

    -   The *consumer\_last\_run* indicates the last time that the consumer job ran and received changes from the producer.
    -   The *last\_heartbeat\_received\_on* shows the timestamp when the consumer last received a heartbeat from the producer instance.

        **Note:** The timestamps are GMT.


**Parent Topic:**[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

