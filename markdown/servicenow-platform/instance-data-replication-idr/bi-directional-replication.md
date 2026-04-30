---
title: Set up bidirectional replication in Instance Data Replication
description: Replicate updated data on a consumer instance to the producer instance using bidirectional replication in Instance Data Replication \(IDR\).
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Set up bidirectional replication in Instance Data Replication

Replicate updated data on a consumer instance to the producer instance using bidirectional replication in Instance Data Replication \(IDR\).

## Before you begin

Role required: idr\_admin or admin

## Procedure

1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**:

    -   Click **New** for a new replication set
    -   Click on a producer replication set.
2.  Check the **Bi-Directional** checkbox to enable bi-direction for your producer replication set.

    Bi-directional replication enables changes to records that are made on the consumer instance to propagate to the producer instance.

    **Note:** Bi-directional replication works for records that originate on the producer or consumer.

3.  On a consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets** and click a consumer replication set that is connected to the producer replication set.

4.  On the Consumer Replication Set pane, click the **Synchronize Replication Entries** related link to update the Consumer Replication Entries configuration on the consumer to match the configuration on the producer.


## Result

Data that is updated on this consumer instance automatically replicates on the producer instance, which then replicates the updates to its other consumer instances.

**Parent Topic:**[Configuring Instance Data Replication](../concept/configuring-instance-data-replication.md)

**Related topics**  


[Create a producer replication set in Instance Data Replication](create-p-replication-set.md)

[Create a consumer replication set for Instance Data Replication](create-c-replication-set.md)

[Seed a consumer instance for Instance Data Replication](seed-consumer-instance.md)

[Trigger a workflow after replication using Instance Data Replication](post-replication-actions.md)

[Reconfigure a replication set in Instance Data Replication](change-replication-set-config.md)

[Manage consumer access to replication data in Instance Data Replication](approve-consumer.md)

[Transform replication data for Instance Data Replication](modify-replicated-data.md)

[Create a discrete producer replication set for Instance Data Replication](discrete-producer-replication-set.md)

