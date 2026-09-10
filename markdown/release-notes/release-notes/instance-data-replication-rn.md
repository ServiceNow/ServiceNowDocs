---
title: Instance Data Replication release notes
description: The ServiceNow Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Australia release.The ServiceNow Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Instance Data Replication release notes

The ServiceNow® Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Australia release.

## About Instance Data Replication

View updated diagnostic test descriptions and results on the redesigned IDR Diagnostics page.

See [Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication.md) for more information.

## Activation and other requirements

-   **Activation information**

    IDR is a ServiceNow AI Platform feature that is available with activation of the IDR \(com.glide.idr\) plugin, which requires a separate subscription. For details, see [Request an Instance Data Replication subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/request-instance-data-replication.md).

-   **Upgrade information**

    Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is composed of seven shards, with five days for each shard. All log entries in this table that are created before the upgrade are automatically truncated.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-capabilities-rn-landing.md)

## Australia

The ServiceNow® Instance Data Replication \(IDR\) application simplifies the data replication process between instances. Instance Data Replication was enhanced and updated in the Australia release.

### What's new

-   **[IDR Diagnostics page improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/test-IDR-connectivity.md)**

    Access detailed test descriptions and results on the redesigned IDR Diagnostics page.


