---
title: Perform a manual observable enrichment in Microsoft Defender for Endpoint
description: Select individual or multiple observables and perform a manual observable enrichment to enrich observables with additional information from Microsoft Defender for Endpoint.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and configure profile, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Perform a manual observable enrichment in Microsoft Defender for Endpoint

Select individual or multiple observables and perform a manual observable enrichment to enrich observables with additional information from Microsoft Defender for Endpoint.

## Before you begin

Role required: sn\_si.analyst

## About this task

The Microsoft Defender for Endpoint integration enables observable enrichment for all the observable types that are mapped in the Observable-Indicator Mapping module.

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the Microsoft Defender for Endpoint information.

3.  Click **Show All related lists**.

4.  Click the **Associated Observables** tab.

5.  Select the observables.

6.  From the Actions list, click **Run Observable Enrichment**.

7.  Select a Microsoft Defender for Endpoint **source** and move it to the **Selected** column to specify which implementation you want to use to enrich the selected observables.

8.  Click **Submit**.

9.  To validate the status of the execution, view the work notes.

10. To view the results, click **Microsoft Defender Indicator** tab.

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


