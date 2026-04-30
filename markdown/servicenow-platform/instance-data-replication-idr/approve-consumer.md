---
title: Manage consumer access to replication data in Instance Data Replication
description: Approve a consumer's request to access replication data in Instance Data Replication \(IDR\).
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Manage consumer access to replication data in Instance Data Replication

Approve a consumer's request to access replication data in Instance Data Replication \(IDR\).

## Before you begin

Role required: admin, idr\_admin

## About this task

You can review consumer access requests for all of your producer replication sets or for a specific producer replication set. The administrators of consumer sets must apply for access before they can receive the replication data.

## Procedure

1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Consumers Pending Approval**.

2.  Select the option for each consumer replication set that you want to approve.

3.  On the Actions on selected rows list, select **Approve**.

    The approved consumer sets start receiving the replicated data.

    **Note:** You can change the Consumer Approval Status to Denied to prevent the consumer from receiving the replicated data.

4.  Approve a consumer access request for a specific producer replication set.

    1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

    2.  Select the producer replication set where you want to approve consumer access.

    3.  Under Related Links, on the **Consumer Subscriptions** tab, select the option for the consumer replication set that you want to approve.

    4.  On the Actions on selected rows list, select **Approve**.

        The approved consumer set starts receiving replicated data.

        **Note:** You can change the Consumer Approval Status to Denied to prevent the consumer from receiving the replicated data.


-   **[Revoke access to replicated data for Instance Data Replication](revoke-consumer-sets.md)**  
Revoke a consumer's access to replicated data if you believe that consumer instance should no longer receive data in Instance Data Replication \(IDR\).
-   **[Restore access to replication data for Instance Data Replication](restore-access.md)**  
Restore Instance Data Replication \(IDR\) access to replicated data by sending a request to the producer replication set admin.

**Parent Topic:**[Configuring Instance Data Replication](../concept/configuring-instance-data-replication.md)

**Related topics**  


[Create a producer replication set in Instance Data Replication](create-p-replication-set.md)

[Create a consumer replication set for Instance Data Replication](create-c-replication-set.md)

[Seed a consumer instance for Instance Data Replication](seed-consumer-instance.md)

[Trigger a workflow after replication using Instance Data Replication](post-replication-actions.md)

[Reconfigure a replication set in Instance Data Replication](change-replication-set-config.md)

[Transform replication data for Instance Data Replication](modify-replicated-data.md)

[Set up bidirectional replication in Instance Data Replication](bi-directional-replication.md)

[Create a discrete producer replication set for Instance Data Replication](discrete-producer-replication-set.md)

