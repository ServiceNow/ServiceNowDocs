---
title: Upgrade legacy replication sets in Instance Data Replication
description: Replicate high volumes of data faster and more reliably by upgrading your Instance Data Replication \(IDR\) legacy producer and consumer replication sets to V2.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Upgrading legacy sets, Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Upgrade legacy replication sets in Instance Data Replication

Replicate high volumes of data faster and more reliably by upgrading your Instance Data Replication \(IDR\) legacy producer and consumer replication sets to V2.

## Before you begin

Role required: admin

## About this task

**Important:** Legacy replication sets are planned for deprecation by the Zurich release. To continue replicating data, you must upgrade all legacy replication sets to V2.

## Procedure

1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

2.  Select a producer replication set that you want to upgrade.

3.  Verify that the producer replication set is eligible for upgrade by checking the **Upgrade Eligibility** column on the Consumer Subscriptions related list.

    -   If the value for each consumer is **Eligible**, you can upgrade the replication set.
    -   If the value for any consumer **Not eligible**, this means that either the consumer instance isn't on Utah or higher, or the consumer replication set is on Utah, but isn't eligible for upgrade to V2 because of its configuration. See [Upgrade eligibility](../concept/upgrading-legacy-replication-sets-v2.md#section_r2w_4b5_lvb) for more information.
4.  Create a V2 producer replication set.

    1.  On the Producer Replication Set form, select **Upgrade**.

    2.  In the dialog box, either accept the default name or enter a unique replication set name.

        By default, the system appends -V2 to the legacy replication set name, but you can use any valid set name to differentiate the V2 version from the legacy version.

    3.  Select **OK**.

    The legacy producer replication set is copied to create a V2 producer replication set. The producer instance sends metadata to the consumer instance, which enables you to upgrade the legacy consumer replication set.

5.  On the consumer instance, navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**.

6.  Select the legacy consumer replication set that's subscribed to the producer replication set you upgraded.

7.  Upgrade the legacy consumer replication set.

    If the **Begin upgrade** button doesn't appear on the Consumer Replication Set form, resend the metadata from the producer replication set:

    1.  Select **Begin upgrade**.

    2.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

    3.  Select the new V2 producer replication set.

    4.  Select the check box next to the consumer subscription in the Consumer Subscriptions related list.

    5.  Select the **Actions on selected rows** list.

    6.  Select **Resend Metadata**.

    The V2 consumer replication set is created, and the producer instance sends metadata replication entries to the consumer instance. After all the entries are received, the **Start dry run** button appears on the Consumer Replication Set form.

8.  Confirm that the consumer instance can connect to the Hermes Messaging Service and that replication succeeds by selecting **Start dry run**.

    Data is consumed from the Kafka topic by the consumer instance but not persisted in the database yet.

9.  Complete the upgrade by activating the V2 consumer replication set with or without data integrity checks.

    -   Ensure that the legacy and V2 topics are in sync by selecting **Finish upgrade**.

        This option ensures that IDR performs all necessary data integrity checks before activating the V2 consumer replication set. If any data integrity checks fail, the upgrade is automatically rolled back to prioritize data consistency.

    -   Complete the upgrade without data integrity checks by selecting **Finish upgrade without sync**.

        This option allows you to complete the upgrade for replication sets where the consumer replication is lagging or no records have been replicated to the V2 topic. However, it may skip replicated records or attempt to duplicate replication. If you have concerns over missing or mismatched records, you can create a data comparison request to reseed those records.

    **Note:** If the **Finish upgrade** button doesn't appear on the Consumer Replication Set form, contact Customer Service and Support.

    The V2 consumer replication set is activated and the legacy consumer replication set is automatically deactivated.

10. After all subscribed consumers are upgraded to V2, deactivate the legacy producer replication set.

    **Note:** Legacy consumer replication sets stop consuming when you deactivate the legacy producer, so you must ensure all subscribed consumers are upgraded to V2 before you deactivate it.

    1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

    2.  Select the legacy producer replication set that you upgraded.

    3.  Select **Deactivate**.

    4.  Confirm deactivation by selecting **OK**.


## Result

The legacy producer and consumer replication sets are upgraded to V2 and the upgrade status changes to Up to date. Data replication continues based on the last message ID that was processed by the legacy replication set.

**Parent Topic:**[Upgrading legacy replication sets to V2 in Instance Data Replication](../concept/upgrading-legacy-replication-sets-v2.md)

