---
title: Rolling back an upgrade in Instance Data Replication
description: If a problem occurs during an upgrade to V2, the upgrade is rolled back in Instance Data Replication \(IDR\).
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-05-13"
reading_time_minutes: 1
breadcrumb: [Upgrading legacy sets, Instance Data Replication set up, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Rolling back an upgrade in Instance Data Replication

If a problem occurs during an upgrade to V2, the upgrade is rolled back in Instance Data Replication \(IDR\).

**Important:** Legacy replication sets are planned for deprecation by the Zurich release. To continue replicating data, you must upgrade all legacy replication sets to V2.

If you upgrade a legacy replication set to V2 and a problem occurs with the upgrade, the upgrade is automatically rolled back to ensure data consistency. If a processing delay caused the issue, you can try the upgrade again.

For example, when the consumer instance identifies the most recent message in the legacy topic, but can’t find that same message in the Hermes topic, the upgrade is rolled back. If you attempt the upgrade again and the consumer instance successfully finds the most recent message in the Hermes topic, the upgrade continues, and processing begins only from the Hermes topic.

-   If the legacy consumer job is still processing records that were replicated prior to when the upgrade started replicating to both the legacy and the Hermes topics, the upgrade is rolled back. In this scenario, allow time for the consumer to process the replication backlog and then try the upgrade to V2 again. For example, if the lag persists after 30 minutes, wait another 2 hours and try again, or wait 24 hours and try again.
-   If no records are being replicated from the producer to the Hermes topic after the upgrade starts, wait and retry the upgrade after allowing at least one record to replicate from the producer to the consumer. Alternatively, you can manually trigger replication by making a change to at least one record.
-   If you want to complete the upgrade without data integrity checks, you can use the **Finish upgrade without sync** option after performing the dry run.

    This option allows you to complete the upgrade for replication sets where the consumer replication is lagging or no records have been replicated to the V2 topic. However, it may skip replicated records or attempt to duplicate replication. If you have concerns over missing or mismatched records, you can create a data comparison request to reseed those records.


**Parent Topic:**[Upgrading legacy replication sets to V2 in Instance Data Replication](upgrading-legacy-replication-sets-v2.md)

