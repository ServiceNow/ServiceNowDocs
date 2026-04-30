---
title: Create a consumer replication set for Instance Data Replication
description: Create a consumer replication set to specify the tables and columns on a consumer instance that receive the producer data in Instance Data Replication \(IDR\).
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a consumer replication set for Instance Data Replication

Create a consumer replication set to specify the tables and columns on a consumer instance that receive the producer data in Instance Data Replication \(IDR\).

## Before you begin

-   [Create and activate a producer replication set](create-p-replication-set.md).
-   Reduce latency by ensuring that the producer and consumer instances are in the same geographic region and belong to the same customer. You can replicate data between instances across different geographic regions. However, replication latency can occur when instances are located in data centers in separate regions.
-   Role required: idr\_admin or admin

## About this task

Create a consumer replication set and link it to a producer replication set. IDR replicates data from the producer to the tables and table columns of the same name on the consumer instance. The administrator of the producer replication set must grant the consumer instance access to the replication data.

If the producer replication set administrator generates a new encryption key, the encryption key value that is stored in the consumer replication set might not automatically update. If it does not update, replication stops. To restore access, see [Restore access to replication data](restore-access.md).

## Procedure

1.  On a consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Producer Instance URL|URL of the producer instance. For example, https://&lt;producer\_instance&gt;.servicenow.com.|
    |Producer Replication Set Name|Name of the consumer replication set. The name on the consumer must match the name on the producer. Obtain the name from the producer administrator.|
    |Description|Description of the purpose of the replication.|

4.  Select **Submit**.

    The list of all consumer replication sets appears. The system sends a request to the producer replication set administrator to approve or deny your request for a shared encryption key.

    **Warning:** Do not change any of the values.

5.  In the list of all consumer replications sets, select the replication set.

    The Consumer Replication Set displays the replication set information.

    ![Consumer replication set.](../image/consumer-rep-entries.png)

    The Consumer Approval Status shows Approval Pending. The producer administrator must approve your request to be a consumer.

    **Note:** If you receive an error saying that your encryption key does not work, contact Customer Service and Support.

6.  Wait until the producer administrator approves the request.

    The Consumer Approval Status changes to Approved. For more information, see [Grant access to replication data](approve-consumer.md).

7.  Refresh the browser page.

    The system replaces the **Request Producer Approval** button with the **Activate** button.

8.  To update the Consumer Replication Entries configuration on the consumer to match the configuration on the producer after you receive confirmation, click the **Synchronize Replication Entries** related link.

    If you do not see this option, refresh the page.

    A dialog box confirms the synchronization. The tables that you select for replication in the producer replication set are replicated in the consumer replication set and appear on the **Inbound Entries** tab. The initial seeding of all the table data may take some time. After initial seeding, only data updates are replicated to consumer replication sets. For more information about seeding, see [Seed a consumer instance.](seed-consumer-instance.md)

9.  To configure who receives replication notifications, click the **Notification Configuration** related link.

10. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |When to send|Trigger for sending a notification.|
    |Who will receive|Person who receives the notifications.|
    |What it will contain|Notification content.|

11. Select **Update**.

12. Activate the consumer replication set.

    1.  Select the consumer replication set that you want to activate.

    2.  Open the **Inbound Entries** tab.

    3.  Select **Activate**.

    After some time, the Status is Active Replication, and the **Partial Seeding** and **Full Seeding** buttons are displayed. With both seeding options, IDR generates audit trails of all record updates. If you encounter an error during seeding, see [Fix seeding errors](fix-seeding-errors.md). For more information about seeding, see [Seed a consumer instance](seed-consumer-instance.md).

13. To discard your seeding request before clicking **Activate**:

    1.  On the **Seeding Requests** tab, click a seeding request.

    2.  On the Seeding Request form, click **Cancel**.

14. To modify the behavior of the consumer, click a source table name on the **Inbound Entries** tab.

    1.  To preserve the user name in an Activities entry, select the **Preserve Modified By** option on the Inbound Entry form.

        For example, the **Work Notes** field is an Activity type in change request records. When a user updates a change request, the work note moves into the Activities stream.

        -   If you do not select **Preserve Modified By**, Instance Data Replication appears in place of the user name in the consumer records.
        -   If you select **Preserve Modified By**, the user who updated the change request is identified in the entry and the system prepends IDR to their name.
        ![Preserve modified by.](../image/preserved-modified-by-2.png)

        When replicating changes, **Preserve modified by** affects values for the **Updated by**, **Updated**, **Created**, and **Created by** system fields:

        -   When **Preserve modified by** is enabled and you include system fields in the producer replication entry, producer system field values are replicated to the consumer records. If you do not include system fields in the producer replication entry, default system values from the consumer instance are used instead.
        -   When **Preserve modified by** is disabled, default system field values from the consumer instance are used, which means they may not match the system field values in records on the producer.
        When seeding data, the **Preserve modified by** setting has no effect:

        -   If you include system fields in the producer replication entry, producer system field values appear in the seeded records.
        -   If you do not include system fields in the producer replication entry, null values appear in the system fields for seeded records.
    2.  To run business workflows after a replication, select the **Run Business Rule** option.

        A business rule is a server-side script that is associated with a table. Use business rules to trigger workflows that are associated with replications, such as sending a notification or validating the replicated data. For more information, see [Trigger workflows after replication](post-replication-actions.md).

    3.  To replicate the data from the producer tables into tables with different names on the consumer instance, click **Enable Transform**.

        For more information, see [Transform replication data](modify-replicated-data.md).

    4.  Click **Update**.


## What to do next

The consumer instances contain, at a minimum, the current data in the producer replication set tables. The consumer instances are now ready to accept replicated data updates. By default, the data in the producer tables is replicated into tables and table columns of the same name on the consumer instances. For more information about how to map the data into different tables and table columns and how to modify the data as it is replicated, see [Transform replicated data](modify-replicated-data.md).

-   [Map the replication data to different tables](modify-replicated-data.md) on the consumer instance.
-   [Modify the values](modify-replicated-data.md) during replication.
-   Set up business rules to [trigger post-replication workflows](post-replication-actions.md).

**Parent Topic:**[Configuring Instance Data Replication](../concept/configuring-instance-data-replication.md)

**Related topics**  


[Create a producer replication set in Instance Data Replication](create-p-replication-set.md)

[Seed a consumer instance for Instance Data Replication](seed-consumer-instance.md)

[Trigger a workflow after replication using Instance Data Replication](post-replication-actions.md)

[Reconfigure a replication set in Instance Data Replication](change-replication-set-config.md)

[Manage consumer access to replication data in Instance Data Replication](approve-consumer.md)

[Transform replication data for Instance Data Replication](modify-replicated-data.md)

[Set up bidirectional replication in Instance Data Replication](bi-directional-replication.md)

[Create a discrete producer replication set for Instance Data Replication](discrete-producer-replication-set.md)

