---
title: Notifications for users on retry mechanism
description: Netskope integration will retry the configured number of times in case of API failures during DLP Incident ingestion.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response Integration with Netskope, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Notifications for users on retry mechanism

Netskope integration will retry the configured number of times in case of API failures during DLP Incident ingestion.

Once the maximum retry limit is exceeded, Netskope integration sends out an email notification to users who have the DLP Admin \(sn\_dlir.admin\) role.

After you complete the integration setup and configuration, provide the DLP Admin \(sn\_dlir.admin\) role to the users who should be notified when the maximum retry limit exceeds.

Once the maximum retry limit is exceeded, the profile will skip ingestion for a duration of up to one hour. The maximum retries are configured using the property: `Maximum number of retries to be performed for API failures`. For more information, see[Configure Netskope DLP integration settings](../task/configure-netskope-dlp-integration-settings.md).

**Parent Topic:**[Data Loss Prevention Incident Response Integration with Netskope](dlp-incident-response-integration-netskope.md)

