---
title: Instance Data Replication release notes
description: The ServiceNow Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Instance Data Replication release notes

The ServiceNow® Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Australia release.

## IDR highlights for the Australia release

View updated diagnostic test descriptions and results on the redesigned IDR Diagnostics page.

See Instance Data Replication for more information.

## Important information for upgrading IDR to Australia

Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is composed of seven shards, with five days for each shard. All log entries in this table that are created before the upgrade are automatically truncated.

## New in the Australia release

-   **IDR Diagnostics page improvements**

    Access detailed test descriptions and results on the redesigned IDR Diagnostics page.


## Activation information

IDR is a ServiceNow AI Platform feature that is available with activation of the IDR \(com.glide.idr\) plugin, which requires a separate subscription. For details, see Request an Instance Data Replication subscription.

## Related ServiceNow applications and features

-   **Hermes Messaging Service**

    Hermes Messaging Service is a multi-tenant, multi-cluster data transport and queuing service built on Apache Kafka that enables your instance to produce and consume large volumes of Kafka events reliably.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

