---
title: Security Incident Response form after alert ingestion
description: After a Microsoft Graph Security API alert has been ingested, a security incident is created and the corresponding updates are made to the security incident record.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response form after alert ingestion

After a Microsoft Graph Security API alert has been ingested, a security incident is created and the corresponding updates are made to the security incident record.

## Worknotes

If you had selected the **Log work note for new alert** option in the alert Aggregation Criteria as described in the [Mapping alerts to security incident response fields](ms-graph-create-profile-map.md), a worknote is posted when the alert is aggregated.

![Microsoft Graph Security API: Log worknote](../image/ms-graph-worknote.png)

Click on the alert link to navigate to the internal alert import record that contains raw alert data.

![Microsoft Graph Security API Alert Import Record](../image/ms-graph-sir-alert-record.png)

## Aggregated alerts

Click **Related Lists** &gt; **Aggregated Microsoft Graph Security alerts** to view the alerts aggregated to the security incident.

![Microsoft Graph Security API: aggregated alerts](../image/ms-graph-related-aggregated.png)

-   **Create security incident**: Select an alert from the list, click the **Actions** menu and click **Create security incident**. This option creates a new security incident for the alert and this alert is de-aggregated from the parent security incident.
-   **Delete alert record**: Select an alert from the list, click the **Actions** menu and click **Delete**. This option deletes the alert record.

