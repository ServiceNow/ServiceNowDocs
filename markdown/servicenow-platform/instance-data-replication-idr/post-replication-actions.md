---
title: Trigger a workflow after replication using Instance Data Replication
description: Use platform business rules to trigger workflows after replication using Instance Data Replication \(IDR\).
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Trigger a workflow after replication using Instance Data Replication

Use platform business rules to trigger workflows after replication using Instance Data Replication \(IDR\).

## Before you begin

Role required: idr\_admin or admin

## About this task

Inserts and updates that are replicated to a consumer instance can trigger business rules configured on the target table. A business rule is a server-side script that is associated with a table. Use business rules to trigger workflows that are associated with replications, such as sending a notification or validating the replicated data.

Business rules are part of the ServiceNow AI Platform. For more information, see [Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Procedure

1.  On a consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets** and click a consumer replication set.

2.  On the **Inbound Entries** tab, click a replication set table.

3.  Select the **Run Business Rule** option.

4.  Repeat this procedure for the other tables in the replication set.

5.  Click **Update**.

    IDR invokes the business rules that are associated with the specified table after replicating the data to the table.


**Parent Topic:**[Configuring Instance Data Replication](../concept/configuring-instance-data-replication.md)

**Related topics**  


[Create a producer replication set in Instance Data Replication](create-p-replication-set.md)

[Create a consumer replication set for Instance Data Replication](create-c-replication-set.md)

[Seed a consumer instance for Instance Data Replication](seed-consumer-instance.md)

[Reconfigure a replication set in Instance Data Replication](change-replication-set-config.md)

[Manage consumer access to replication data in Instance Data Replication](approve-consumer.md)

[Transform replication data for Instance Data Replication](modify-replicated-data.md)

[Set up bidirectional replication in Instance Data Replication](bi-directional-replication.md)

[Create a discrete producer replication set for Instance Data Replication](discrete-producer-replication-set.md)

