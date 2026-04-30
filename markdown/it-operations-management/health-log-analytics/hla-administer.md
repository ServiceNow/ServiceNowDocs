---
title: Health Log Analytics administration
description: Health Log Analytics enables you to configure system properties, enable or disable system features, and view system health notifications.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Health Log Analytics administration

Health Log Analytics enables you to configure system properties, enable or disable system features, and view system health notifications.

-   **[Configure Health Log Analytics system properties for a single log source](../task/hla-system-properties-configure-single.md)**  
Configure system properties for a specific log source if you need to alter the default values, which should not usually be necessary.
-   **[Enable or disable Health Log Analytics system features](../task/hla-features-configure.md)**  
Customize the basic configuration of Health Log Analytics by enabling or disabling system features.
-   **[Alert notification in Slack or Microsoft Teams channels](hla-alert-notification-in-channel.md)**  
Health Log Analytics sends notifications for new anomaly alerts in real time to Slack or Microsoft Teams channels. This built-in functionality frees you from having to continuously monitor logs to prevent incidents.
-   **[Enhancing the CMDB with host data found in logs](hla-cmdb-enrich-concept.md)**  
When Health Log Analytics streams logs, it extracts host data from the log events. If host data is discovered that doesn't match the information in the Configuration Management Database \(CMDB\), the system creates a configuration item \(CI\) candidate based on the data it found in the logs for you to review.
-   **[Storage space for log retention in Health Log Analytics](hla-log-retention-space.md)**  
The Health Log Analytics base system typically provides 1,000 GB storage space for log source retention, although the storage capacity may vary depending on your license. The default retention time for logs is three days, but you can modify that period.
-   **[Scaling Health Log Analytics to stream logs at a higher rate](hla-scaling.md)**  
Stream log data to Health Log Analytics in a scalable, more stable way using the advanced ServiceNow infrastructure.

**Parent Topic:**[Configuring Health Log Analytics](hla-configuring.md)

