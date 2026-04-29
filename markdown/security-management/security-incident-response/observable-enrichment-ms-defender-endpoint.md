---
title: Perform an automatic observable enrichment in Microsoft Defender for Endpoint
description: Perform an automatic observable enrichment in Microsoft Defender for Endpoint to enrich observables with additional information from various sources.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create and configure profile, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Perform an automatic observable enrichment in Microsoft Defender for Endpoint

Perform an automatic observable enrichment in Microsoft Defender for Endpoint to enrich observables with additional information from various sources.

## Before you begin

Verify that you have enabled the **Security Incident Response** system property. This option triggers the observable enrichment capability in SIR, whenever an observable is associated to a Security Incident.

Role required: sn\_si.admin, sn\_si.analyst

## About this task

You can use this capability during incident response investigations to contain an identified threat. When new observables are associated with the security incident, you can enable the observable enrichment in Microsoft Defender for Endpoint capability to run automatically.

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the Microsoft Defender for Endpoint information.

3.  Validate the automation activity once the new observables have been associated with the security incident.

4.  View the results the enrichment results in the Indicators related list of the security incident.

    You can use the following table for more information on the observable enrichment.

    |Field|Description|
    |-----|-----------|
    |Indicator ID|Identity of the Indicator entity. Click **Open** to view the record in detail in the ServiceNow AI Platform instance|
    |Observable|The observable associated with the result.|
    |Title|Title for the indicator.|
    |Indicator Type|Type of the indicator.|
    |Action|Action performed by the indicator.|
    |Recommended Action|Recommended actions for the indicator.|
    |Integration Vendor|Defender source integration from which the data is retrieved.|
    |Expiration Date|Expiration time for the indicator.|
    |Retrieval Date|Date when the enrichment record is created.|


