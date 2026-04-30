---
title: Data privacy in Instance Data Replication
description: The ability of replication sets to host multiple remote consumers in Instance Data Replication \(IDR\) means that there are potential data privacy issues to consider.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Data privacy in Instance Data Replication

The ability of replication sets to host multiple remote consumers in Instance Data Replication \(IDR\) means that there are potential data privacy issues to consider.

Replications sets in IDR serve multiple instances with multiple consumers. A replication set can have a single customer or can have multiple customers. A consumer could also be located within the same geographic region as the producer or located in a different geographical region.

Depending on how you configure your replication set, you can have data sharing internally, between offices of the same company, or externally, extending across multiple companies. You can also confine data sharing to a single location or region, or you can share data across all regions.

An active replication set occurs after the producer instance administrator approves a consumer subscription. An active replication set involves data transfer, which could include transfer of personal data, between geographical regions. The data transfer between different geographical regions could subject the data to differing personal data regulations.

During the approval process, if IDR determines that the consumer and producer instances are in different geographical regions, it alerts the producer before activation. This alert should make administrators aware of the potential for differing data transfer regulations between regions.

Once a replication set is active, a replication set with multiple consumers might have specific discrete rules which direct specific data to specific consumers. Any modification of a discrete rule on an active replication set which spans multiple consumers has the potential to expose data. This data exposure can include personal data, which might be viewable by unintended consumers that subscribe to the replication set.

If you set bi-direction between a producer and consumer instance, the consumer can originate data that shares back to the producer instance. This data can also potentially reach any other consumer that is part of the replication set.

**Parent Topic:**[Instance Data Replication reference](reference-instance-data-replication.md)

**Related topics**  


[Adapter descriptions for Instance Data Replication](../reference/adapter-descriptions.md)

[Excluded tables in Instance Data Replication](../reference/IDR-excluded-tables.md)

[Domain separation and IDR](../reference/instance-data-replication-domain-separation.md)

[Instance Data Replication system properties](../reference/instance-data-replication-properties.md)

[Instance Data Replication roles](../reference/instance-data-replication-roles.md#)

