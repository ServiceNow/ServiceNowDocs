---
title: Configure and enable VirusTotal Integration
description: Set up VirusTotal integration with Threat Intelligence Security Center to perform threat lookups on observables.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
breadcrumb: [TISC VirusTotal integration, Threat Lookup, TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure and enable VirusTotal Integration

Set up VirusTotal integration with Threat Intelligence Security Center to perform threat lookups on observables.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Important:** type="note"&gt;The Threat Intelligence Security Center and VirusTotal Threat Lookup plugins must be installed and active.

Download the VirusTotal integration from the ServiceNow Store. Verify you have a valid VirusTotal account before use. For more information see, [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

This integration requires a valid VirusTotal API key and enables automated security analysis.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Threat Lookup**.

    **Note:** After installation is complete, access VirusTotal. Obtain the API Key under your VirusTotal profile.

2.  Select **Configure New Enrichment** to configure **VirusTotal** integration.

3.  Complete the fields on the Configure New Enrichment form.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the new enrichment integration. For example, VirusTotal.|
    |Vendor Name|Name of the vendor. The details of the selected vendor is populated by default. For example, VirusTotal.|
    |Integration Type|Type of integration that you selected. For example, Threat Lookup.|
    |Description|Description for the new enrichment integration.|

4.  Navigate to **Integration Configuration** section.

5.  In the **API Key** field, enter the API key you acquired from the VirusTotal site.

6.  Select **Save** to apply the changes.

    The system validates the integration details. By default, the VirusTotal integration status is inactive.

7.  Select **Enable** to enable the VirusTotal integration.


## Result

After configuration, you can select VirusTotal to perform lookups on observables in Threat Intelligence Security Center.

**Parent Topic:**[TISC VirusTotal integration](../concept/tisc-virustotal-integration_0.md)

