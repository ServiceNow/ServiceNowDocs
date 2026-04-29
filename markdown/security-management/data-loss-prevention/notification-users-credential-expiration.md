---
title: Email notifications on credential expiration
description: When the token used in the ServiceNow instance expires, Netskope integration sends out an email notification to users with the DLP Admin \(sn\_dlir.admin\) role.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response Integration with Netskope, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Email notifications on credential expiration

When the token used in the ServiceNow instance expires, Netskope integration sends out an email notification to users with the DLP Admin \(sn\_dlir.admin\) role.

After the setup of the integration configuration is completed, provide the DLP Admin \(sn\_dlir.admin\) role to the users who should be notified if the token expired.

If the token expires, the data ingestion for associated profiles would be on hold until the Netskope integration configuration is updated with a valid token.

You must create a token or renew the old one on Netskope, and then update the token on the ServiceNow instance. If you renew the token by extending the expiry time, then the Netskope application automatically detects the renewal and will continue with the data collection. If you create a token, you must update the token in the configuration.

**Parent Topic:**[Data Loss Prevention Incident Response Integration with Netskope](../concept/dlp-incident-response-integration-netskope.md)

