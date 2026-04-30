---
title: Upgrading legacy replication sets to V2 in Instance Data Replication
description: Improve message processing and replication performance by upgrading your legacy replication sets in IDR to V2.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-05-13"
reading_time_minutes: 3
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Upgrading legacy replication sets to V2 in Instance Data Replication

Improve message processing and replication performance by upgrading your legacy replication sets in IDR to V2.

## Legacy and V2 replication sets

**Important:** Legacy replication sets are planned for deprecation by the Zurich release. To continue replicating data, you must upgrade all legacy replication sets to V2.

-   Legacy replication sets use a ServiceNow Kafka message transport and delivery implementation that was created prior to the Utah release. All replication sets created prior to the Utah release are considered legacy replication sets.

    Beginning with the Washington DC release, you can no longer create legacy replication sets.

-   V2 replication sets use the ServiceNow Hermes Messaging Service for Kafka message transport and delivery, which replicates data faster, at scale, and with high reliability. The Hermes Messaging Service is a ServiceNow AI Platform capability that's automatically enabled when the IDR plugin \(com.glide.idr\) is activated. All replication sets created after the Washington DC release are V2 replication sets.

**Note:** Data sent from a V2 producer replication set is retained in the message queue for 24 hours.

## Upgrading legacy replication sets

Upgrade your eligible legacy replication sets to V2 to take advantage of the benefits provided by Hermes. Upgrading replication sets from legacy to V2 is a seamless process. Active data replication from the producer to consumer continues throughout the upgrade, which means you don't need to pause replication before you begin. Replication continues using the V2 replication sets after the upgrade is finished.

You can either create new V2 replication sets or upgrade existing legacy replication sets to V2. See [Upgrade legacy replication sets in Instance Data Replication](../task/upgrade-legacy-replication-sets.md).

## Upgrade eligibility

Legacy replication sets are eligible for upgrade to V2 when both the producer and consumer instance are on Utah or higher. Note that some Utah legacy replication sets aren't eligible for upgrade to V2, depending on their configuration \(for example, the replication set can't be bidirectional or discrete\).

You can confirm upgrade eligibility by viewing the producer replication set and checking the **Upgrade Eligibility** column in the Consumer Subscriptions related list.

-   If the value for each subscribed consumer is **Eligible**, you can begin the upgrade process by following the steps in [Upgrade legacy replication sets in Instance Data Replication](../task/upgrade-legacy-replication-sets.md).
-   If the value for a subscribed consumer is **Not eligible**, this means that either the consumer instance isn't on Utah or higher, or the consumer replication set is on Utah, but isn't eligible for upgrade to V2 because of its configuration.

For details on which types of legacy replication sets are eligible for upgrade in Utah, refer to the "Upgrading legacy replication sets to V2" topic in the Utah version of the IDR documentation.

## Compatibility

V2 producer replication sets are compatible only with V2 consumer replication sets.

If you upgrade a producer replication set to V2, you must upgrade the subscribed consumer replication sets to V2 as well to take advantage of the V2 processing improvements.

-   **[Upgrade legacy replication sets in Instance Data Replication](../task/upgrade-legacy-replication-sets.md)**  
Replicate high volumes of data faster and more reliably by upgrading your Instance Data Replication \(IDR\) legacy producer and consumer replication sets to V2.
-   **[Rolling back an upgrade in Instance Data Replication](rolling-back-an-upgrade.md)**  
If a problem occurs during an upgrade to V2, the upgrade is rolled back in Instance Data Replication \(IDR\).

**Parent Topic:**[Configuring Instance Data Replication](configuring-instance-data-replication.md)

**Related topics**  


[Request an Instance Data Replication subscription](../task/request-instance-data-replication.md)

[Preparing for Instance Data Replication](prepare-instance-data-replication.md)

[Preserving table hierarchy in Instance Data Replication](preserving-table-hierarchy.md)

[Upgrading your instance with Instance Data Replication enabled](upgrading-instance-with-idr.md)

