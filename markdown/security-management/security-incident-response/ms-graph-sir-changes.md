---
title: Security incident Response form after alert ingestion
description: After a Microsoft Graph Security API alert has been ingested, a security incident is created and the corresponding updates are made to the security incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/ms-graph-sir-changes.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security incident Response form after alert ingestion

After a Microsoft Graph Security API alert has been ingested, a security incident is created and the corresponding updates are made to the security incident record.

## Worknotes

If you had selected the **Log work note for new alert** option in the alert Aggregation Criteria as described in the [Mapping alerts to security incident response fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/ms-graph-create-profile-map.md), a worknote is posted when the alert is aggregated.

Select the alert link to navigate to the internal alert import record that contains raw alert data.

## Aggregated alerts

Select **Related Lists** &gt; **Aggregated Microsoft Graph Security alerts** to view the alerts aggregated to the security incident.

-   **Create security incident**: Select an alert from the list, select the **Actions** menu and select **Create security incident**. This option creates a new security incident for the alert and this alert is de-aggregated from the parent security incident.
-   **Delete alert record**: Select an alert from the list, select the **Actions** menu and select **Delete**. This option deletes the alert record.

