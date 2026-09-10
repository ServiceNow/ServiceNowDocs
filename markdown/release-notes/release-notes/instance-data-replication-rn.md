---
title: Instance Data Replication release notes
description: The ServiceNow Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Yokohama release.The ServiceNow Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Instance Data Replication release notes

The ServiceNow® Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Yokohama release.

## About Instance Data Replication

-   Replicate data that's frequently updated in large tables on your instance by scheduling data replication.
-   Queue multiple seeding requests from your producer instance.
-   Reseed missing or mismatched records automatically when creating a data comparison request.

See [Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/instance-data-replication.md) for more information.

## Activation and other requirements

-   **Activation information**

    Instance Data Replication is a ServiceNow AI Platform feature that is available with activation of the IDR \(com.glide.idr\) plugin, which requires a separate subscription. For details, see [Request an Instance Data Replication subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/request-instance-data-replication.md).

-   **Upgrade information**

    Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading your replication sets to V2, which uses Hermes Messaging Service. For details, see [Upgrading legacy replication sets to V2 in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/upgrading-legacy-replication-sets-v2.md).

    Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is comprised of seven shards, with five days for each shard. All log entries in this table created before the upgrade are automatically truncated.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-capabilities-rn-landing.md)

## Yokohama

The ServiceNow® Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Yokohama release.

### What's new

-   **[Scheduled seeding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/set-up-scheduled-replication-idr.md)**

    Replicate data from a producer to a consumer at scheduled times each day.

-   **[Multiple seeding requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/seed-consumer-instance.md)**

    Run concurrent seeding requests across multiple replication sets, with up to one active request per set.

-   **[Automatically seed missing or mismatched records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/compare-replicated-data.md)**

    Automatically seed missing or mismatched records when you create a data comparison request.


### What's changed

-   **[Seeding request improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/exploring-instance-data-replication.md)**

    In V2 replication sets, the number of records in a seeding request is now unlimited.

-   **[Data comparison improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/comparing-replicated-data.md)**

    In V2 replication sets, the number of records in comparison or reseeding counts is now unlimited.

-   **[Reseed missing attachments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/comparing-replicated-data.md)**

    Attachments are now included in data comparison requests.

-   **[Seeding performance improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/seed-consumer-instance.md)**

    Seeding throughput and message queue efficiency has been optimized in IDR.


### What's deprecated or removed

Legacy replication sets are planned for deprecation by the Zurich release. To continue replicating data in Zurich, you must upgrade all legacy replication sets to V2. For details on upgrading legacy replication sets to V2 before the upgrade, see [Upgrading legacy replication sets to V2 in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/upgrading-legacy-replication-sets-v2.md).

