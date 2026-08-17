---
title: Instance Data Replication release notes
description: The ServiceNow Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Instance Data Replication release notes

The ServiceNow® Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Yokohama release.

## Instance Data Replication highlights for the Yokohama release

-   Replicate data that's frequently updated in large tables on your instance by scheduling data replication.
-   Queue multiple seeding requests from your producer instance.
-   Reseed missing or mismatched records automatically when creating a data comparison request.

See  for more information.

## Important information for upgrading Instance Data Replication to Yokohama

Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading your replication sets to V2, which uses Hermes Messaging Service. For details, see .

Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is comprised of seven shards, with five days for each shard. All log entries in this table created before the upgrade are automatically truncated.

## New in the Yokohama release

-   **Scheduled seeding**

    Replicate data from a producer to a consumer at scheduled times each day.

-   **Multiple seeding requests**

    Run concurrent seeding requests across multiple replication sets, with up to one active request per set.

-   **Automatically seed missing or mismatched records**

    Automatically seed missing or mismatched records when you create a data comparison request.


## Changed in this release

-   **Seeding request improvements**

    In V2 replication sets, the number of records in a seeding request is now unlimited.

-   **Data comparison improvements**

    In V2 replication sets, the number of records in comparison or reseeding counts is now unlimited.

-   **Reseed missing attachments**

    Attachments are now included in data comparison requests.

-   **Seeding performance improvements**

    Seeding throughput and message queue efficiency has been optimized in IDR.


## Deprecations

Legacy replication sets are planned for deprecation by the Zurich release. To continue replicating data in Zurich, you must upgrade all legacy replication sets to V2. For details on upgrading legacy replication sets to V2 before the upgrade, see .

## Activation information

Instance Data Replication is a ServiceNow AI Platform feature that is available with activation of the IDR \(com.glide.idr\) plugin, which requires a separate subscription. For details, see .

## Related ServiceNow applications and features

-   ****

    Hermes Messaging Service is a multi-tenant, multi-cluster data transport and queuing service built on Apache Kafka that enables your instance to reliably produce and consume large volumes of Kafka events.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-capabilities-rn-landing.md)

