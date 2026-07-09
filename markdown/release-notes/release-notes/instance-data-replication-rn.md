---
title: Instance Data Replication release notes
description: The ServiceNow Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Instance Data Replication release notes

The ServiceNow® Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Zurich release.

## Instance Data Replication highlights for the Zurich release

-   Monitor the progress of all your scheduled replication sets.
-   Track the progress of scheduled replication requests within a scheduled replication set.
-   Access details of scheduled replication requests within a scheduled replication set.

See [Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/instance-data-replication.md) for more information.

## Important information for upgrading Instance Data Replication to Zurich

-   Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading your replication sets to V2, which uses Hermes Messaging Service. For details, see [Upgrading legacy replication sets to V2 in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/upgrading-legacy-replication-sets-v2.md).
-   Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is composed of seven shards, with five days for each shard. All log entries in this table created before the upgrade are automatically truncated.

## New in the Zurich release

-   **[Monitor scheduled replication sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/instance-data-replication-dashboard.md)**

    Monitor the progress your scheduled replication sets in the IDR Monitoring Dashboard.

-   **[Track scheduled replication requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/set-up-scheduled-replication-idr.md)**

    Track the progress of scheduled replication requests in the Scheduled Replication Requests related list.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Removed in this release

-   The Key Management Service test has been removed from the IDR Diagnostics page.
-   The VAULT Service Status test has been removed from the IDR Diagnostics page.

## Deprecations

Legacy replication sets have been deprecated in the Zurich release and are no longer supported.

## Activation information

Instance Data Replication is a ServiceNow AI Platform feature that is available with activation of the IDR \(com.glide.idr\) plugin, which requires a separate subscription. For details, see [Request an Instance Data Replication subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/request-instance-data-replication.md).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/hermes-messaging-service.md)**

    Hermes Messaging Service is a multi-tenant, multi-cluster data transport and queuing service built on Apache Kafka that enables your instance to produce and consume large volumes of Kafka events reliably.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-capabilities-rn-landing.md)

