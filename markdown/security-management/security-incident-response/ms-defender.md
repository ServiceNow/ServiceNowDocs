---
title: Microsoft Defender integration for Security Operations
description: The Microsoft Defender integration for ServiceNow Security Operations ingests alerts and incidents into the ServiceNow Security Incident Response \(SIR\) platform for centralized case management. Bi-directional synchronization keeps status and work notes aligned across both platforms, ensuring teams working in either system maintain consistent information without discrepancies.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-01-06"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Microsoft Defender integration for Security Operations

The Microsoft Defender integration for ServiceNow Security Operations ingests alerts and incidents into the ServiceNow Security Incident Response \(SIR\) platform for centralized case management. Bi-directional synchronization keeps status and work notes aligned across both platforms, ensuring teams working in either system maintain consistent information without discrepancies.

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), migrate to the new Defender portal integration as soon as possible. The Defender integration built-in migration utility automatically converts your existing Sentinel profiles to Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Microsoft Defender and Security Operations

See the following diagram to learn how the Microsoft Defender incident flows with Security Operations applications.

![Microsoft Defender and Security Operations](../image/md-secops.png)

## Key Features

This integration includes the following key features:

-   Create flexible event‑forwarding profiles to ingest Microsoft Defender incidents into ServiceNow SIR.
-   Ingest historical, ongoing, new, and updated notable events on configurable intervals.
-   Filter out noisy or low‑value alerts and bring only actionable notable events into SIR.
-   Map Microsoft Defender incident, alert, and event fields directly to SIR security incident fields.
-   Bi-directional synchronization of status, and work notes between Microsoft Defender and ServiceNow SIR.

## Roles Required

Microsoft Defender integration tasks involve the following roles.

-   sn\_si.admin: Can read, write, and delete records.
-   sn\_si.ingestion\_profile\_admin: Can read, write, and delete records.
-   sn\_si.analyst: Can read, write, and delete records.

For more information on Roles installed, see [Components installed with Security Incident Response](../../../security-incident-response/reference/installed-with-sir.md)

