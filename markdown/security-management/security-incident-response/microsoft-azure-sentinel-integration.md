---
title: Microsoft Azure Sentinel integration
description: Microsoft Azure Sentinel is a cloud-based Security Information Event Management \(SIEM\) and Security Orchestration Automated Response \(SOAR\) solution. You can use the Microsoft Azure Sentinel integration to ingest Azure Sentinel incidents and automatically create security incidents in Security Incident Response.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Microsoft Azure Sentinel integration

Microsoft Azure Sentinel is a cloud-based Security Information Event Management \(SIEM\) and Security Orchestration Automated Response \(SOAR\) solution. You can use the Microsoft Azure Sentinel integration to ingest Azure Sentinel incidents and automatically create security incidents in Security Incident Response.

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), migrate to the new Defender portal integration as soon as possible. The Defender integration built-in migration utility automatically converts your existing Sentinel profiles to Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Overview of Microsoft Azure Sentinel integration

See the following diagram to learn how Microsoft Azure Sentinel integrates with the ServiceNow AI Platform Security Operations applications.

![How Azure Sentinel integrates with the ServiceNow AI Platform.](../image/sentinel-overview.png)

## Key features

Use the key features of this integration to do the following actions:

-   Discover Microsoft Azure Sentinel incidents that are candidates for security incidents and automate the creation of these security incidents.
-   Map Microsoft Azure Sentinel incident and entity fields to SIR security incident fields.
-   Filter Microsoft Azure Sentinel incidents.
-   Aggregate incidents to existing open security incidents so that you don't have to create duplicate security incidents.
-   Automate Microsoft Azure Sentinel incident status updates for Security Incident Response so that you can create and close security incidents.

    **Note:** ServiceNow updates the status of Microsoft Azure Sentinel incidents based on the security incident creation or closure. This update also includes comments of aggregated incidents and new incidents.

-   Schedule incident ingestion to create security incidents periodically.
-   Synchronize Microsoft Azure Sentinel incident comments with SIR Work notes.

## Learn about this integration

|Document identifier|Document title|
|-------------------|--------------|
|Microsoft product documentation website|[Microsoft Product Documentation website](https://docs.microsoft.com/en-us/azure/sentinel/)|
|ServiceNow product documentation website|[ServiceNow Product Documentation website](https://servicenow.com/docs)|

