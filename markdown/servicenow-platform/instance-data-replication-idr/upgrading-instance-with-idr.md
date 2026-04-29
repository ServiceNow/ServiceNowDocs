---
title: Upgrading your instance with Instance Data Replication enabled
description: When upgrading your instance, IDR automatically pauses replication to maintain data replication without any manual intervention.
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2026-03-12"
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

**Parent Topic:**[Configuring Instance Data Replication](configuring-instance-data-replication.md)

