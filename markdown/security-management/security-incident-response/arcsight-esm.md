---
title: ArcSight ESM Event Ingestion integration
description: The ArcSight ESM event ingestion integration with the Security Incident Response product allows security incident analysts to collect correlated events and automate creation of security incidents with the ServiceNow platform. Data is ingested continually based on a configured polling schedule, and it is used by analysts to identify and respond to potential cyber security threats.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# ArcSight ESM Event Ingestion integration

The ArcSight ESM event ingestion integration with the Security Incident Response product allows security incident analysts to collect correlated events and automate creation of security incidents with the ServiceNow platform. Data is ingested continually based on a configured polling schedule, and it is used by analysts to identify and respond to potential cyber security threats.

With this integration, correlated events that are candidates for security incidents can be ingested on a periodic basis. You can map fields in correlated events to security incident fields, preview the setup of an event as a security incident, and setup scheduled ingestion of events to automatically create security incidents on an ongoing basis.

## Overview of ArcSight ESM Event Ingestion integration

This integration provides a security operations center \(SOC\) analyst with visibility to correlation events in ArcSight ESM. This data can be integrated into ServiceNow AI Platform Security Incident Response \(SIR\) security incidents for further investigation and remediation. Profiles are created in your ServiceNow AI Platform instance to handle different correlation event types that are created and made available via correlation query viewers in ArcSight ESM. These profiles customize how different ArcSight ESM correlated event fields are displayed on SIR security incidents.

## Key features

This integration includes the following key features:

-   Create multiple event ingestion profiles to create SIR security incidents for specific types of threats such as malware and unauthorized access attempts.
-   Drag-and-drop mapping of ArcSight ESM correlation event field values to associated SIR security incident fields.
-   A preview of the SIR security incident layout based on sample correlation events to validate event mapping details.
-   Ingest historical correlation events as well as new notable events on configurable intervals.
-   Filter out correlation events that do not meet SIR incident generation criteria, e.g. low priority events
-   Aggregate events to existing SIR security incidents based on matching field values to avoid duplicate security incidents.
-   Update correlation events based on SIR incident creation and/or closure conditionals via a bi-directional interface.

## Supported ServiceNow AI Platform versions

This integration supports the New York Patch 6 and Orlando ServiceNow AI Platform releases.

The following Security Operations applications must be installed and activated from the ServiceNow Store. Install and then activate one application at a time in the order listed below to ensure a smooth installation:

1.  Security Integration Framework
2.  Security Support Common
3.  Security Incident Response
4.  Event and Alert Ingestion for Security Operations
5.  Integration Hub Plugins
    1.  ServiceNow Integration Hub Runtime
    2.  ServiceNow Integration Hub Action Step - REST

For more information about installing the Security Operations core applications, see [Get entitlement for a Security Operations product or application](../../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../../security-incident-response/task/activate-entitled-store-app.md).

## ArcSight ESM supported versions

This integration has been tested with Version 7.0.0.2436 of the ArcSight ESM Manager. The integration supports both ArcSight ESM on-premises and Cloud/Hosted service environments.

## MID Server

This integration requires an installed and configured MID Server in your ServiceNow AI Platform® instance to connect to the ArcSight ESM service when the ArcSight ESM server is deployed within your corporate network. If you are using the ArcSight ESM cloud service, a MID Server is not required. See the [ServiceNow Product Documentation website](https://servicenow.com/docs) for more information about MID Servers.

## References

|Reference|Document Identifier|Document Title|
|---------|-------------------|--------------|
|1|ArcSight ESM product documentation|[ArcSight product documentation](https://community.microfocus.com/t5/ArcSight-Product-Documentation/ct-p/productdocs).|
|2|ServiceNow Product documentation website|[ServiceNow Product Documentation website](https://servicenow.com/docs)|

