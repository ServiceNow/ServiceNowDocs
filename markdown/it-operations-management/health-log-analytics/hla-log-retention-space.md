---
title: Storage space for log retention in Health Log Analytics
description: The Health Log Analytics base system typically provides 1,000 GB storage space for log source retention, although the storage capacity may vary depending on your license. The default retention time for logs is three days, but you can modify that period.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Health Log Analytics administration, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Storage space for log retention in Health Log Analytics

The Health Log Analytics base system typically provides 1,000 GB storage space for log source retention, although the storage capacity may vary depending on your license. The default retention time for logs is three days, but you can modify that period.

This feature is supported in the Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). To activate it, contact your ServiceNow account manager or ServiceNow Support.

When the storage space used by all log sources exceeds 80 percent of the total, you receive an email notification. You can change the default threshold percentage by modifying the **sn\_occ.elastic\_storage.utilization\_limit.percent** system property in the System Properties table.

## Automatic reduction of log retention days

By default, logs are retained for three days. You can adjust this period to 3, 7, 14, or 30 days. For more information, see [Modify the log source retention period](../task/hla-log-retention.md).

If the storage space used by all log sources reaches 100 percent, the number of retention days allocated per source is automatically lowered by one level and you receive an email notification with the specifics. The automatic reduction process starts with the sources that were allocated the highest number of retention days. For example, for a source with 30 retention days, the number is reduced to 14. If the source has 14 retention days, the number is reduced to 7, and so on.

You can change the threshold percentage for the automatic reduction of log retention days by modifying the **sn\_occ.log\_retention.automatic\_reduction\_utilization\_percent** system property in the System Properties table.

-   **[Modify the log source retention period](../task/hla-log-retention.md)**  
Modify the period that Health Log Analytics retains logs from a specific source. You can calculate the impact of your intended change on storage to help you make an informed decision.

**Parent Topic:**[Health Log Analytics administration](hla-administer.md)

**Related topics**  


[Modify the log source retention period](../task/hla-log-retention.md)

