---
title: Comparing Microsoft Azure Sentinel and Microsoft Graph Security API integrations with SIR
description: You can view the differences between Microsoft Azure Sentinel and Microsoft Graph Security API integrations and choose the right integration with your ServiceNow AI Platform instance.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Comparing Microsoft Azure Sentinel and Microsoft Graph Security API integrations with SIR

You can view the differences between Microsoft Azure Sentinel and Microsoft Graph Security API integrations and choose the right integration with your ServiceNow AI Platform instance.

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

## Microsoft Azure Sentinel - Incident Ingestion overview

Microsoft Azure Sentinel is a cloud-based security information event management \(SIEM\) and security orchestration automated response \(SOAR\) solution. Microsoft Azure Sentinel delivers intelligent security analytics and threat intelligence across the enterprise. It provides a single solution for alert detection, threat visibility, proactive hunting, and threat response.

## Microsoft Graph Security API overview

The Microsoft Graph Security API is an intermediary service \(or broker\) that provides a single programmatic interface for connecting multiple security providers \(Native to Microsoft as well as ServiceNow Partners\).

The Microsoft Graph Security API integration addresses these issues by using the Microsoft Graph Security API to connect with different Microsoft security technologies like Azure Sentinel, Microsoft Defender Advanced Threat Protection, and Azure Advanced Threat Protection. Alerts from Microsoft Security providers are ingested and security incidents are automatically created in Security Incident Response.

## Summary of feature differences

![A visual comparision of Azure Sentinel and Graph API](../image/sentinel-graph-api.png)

<table id="table_azf_vmp_wpb"><thead><tr><th>

Microsoft Azure Sentinel

</th><th>

Microsoft Graph Security API

</th></tr></thead><tbody><tr><td>

Ingests Microsoft Azure Sentinel incidents along with entity information \(when available\) and automates security incident creation in SIR.

</td><td>

Ingests alerts from multiple Security providers \(including Azure Sentinel\) in a standard schema and automates security incident creation in SIR.

</td></tr><tr><td>

Automates Microsoft Azure Sentinel incident status updates for Security Incident Response so that you can create and close security incidents.**Note:** ServiceNow updates the status of Microsoft Azure Sentinel incidents based on the security incident creation or closure.

</td><td>

Supports alert updates \(alert status change and alert closure\) for selected security providers.**Note:** For more information on the Microsoft Graph Security API supported security providers, view the [Microsoft documentation](https://docs.microsoft.com/en-us/graph/api/resources/security-api-overview?view=graph-rest-1.0).

</td></tr><tr><td>

Use this integration if your scenario includes the following conditions:-   Preliminary incident investigation is in Microsoft Azure Sentinel and subsequent investigation is in SIR
-   Ingest Microsoft Azure Sentinel incidents to SIR

</td><td>

Use this integration if your scenario includes the following conditions:-   Perform incident investigation in SIR.
-   Ingest Microsoft Azure Sentinel alerts in SIR.
-   Incidents are not created in Microsoft Azure Sentinel.

</td></tr><tr><td>

Alert is an entity in Microsoft Azure Sentinel. You cannot retrieve standalone or specific alerts using the Microsoft Azure Sentinel Management API. You can only retrieve the alert data associated with an incident. The alert data available using this integration is richer than the alert data available using the Microsoft Graph Security API.

</td><td>

The Microsoft Azure Sentinel normalized alert data is available. The Microsoft Azure Sentinel alert fields that are mapped internally in Microsoft Graph Security API, and are available in Microsoft Graph Security API, are available for use in this integration.

</td></tr><tr><td>

 

</td><td>

You cannot update alerts in Microsoft Azure Sentinel using this integration.

</td></tr></tbody>
</table>