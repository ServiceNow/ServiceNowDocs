---
title: Upgrading your instance with Instance Data Replication enabled
description: When upgrading your instance, IDR automatically pauses replication to maintain data replication without any manual intervention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/instance-data-replication-idr/upgrading-instance-with-idr.html
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Upgrading your instance with Instance Data Replication enabled

When upgrading your instance, IDR automatically pauses replication to maintain data replication without any manual intervention.

Upgrading your instance with Instance Data Replication \(IDR\) enabled is a seamless process.

-   IDR doesn't consume or produce messages during an instance upgrade. IDR jobs are automatically stopped when the upgrade begins.
-   The data\_replication\_queue tracks the timestamp of the last message sent. This ensures that replication resumes from the last change made prior to the upgrade.
-   Any seeding in progress before the upgrade will be automatically paused when the upgrade starts and will resume once the upgrade is completed. To ensure that seeding completes without interruptions, avoid initiating a seeding request before an upgrade.
-   Seeding requests can't be initiated during an instance upgrade.
-   Replication resumes immediately after the upgrade is completed. There is no need to make any adjustments to IDR for record replication to continue.

**Parent Topic:**[Configuring Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/instance-data-replication-idr/configuring-instance-data-replication.md)

**Related topics**  


[Request an Instance Data Replication subscription]()

[Preparing for Instance Data Replication]()

[Preserving table hierarchy in Instance Data Replication]()

[Upgrading legacy replication sets to V2 in Instance Data Replication]()

