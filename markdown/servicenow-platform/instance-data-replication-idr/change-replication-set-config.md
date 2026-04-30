---
title: Reconfigure a replication set in Instance Data Replication
description: If you must change or update your original replication set, reconfigure Instance Data Replication \(IDR\) replication sets on the producer instance.
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Reconfigure a replication set in Instance Data Replication

If you must change or update your original replication set, reconfigure Instance Data Replication \(IDR\) replication sets on the producer instance.

## Before you begin

Role required: idr\_admin or admin

## About this task

After activating a revised producer replication set, update the producer replication set name, shared key, producer ID, and producer set ID on each consumer instance.

Note the following important information:

-   Make sure that a seeding request is not in progress before you reconfigure a producer instance. Check the consumer replication sets seeding requests status.
-   If you make a change to the producer replication set, you must re-synchronize the consumer replication set. On the consumer instance, click **Synchronize Replication Entries**, and then click **Activate**.

## Procedure

1.  Reconfigure a producer instance:

    1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

    2.  Select a producer replication set and make one or more of the following changes to the set:

        -   To add a table to the set, on the **Replication Entries** tab, click **New**.
        -   On the **Replication Entries** tab, click a replication set. In the Replication Entry form, modify the columns that are included in the replication set, and click **Update**.
        -   To remove the table from the replication set, on the **Replication Entries** tab, click a replication set and click **Delete**.
        -   To change the shared encryption key, click **Generate New Shared Key**.

            Only generate new shared keys when you discover that they are compromised or if you want to stop sending data to a consumer. After changing the encryption key on the producer instance, consumers that have the Consumer Approved Status of Denied must reapply for access to the producer replication set. For more information, see [Grant access to replication data](approve-consumer.md).

        These changes stop replication and produce this status message on the consumer instance: `Producer Replication Set configuration has been modified`.

2.  Navigate to **Instance Data Replication** &gt; **Consumer Replication Sets** and click the consumer replication set and each consumer instance that you want to update with the changes made on the producer.

    The status of the replication set is Replication Error. The following table lists the action to take according to the status message.

    |Status Message|Action|
    |--------------|------|
    |**Approval was denied by producer instance.**|The producer changed the shared key and that revokes this consumer's access to the replication data. Replication stops. Click the **Request shared key** related link. The producer must approve your request. For more information, see [Grant access to replication data](approve-consumer.md). If the consumer's access is not revoked, replication continues. Do nothing on the consumer instance.|
    |**Producer Replication Set configuration has been modified.**|The producer added or subtracted tables or table columns in the producer replication set. Replication stops. Click **Synchronize Replication Entries** and then click **Activate**. The system keeps the tables on the consumer instance that the producer is no longer replicating.|

3.  Discard the entire IDR configuration and start over, delete the replication set on the producer and the consumer.

    -   To delete a producer replication set from the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**. Click the producer replication set that you want to delete, and click **Delete**.
    -   To delete a consumer replication set on a consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**. Click the consumer replication set that you want to delete, and click **Delete**.

**Parent Topic:**[Configuring Instance Data Replication](../concept/configuring-instance-data-replication.md)

**Related topics**  


[Create a producer replication set in Instance Data Replication](create-p-replication-set.md)

[Create a consumer replication set for Instance Data Replication](create-c-replication-set.md)

[Seed a consumer instance for Instance Data Replication](seed-consumer-instance.md)

[Trigger a workflow after replication using Instance Data Replication](post-replication-actions.md)

[Manage consumer access to replication data in Instance Data Replication](approve-consumer.md)

[Transform replication data for Instance Data Replication](modify-replicated-data.md)

[Set up bidirectional replication in Instance Data Replication](bi-directional-replication.md)

[Create a discrete producer replication set for Instance Data Replication](discrete-producer-replication-set.md)

