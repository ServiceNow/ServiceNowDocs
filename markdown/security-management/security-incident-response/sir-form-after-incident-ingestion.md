---
title: SIR form after an incident ingestion
description: After the ServiceNow AI Platform ingests the Microsoft Azure Sentinel incident, a security incident is created and the updates are made to that security incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/sir-form-after-incident-ingestion.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# SIR form after an incident ingestion

After the ServiceNow AI Platform ingests the Microsoft Azure Sentinel incident, a security incident is created and the updates are made to that security incident record.

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

## Work notes

A work note is posted when an incident is aggregated and if you have configured the **Log work note for new incident** option in the [Incident Aggregation Criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/filter-and-aggregation-criteria.md). The following example shows the work notes in SIR.

\[Omitted image "sentinel-worknotes.png"\] Alt text: Work notes in SIR.

When you click the incident number, you can view the internal incident import record that contains the raw incident data. The following example shows the raw incident data in SIR.

\[Omitted image "sentinel-incident-raw.png"\] Alt text: View the incident raw data in SIR.

When you click the **Click here** link, you can view the record in the Microsoft Azure Sentinel environment. The following example shows the record in the Microsoft Azure Sentinel environment.

\[Omitted image "sentinel-record.png"\] Alt text: Incident record in Azure Sentinel

## Aggregated Sentinel Incidents

View Aggregated Sentinel Incidents: View the incidents that are aggregated to the security incident. Navigate to **Show All Related Lists** &gt; **Aggregated Microsoft Azure Sentinel incidents**.

\[Omitted image "Sentinel-aggregated-related-lists.png"\] Alt text: Incidents that are aggregated to the security incident.

Create security incident: Select an incident from the list, click the **Actions** menu, and then click **Create security incident**. This option creates a new security incident for the incident and this incident is de-aggregated from the parent security incident.

\[Omitted image "sentinel-create-incident.png"\] Alt text: Security incident and de-aggregate from the parent security incident.

## Azure Sentinel Alerts

To view the alerts that are associated with the Sentinel Incident that triggered the security incident, navigate to **Show All Related Lists** &gt; **Azure Sentinel Alerts**.

\[Omitted image "azure-sentinel-alerts.png"\] Alt text: Alerts that are associated with the Sentinel incident that triggered the security incident.

