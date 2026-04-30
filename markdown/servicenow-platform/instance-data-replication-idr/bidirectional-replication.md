---
title: Bidirectional replication
description: Bidirectional replication in Instance Data Replication \(IDR\) enables data to flow from a producer instance to a consumer instance and accept data from a consumer instance to flow back to the producer instance.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Explore, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Bidirectional replication

Bidirectional replication in Instance Data Replication \(IDR\) enables data to flow from a producer instance to a consumer instance and accept data from a consumer instance to flow back to the producer instance.

All inserts and changes to records on either instance are sent to the other instance to keep the tables identical on both instances. For example, you can enable bidirectional replication for the Incidents table to keep incident records synchronized between two instances.

To make data flow bi-directionally, the system creates a producer replication set on the consumer instance and a consumer replication set on the producer instance.

![Consumer and producer replication sets are automatically generated to create bi-directional replication.](../image/bi-directional-replication.png "Bi-directional replication")

If you look at the replication sets on the original producer instance, you see the replication set name and the automatically generated consumer instance. It has the same name appended with the suffix, `-<long-number>-reverse`, where `<long-number>` is a randomly generated number. For example, if Test is the producer replication set name, `Test-2034802-reverse` might be the name of the consumer replication set that is automatically created on the same instance. On the original consumer instance, you see the same names. Replication sets with the `reverse` suffix are read-only.

You can verify a consumer on a producer instance and a producer on a consumer instance by running `https://<producer-instance-name>/xmlstats.do?include=idr` and `https://<consumer-instance-name>/xmlstats.do?include=idr` on the producer and consumer instances. In the following image, the original producer instance is on the left and the original consumer instance is on the right.

![Bidirectional replication seen using xmlstats](../image/bi-directional-replication-2.png)

Bidirectional replication has the following limitations:

-   Auto-conflict resolution is unsupported.
-   Merge conflicts happen if producer and consumer instances modify the same record at the same time.

    The most recent update wins, which means that the data on the consumer and producer tables might be different.

-   Bidirectional replication supports the [Number](../reference/adapter-descriptions.md) adapter but none of the other adapters.
-   Bidirectional replication keeps data in sync between producer and consumer instances. However, in some scenarios, avoid using bidirectional replication and use one-way replication instead.
    -   If you plan to use adapters to differentiate data replicated between two instances, use two one-way replication sets to replicate data back and forth instead of using bidirectional sets.
    -   If you need to seed data from one instance to another and vice versa, use two one-way replication sets.
-   With bidirectional replication, records created on the producer instance are replicated to a consumer instance and vice versa. When the record is inserted on the consumer instance and it triggers a business rule that updates the record, that update is not replicated back to the producer instance.

If you must understand the implications of bi-direction and data transfer between instances, see [data privacy in IDR](data-privacy-consumers-idr.md) for more information.

