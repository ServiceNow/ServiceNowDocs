---
title: Discrete replication
description: Distinguish consumers in Instance Data Replication \(IDR\) using discrete mapping in a producer replication set.
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Discrete replication

Distinguish consumers in Instance Data Replication \(IDR\) using discrete mapping in a producer replication set.

Every producer replication set has a unique relationship with each consumer subscription. One way of distinguishing this relationship is by mapping discrete field values for producer replication sets.

Once you enable discrete mapping, you can define for each outbound entry of a replication set a discrete value field. An administrator of the producer replication set can define the mapping of each consumer subscription by the setting this discrete value.

For example, you might have an ACME corporation as the producer instance, and have consumer subscribers of ACME US and ACME Europe. You could set a discrete value of **region** on the outbound replication entries for the incident table. While both of these entries reference the same company table, a rule set for the discrete value can display US for ACME US, and Europe for ACME Europe.

If you have bi-direction enabled with discrete mappings, different consumer subscriptions:

-   Should never receive records sent from other consumer subscribers
-   Should never receive records from a producer intended for other consumers subscribers

With bidirectional replication, records created on a consumer instance are replicated to the producer instance and vice versa. When the consumer replicates a record to the producer, the consumer's discrete field value that you defined in the producer replication set overrides the discrete field value in the consumer record if it's different. For example, say you define a discrete mapping using separate regions for each consumer instance as follows:

|Consumer instance|Region|
|-----------------|------|
|Consumer instance A|Asia|
|Consumer instance B|Europe|
|Consumer instance C|USA|

When a record is manually added to consumer instance B with the Region field set to Asia, bi-directional replication sends the record from the consumer to the producer to be inserted, but the region field is overwritten and the value is changed to Europe. The discrete value that is defined in the producer replication set is used instead.

For details on the implications with discrete mappings and data transfer between instances, see [data privacy in IDR](data-privacy-consumers-idr.md).

