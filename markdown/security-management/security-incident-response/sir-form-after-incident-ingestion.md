---
title: SIR form after an incident ingestion
description: After the ServiceNow AI Platform ingests the Microsoft Azure Sentinel incident, a security incident is created and the updates are made to that security incident record.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# SIR form after an incident ingestion

After the ServiceNow AI Platform ingests the Microsoft Azure Sentinel incident, a security incident is created and the updates are made to that security incident record.

## Work notes

A work note is posted when an incident is aggregated and if you have configured the **Log work note for new incident** option in the [Incident Aggregation Criteria](filter-and-aggregation-criteria.md#). The following example shows the work notes in SIR.

![Work notes in SIR.](../image/sentinel-worknotes.png "Viewing work notes in SIR")

When you click the incident number, you can view the internal incident import record that contains the raw incident data. The following example shows the raw incident data in SIR.

![View the incident raw data in SIR.](../image/sentinel-incident-raw.png "Viewing the incident raw data in SIR")

When you click the **Click here** link, you can view the record in the Microsoft Azure Sentinel environment. The following example shows the record in the Microsoft Azure Sentinel environment.

![Incident record in Azure Sentinel](../image/sentinel-record.png "Viewing the incident record in Azure Sentinel")

## Aggregated Sentinel Incidents

View Aggregated Sentinel Incidents: View the incidents that are aggregated to the security incident. Navigate to **Show All Related Lists** &gt; **Aggregated Microsoft Azure Sentinel incidents**.

![Incidents that are aggregated to the security incident.](../image/Sentinel-aggregated-related-lists.png)

Create security incident: Select an incident from the list, click the **Actions** menu, and then click **Create security incident**. This option creates a new security incident for the incident and this incident is de-aggregated from the parent security incident.

![Security incident and de-aggregate from the parent security incident.](../image/sentinel-create-incident.png)

## Azure Sentinel Alerts

To view the alerts that are associated with the Sentinel Incident that triggered the security incident, navigate to **Show All Related Lists** &gt; **Azure Sentinel Alerts**.

![Alerts that are associated with the Sentinel incident that triggered the security incident.](../image/azure-sentinel-alerts.png "Azure Sentinel Alerts")

